---
title: "Anatomy Learning Platform"
excerpt: "An evidence-based web app for learning human anatomy, movement, and personal-training fundamentals — 16 body regions, 51 muscles, 49 exercises, every claim cited.<br/><img src='/images/anatomy-platform.png'>"
collection: portfolio
---

[**▶ Browse the live demo**](https://saharr1372.github.io/AnatomyKnowledge/) &nbsp;·&nbsp; [**Source on GitHub**](https://github.com/SaharR1372/AnatomyKnowledge)

A full-stack web application for learning human anatomy, movement, and
personal-training fundamentals — built around the idea that a learner should be
told *why*, and be able to check the source for every claim.

![Anatomy Learning Platform](/images/anatomy-platform.png)

## What it covers

All 16 body regions at full depth — 51 muscles, 23 joints, 40 movements,
49 exercises, 38 lessons, and 99 quiz questions. Each muscle page gives its
origin, insertion, actions, innervation, plane of movement, what it does in
daily life versus in the gym, and the muscles it is commonly confused with.
Exercises are never reduced to a single muscle: each one lists its primary,
secondary, and stabilising movers.

## Design decisions worth noting

**Citations are first-class.** Sources are a modelled entity, not a footnote.
Any claim can be attached to a source through a polymorphic citation table, and
sources carry a reliability tier and a last-checked date, so the interface can
show *how well supported* a statement is rather than presenting everything with
equal confidence. Where authoritative sources disagree, the disagreement is
displayed instead of quietly resolved.

**Quiz grading is server-side.** Correct options are never sent to the browser.
Answers are graded against the stored options, and each result feeds a
spaced-repetition schedule so missed questions resurface sooner.

**Safety is explicit.** The content is labelled by review status and is clear
about a trainer's scope of practice and when to refer a learner to a healthcare
professional. No proprietary certification questions are used.

## Built with

Next.js 15 (App Router) · TypeScript · Tailwind CSS · Prisma · SQLite → PostgreSQL ·
Auth.js · Vitest. All anatomical diagrams are original SVGs released under CC0.

## About the demo

The live link above is a static export hosted on GitHub Pages, so it is
read-only: every lesson, muscle, exercise, and source is browsable, and the
flashcards and exercise filters work in the browser. Accounts, saved progress,
private notes, and the quiz engine need the server-rendered app, which runs
locally in about two minutes — see the
[README](https://github.com/SaharR1372/AnatomyKnowledge#readme).
