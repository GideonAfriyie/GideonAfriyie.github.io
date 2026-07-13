---
layout: page
title: Extreme Value Theory in Prime Gaps
description: How a curiosity about Cramér's conjecture turned into a 14-month journey of brutal peer reviews, 50 million data points, and my first journal publication.
img: assets/img/evt_50m_final_results.png
importance: 1
category: work
related_publications: true
---

This project started out of pure, stubborn curiosity. 

About a year and a half ago, I read an article explaining how Extreme Value Theory (EVT) is used to model the "tails" of distributions—basically, predicting rare, extreme events like massive floods or stock market crashes. I immediately wondered: *Could we use this to study prime numbers?* 

Specifically, I wanted to look at **Cramér's conjecture**, which predicts how large the gaps between consecutive prime numbers can get. Other researchers had studied this from a purely theoretical math perspective, but I wanted to see if the statistical data actually backed it up. 

I didn't really know where to start, so I just started asking questions. When I got stuck, I reached out to my professors for guidance, took their feedback, and kept pushing forward.

---

### The First Attempt & The Brutal Review

In my first draft of the paper, I used a dataset of **1 million prime gaps**. At that scale, the data showed what's called *Fréchet* behavior (a type of heavy-tailed distribution limit). I submitted it to the *Journal of Statistics & Probability Letters* (Elsevier).

The reviewers did not hold back. They were brutal, but incredibly helpful. One of the reviewers wrote:

> "The manuscript presents an interesting statistical approach to studying prime gaps... While the statistical analysis is carefully executed, the manuscript raises significant conceptual and methodological concerns, particularly the justification of EVT assumptions and the interpretation of results, [which] must be addressed before publication."

I had two choices: get discouraged and quit, or go through their feedback line-by-line. I chose the second option. 

---

### Overcoming the Math Challenges & The Data Plots

To address the reviewers' critiques, I had to completely restructure my approach. I scaled up the code and expanded the dataset from 1 million to **50 million prime gaps**. 

When I ran the new data, the statistical behavior shifted beautifully from *Fréchet* to **Gumbel** behavior, aligning perfectly with classical number theory predictions. Furthermore, to prove why probability theory applies to deterministic primes, I shifted from an Augmented Dickey-Fuller (ADF) test to an **Autocorrelation Function (ACF)** analysis on normalized gaps:

$$\frac{g_n}{\log p_n}$$

The ACF perfectly demonstrated that prime gaps behave statistically as if they are independent, identically distributed random variables.

<div class="row justify-content-sm-center mt-4">
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/evt_50m_final_results.png" title="Distribution Shift" class="img-fluid rounded z-depth-1" %}
    <div class="caption">Figure 1: The shift from Fréchet to Gumbel distribution as data scaled to 50M gaps.</div>
  </div>
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/acf_validation_50m.png" title="ACF Analysis" class="img-fluid rounded z-depth-1" %}
    <div class="caption">Figure 2: ACF of normalized prime gaps demonstrating statistical independence.</div>
  </div>
</div>

---

### Rejections, Persistence, and Acceptance

It took 14 months of hard work, learning from initial rejections at other journals that thought the paper was "out of scope," and grinding through the intense revision process. But in the end, the changes made the paper incredibly robust, and it was officially accepted for publication!

I learned so much from this process. It taught me that research isn't about being the smartest person in the room from day one. It's about asking "dumb" questions, trying things step-by-step, and taking brutal feedback as a roadmap to improve rather than a reason to stop.

Funny enough, after the paper went through, the journal actually invited me to act as a **peer reviewer** for another manuscript on extreme value distributions. Since it was my first time and I was swamped with other work, I had to decline—but once I gain a bit more experience and clear my schedule, I can’t wait to give back and do the service one day!
