---
layout: page
title: Extreme Value Theory in Prime Gaps
description: How a simple question about Cramér's conjecture became a 15-month journey through peer review, 50 million prime gaps, and my first journal publication.
img: assets/img/evt_50m_final_results.png
importance: 1
category: work
related_publications: true
---

This project began with a simple question that I couldn't stop thinking about.

About a year and few months ago, I came across an article explaining how **Extreme Value Theory (EVT)** is used to study the tails of probability distributions - the rare, extreme events behind things like catastrophic floods, financial crashes, and other unlikely phenomena. My first thought was:

> *Could these same statistical ideas tell us something about prime numbers?*

More specifically, I became fascinated by **Cramér's conjecture** after learning about it in my Abstract Math course, one of the most well-known conjectures about how large the gaps between consecutive prime numbers can become. While the conjecture has traditionally been studied from a theoretical number theory perspective, I wondered whether the data itself could provide statistical evidence supporting its predictions.

I wasn't entirely sure how to approach the problem at first, so I did what I've always done whenever I get curious: I started reading papers, experimenting with ideas, asking lots of questions, and reaching out to professors whenever I got stuck. Every answer seemed to raise another question, and before I knew it, a small curiosity had grown into a full research project.

---

### The First Submission

My first version of the paper analyzed **1 million consecutive prime gaps** using Generalized Extreme Value (GEV) distributions. At that scale, the data appeared to follow a **Fréchet** distribution, suggesting heavy-tailed behavior.

Encouraged by the results, I submitted the manuscript to *Statistics & Probability Letters*.

The reviews came back with a clear message: the statistical analysis was interesting, but the mathematical justification needed to be much stronger.

Reviewer summarized it well:

> "The manuscript presents an interesting statistical approach to studying prime gaps and could potentially contribute to the intersection of statistics and number theory... While the statistical analysis is carefully executed, the manuscript raises significant conceptual and methodological concerns, particularly the justification of EVT assumptions and the interpretation of results, that must be addressed before publication."

At that point I had two options.

I could convince myself that the reviewers simply didn't understand the work, or I could assume they were pointing out genuine weaknesses and use their feedback to improve it.

I chose the second option.

---

### Revisiting the Mathematics

Over four months, I worked through every reviewer comment one by one.

The biggest change was expanding the dataset from **1 million** to **50 million prime gaps**, which required rewriting much of the pipeline and repeating the statistical analysis from scratch.

Interestingly, the conclusions changed.

With the larger dataset, the limiting distribution shifted naturally from **Fréchet** to **Gumbel**, bringing the empirical results into much closer agreement with predictions from classical number theory.

I also revisited one of the central criticisms of the paper.

Rather than relying primarily on an Augmented Dickey-Fuller (ADF) test, I introduced an **Autocorrelation Function (ACF)** analysis of the normalized prime gaps,

$$
\frac{g_n}{\log p_n},
$$

to demonstrate that the sequence behaves statistically much like independent, identically distributed random variables—the key assumption underlying the Extreme Value Theory framework.

<div class="row justify-content-sm-center mt-4">
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/evt_50m_final_results.png" title="Distribution Shift" class="img-fluid rounded z-depth-1" %}
    <div class="caption">Figure 1. As the dataset increased to 50 million prime gaps, the limiting distribution shifted from Fréchet toward Gumbel, aligning with classical theoretical predictions.</div>
  </div>
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/acf_validation_50m.png" title="ACF Analysis" class="img-fluid rounded z-depth-1" %}
    <div class="caption">Figure 2. Autocorrelation analysis of normalized prime gaps showing the weak dependence required for applying Extreme Value Theory.</div>
  </div>
</div>

---

### What I Learned

In summary, this project took about **15 months** from the initial idea to journal acceptance.

Along the way, the paper was rejected by journals that considered it outside their scope, challenged by reviewers who pushed me to justify every assumption, and revised until the work became strong.

Looking back, I'm grateful for every one of those setbacks because it forced the work to become stronger.

More importantly, this project completely changed how I think about research.

I used to believe research was about having brilliant ideas from the beginning.

Now I think it's almost the opposite.

Research is about asking questions you're genuinely curious about, being willing to admit when your first approach is incomplete, and treating criticism as an opportunity to learn rather than a reason to stop.

This paper began with a question that probably sounded naive:

> *Could Extreme Value Theory tell us something about prime numbers?*

Months later, that curiosity became my first peer-reviewed journal publication.

Perhaps the most unexpected moment came when the editorial board invited me to serve as a peer reviewer for a manuscript on extreme value distributions. Since I was balancing work and several commitments, I had to decline the invitation, but it meant a great deal to me. One day, when I have gained more experience, I hope to contribute to the research community in the same way others helped me throughout this journey.
