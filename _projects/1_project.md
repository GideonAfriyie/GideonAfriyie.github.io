---
layout: page
title: 3D Topographic Modeling
description: Research Assistant
img: assets/img/IMG_6369.jpg
importance: 1
category: work
related_publications: false
---

**Gettysburg College · Research Assistant**

I am developing physical 3D topographic models of South Mountain region as part of the Advancing Science project @ Gettysburg College.

The work combines GIS data preparation, digital terrain modeling, and 3D printing. The goal is to create durable, touchable models that help students explore the region’s terrain and geographic features.

## Second Prototype

Building on an initial terrain-only print, the second prototype combines elevation data with roads, streams, lakes, the Appalachian Trail, and the Michaux State Forest boundary.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/IMG_6369 2.jpeg" title="Second 3D-printed prototype" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/feature_layout.png" title="Geographic feature layout" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Left: Completed second prototype. Right: Geographic reference showing roads in red, streams and lakes in blue, the Appalachian Trail in magenta, and the Michaux boundary in green. Colors identify features on the reference map; the physical model was printed in gray.
</div>

Features use different surface treatments:

- **Roads:** Raised, with different widths and heights for interstate highways, US highways, and Pennsylvania state routes.
- **Streams and lakes:** Recessed into the terrain.
- **Appalachian Trail:** Raised and dashed.
- **Michaux State Forest boundary:** Represented by a low ridge.

The printed model measures approximately **210 × 166 × 24 mm**, with a solid base and exaggerated terrain relief. Initial handling showed that the raised roads could be followed by touch, while the streams were less distinct. Further testing will guide refinements before producing additional models.

## GIS Data Preparation

I used QGIS to inspect attribute tables, filter the requested features, and prepare geographic layers for the model. The data included Pennsylvania state roads, NHD flowlines and waterbody polygons, the Appalachian Trail, and landscape and forest boundaries.

The road selection retained **11 highway routes**. For example, this QGIS attribute expression selects the requested route numbers:

```sql
"T_RT_NO" IN (
  '0081',
  '0011', '0015', '0030',
  '0016', '0034', '0094', '0174',
  '0233', '0316', '0997'
)
```

Stream selection used the `GNIS_NAME` field, with a unique-value check confirming **13 distinct stream names** in the main exported network. Falling Spring Branch was saved separately. Lake preparation involved selecting named records and inspecting an unnamed waterbody as a candidate for Lake Meade.

The prepared vector layers were saved as GeoPackages for use in the model-building workflow.

## Building the Combined STL

Using AI-assisted Python workflow, I combined the prepared geographic layers with the elevation raster. The script transformed the layers into a common coordinate system, clipped features to the selected South Mountain boundary, and converted elevation values into a solid terrain surface.

It then added the raised and recessed features. This excerpt from the build script assigns different road widths and heights before adding them to the terrain:

These feature dimensions are enlarged for tactile representation rather than drawn at their real-world widths.

The completed mesh was checked for a closed surface, exported as an STL, and prepared in Creality Print. The 2nd prototype was printed at the college’s Innovation and Creativity Lab and reviewed with the supervising professor.

<div class="row">
  <div class="col-sm-8 mx-auto mt-3">
    {% include figure.liquid loading="lazy" path="assets/img/IMG_6299.jpeg" title="Combined STL preview" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Digital preview of the combined STL, showing the terrain relief and solid base before printing.
</div>

## First Prototype and Early Workflow

The first prototype used TouchTerrain to generate a terrain STL. It provided an initial test of terrain relief, model scale, slicing, and printing before adding the geographic features.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/prototype.jpeg" title="First 3D-printed terrain prototype" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/digital model.jpeg" title="Initial digital terrain model" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Left: First physical terrain prototype. Right: Initial digital terrain model.
</div>

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/QGIS.jpeg" title="Early QGIS mapping" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/creality print.jpeg" title="Early Creality Print preparation" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Left: Early geographic mapping in QGIS. Right: Preparing the initial terrain model in Creality Print.
</div>
