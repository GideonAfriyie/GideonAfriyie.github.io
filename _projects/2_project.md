
---
layout: page
title: Extreme Value Theory and Prime Gaps
description: A 15-month research journey from Cramér's conjecture to journal publication
img: assets/img/prime-pattern.jpeg
importance: 2
category: work
related_publications: true
---

*How a simple question about Cramér's conjecture became a 15-month journey through peer review, 50 million prime gaps, and my first journal publication.*

## How It Started

This project began with a simple question that I couldn't stop thinking about.

About a year and a few months ago, I came across an article explaining how **Extreme Value Theory (EVT)** is used to study the tails of probability distributions — the rare, extreme events behind things like catastrophic floods, financial crashes, and other unlikely phenomena.

My first thought was:

> Could these same statistical ideas tell us something about prime numbers?

More specifically, I became fascinated by **Cramér's conjecture** after learning about it in my Abstract Math course. It is one of the most well-known conjectures about how large the gaps between consecutive prime numbers can become.

While the conjecture has traditionally been studied from a theoretical number theory perspective, I wondered whether the data itself could provide statistical evidence supporting its predictions.

I wasn't entirely sure how to approach the problem at first, so I started reading papers, experimenting with ideas, asking questions, and reaching out to professors whenever I got stuck.

Every answer seemed to raise another question, and before I knew it, a small curiosity had grown into a full research project.

## The First Submission

My first version of the paper analyzed **1 million consecutive prime gaps** using Generalized Extreme Value (GEV) distributions.

At that scale, the data appeared to follow a **Fréchet distribution**, suggesting heavy-tailed behavior.

Encouraged by the results, I submitted the manuscript to *Statistics & Probability Letters*.

The reviews came back with a clear message: the statistical analysis was interesting, but the mathematical justification needed to be much stronger.

The reviewers raised concerns about the justification of EVT assumptions and the interpretation of the results.

At that point, I had two options.

I could convince myself that the reviewers simply didn't understand the work, or I could treat their comments as genuine weaknesses and use the feedback to improve it.

I chose the second option.

## Revisiting the Mathematics

Over the next **4–5 months**, I worked through the reviewer comments one by one.

The biggest change was expanding the dataset from **1 million to 50 million prime gaps**.

Interestingly, the conclusions changed.

With the larger dataset, the fitted extreme-value distribution shifted from **Fréchet toward Gumbel**, bringing the empirical results into closer agreement with predictions from classical number theory.

I also revisited one of the central criticisms of the paper.

Rather than relying primarily on an Augmented Dickey-Fuller (ADF) test, I used an **Autocorrelation Function (ACF)** analysis to examine serial dependence in the prime-gap sequence.

### Extreme Value Analysis

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/prime-gap-evt (2).png" title="Extreme value analysis of 50 million prime gaps" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Figure 1. Distribution of normalized prime gaps, block maxima, and a Generalized Extreme Value fit using 50 million primes.
</div>

### Autocorrelation Analysis

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/acf_validation_50m (2).png" title="Autocorrelation analysis of prime gaps" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Figure 2. Autocorrelation analysis of prime gaps, examining serial dependence across different lags.
</div>

## What I Learned

In total, this project took approximately **15 months**, from the initial idea to journal acceptance.

Along the way, the paper was rejected by journals that considered it outside their scope, challenged by reviewers who pushed me to justify my assumptions, and revised until the work became stronger.

Looking back, I'm grateful for those setbacks because they forced me to think more carefully about the mathematics.

More importantly, this project changed how I think about research.

I used to believe research was about having brilliant ideas from the beginning.

Now I think it's almost the opposite.

Research is about asking questions you're genuinely curious about, being willing to admit when your first approach is incomplete, and treating criticism as an opportunity to learn rather than a reason to stop.

This paper began with a question that probably sounded naive:

> Could Extreme Value Theory tell us something about prime numbers?

Months later, that curiosity became my first peer-reviewed journal publication.

## Publication

The resulting research was published in *Statistics & Probability Letters*.

See my [Publications]({{ '/publications/' | relative_url }}) page for the paper and its bibliographic details.
