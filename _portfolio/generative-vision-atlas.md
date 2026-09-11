---
title: "Generative Vision Atlas"
category: research
order: 1
excerpt: "A living, structured review of modern generative vision — 204 papers organized into 35 research lines, each defined by one explicit bet about where generation should happen.<br/><img src='/images/genai-atlas.png'>"
collection: portfolio
---

[**▶ Open the atlas**](https://saharr1372.github.io/genai-atlas/) &nbsp;·&nbsp; [**Source on GitHub**](https://github.com/SaharR1372/genai-atlas)

A living literature review of modern generative vision, built around a single
organizing question: **where should generation happen?** In a compression code,
inside a foundation model's features, in discrete tokens, or in raw pixels?

Image generation has largely settled its arguments about objectives and
architectures. Where generation should *happen* is still contested, so the atlas
is organized around that disagreement rather than around a taxonomy of methods.

![Generative Vision Atlas](/images/genai-atlas.png)

## How it is organized

204 papers sit inside **35 research lines**, each defined by one explicit bet.
A line states what its group is claiming, what that claim costs them, and which
lines disagree. Six design questions structure the whole atlas — what space you
generate in, what happens at sampling time, how understanding and generation are
arranged, and so on — and lines answering the same question compete directly.

Medical imaging is kept deliberately separate: 27 papers across 5 lines. Clinical
imaging answers the same design question differently, and answers to a different
evidence bar — not a better distribution distance, but whether a diagnostic model
improves and whether a radiologist is fooled.

## What it does that a paper list does not

**It refuses to publish a leaderboard.** One paper reports the same model at
FID 1.65, 1.49, 1.14 and 1.06 under four guidance methods — a swing larger than
most architectural claims. Every one of the 46 benchmark numbers here carries the
guidance method, training budget and model size that produced it, so the reader
can see when a comparison is not actually a comparison.

**It tracks what is unsolved.** 11 open problems, each linked to the papers
attacking it and to the research lines that carry it as a known weakness. Where a
line is weak, its own page says so.

**It keeps itself current.** A pipeline sweeps arXiv and Hugging Face every three
days, filters for genuine relevance, and proposes candidates for review. Nothing
is added automatically, and nothing is claimed without a fetched source —
203 of the 204 entries are verified against arXiv.

## Reproducible evidence

Four notebooks with real outputs from an A100: what each latent discards, RAE
measured against the VAE it replaces, how editing methods actually differ, and
why guidance breaks benchmark comparisons.
