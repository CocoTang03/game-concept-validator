# Game Concept Validator

English | [简体中文](./README.zh-CN.md)

An AI skill for evaluating, comparing, and validating game concepts before prototype production.

It is designed for situations where you have multiple game ideas but have not yet decided which one deserves your time, budget, and development effort.

Instead of expanding every idea into a full GDD, this skill helps answer a more important question:

> Which game concept is most worth pursuing right now, and why?

---

# Use Cases

This skill is useful when you:

* Have multiple game ideas and do not know which one to build first
* Want to compare several projects using the same criteria
* Need to identify which concepts are over-scoped
* Want to know whether a similar game has already been made
* Need to understand how differentiated an idea really is
* Want to identify the true core of a game concept
* Need to test whether a Core Loop is coherent before production
* Want to expose hidden assumptions and major risks
* Need to determine whether a refinement actually improved an idea
* Want a structured design review before entering Prototype development

---

# Not Intended For

This skill is not primarily designed for:

* Writing a full GDD
* Gameplay implementation
* Unity or Unreal programming
* UI implementation
* Bug fixing
* Game balancing
* Production scheduling
* Live Playtesting
* QA
* Full production planning

Its primary responsibility is:

> **Deciding what is worth building next.**

Not:

> **Building the game itself.**

---

# Workflow

The skill uses a **Progressive Filtering** workflow.

It does not deeply analyze every idea from the beginning. Instead, it first filters the portfolio, then progressively increases analysis depth for stronger candidates.

```text
Game Idea Portfolio
        ↓
Phase 1 — Portfolio Triage
        ↓
Prior Art / Comparable Games Research
        ↓
T0 — Raw Idea Score
        ↓
Phase 2 — Concept Architecture
        ↓
T1 — Structured Concept Score
        ↓
Phase 3 — Adversarial Refinement
        ↓
T2 — Refined Concept Score
        ↓
Top Candidates
        ↓
Phase 4 — Schell Game Design Review
        ↓
Final Recommendation
```

---

# Phase 1 — Portfolio Triage

All game ideas are first normalized into the same evaluation format.

This prevents a heavily documented project from automatically appearing stronger than a newer one-line idea.

The skill compares the underlying concepts rather than the amount of documentation already written.

The main evaluation dimensions include:

* Player Hook
* Differentiation
* Core Experience Strength
* Prototype Speed
* Scope Control
* Production Feasibility
* Content Burden
* Market Readability
* Team / Personal Fit
* Validation Cost
* Competitive Whitespace

The purpose of this stage is not to design every game in detail.

It is to answer:

> **Which ideas deserve deeper analysis?**

---

# Phase 2 — Prior Art Research

Promising concepts are researched against existing games and related implementations.

The skill does not only ask:

> Has this exact game already been made?

It also checks:

* Exact Mechanic Match
* Same Player Promise
* Same Hook
* Adjacent Implementations
* Comparable Games
* Experimental Games
* Game Jam Projects
* Commercial and Audience References

For example, an idea may be described as:

> The player understands an invisible world entirely through sound.

Even if no game uses the exact same controls, similar experiences may already exist through:

* Echolocation
* Spatial Audio
* Audio Navigation
* Dark Environment Exploration
* Sound-Based Puzzle Systems

These still count as relevant Prior Art.

---

# Prior Art Analysis

For close references, the skill examines:

* What is similar
* What has already been solved
* What players appear to value
* What common complaints exist
* What limitations are visible
* What your concept does differently
* Whether meaningful Competitive Whitespace remains

The most important question is:

> **Why should a player choose this version instead of the closest existing alternative?**

If there is no clear answer, differentiation is treated as a serious risk.

---

# Phase 3 — Concept Architecture

Shortlisted concepts are then structured more deeply.

The skill analyzes:

* Player Promise
* Player Fantasy
* Design Nucleus
* Core Loop
* Design Pillars
* Core vs Supporting Systems
* Minimum Coherent Version
* Scope Boundary
* Production Burden

The central question is:

> **What is the one thing that makes this game fundamentally itself?**

---

# Player Promise

The skill distinguishes between what the player does and what the player experiences.

For example:

Weak:

> The player listens, moves, and solves puzzles.

Stronger:

> The player learns to reconstruct an unseen world entirely through sound.

The second version describes the intended experience rather than a list of mechanics.

---

# Design Nucleus

The Design Nucleus is the smallest interaction-and-experience combination that still makes the concept meaningfully distinct.

The skill asks:

> If most of the game were removed, what would still need to remain for the game to be itself?

A project that only works when it includes:

* Cooking
* Riding
* Selling
* Exploration
* Collecting
* Narrative
* 2D content
* 3D content

may carry a much higher Scope Risk than a concept with one strong, reusable nucleus.

---

# Minimum Coherent Version

The skill also evaluates the smallest version of the game that can still deliver its Player Promise.

It considers:

* Number of mechanics
* Number of levels
* Number of environments
* Number of characters
* Art requirements
* Narrative requirements
* Audio requirements
* Custom tooling requirements

This stage is especially important for identifying concepts whose minimum viable form is already too large.

---

# Phase 4 — Adversarial Refinement

This phase actively tries to disprove the concept.

The purpose is not to add more features.

Instead, it looks for:

* Critical Assumptions
* Hidden Blind Spots
* Failure Modes
* Retention Risk
* Scope Risk
* Technical Risk
* Production Risk
* Market Communication Risk
* Accessibility Risk
* Team Fit Risk
* Kill Criteria
* Pivot Opportunities

The main question is:

> **If this game fails, what is the most plausible reason?**

---

# Riskiest Assumption

Each concept should have one dominant assumption that could seriously damage the project if proven false.

Examples:

> Players can reliably understand spatial relationships through the intended audio language.

> The main interaction remains satisfying after repeated use.

> The game's hook can be communicated clearly in a short trailer.

> The required content volume is realistic for the current team.

---

# Kill Criteria

The skill encourages observable Kill Criteria.

Weak:

> Stop if players do not like it.

Stronger:

> If first-time players consistently fail to understand spatial direction without additional visual support, the current audio interaction model should be redesigned before further production.

This helps prevent Sunk Cost from becoming the main reason to continue a weak direction.

---

# Refinement vs Pivot

After refinement, changes are classified into two types.

## Minor Refinement

The concept remains substantially the same if it keeps the same:

* Player Promise
* Design Nucleus
* Core Loop

Examples:

* Removing unnecessary systems
* Reducing Scope
* Improving feedback
* Clarifying controls
* Reworking supporting features

In this case, the same Concept Version is re-scored.

---

## Major Pivot

A new Concept Version is created if refinement materially changes:

* Player Promise
* Design Nucleus
* Primary Core Loop
* Player Fantasy
* Main Interaction Model

Example:

```text
Sound Puzzle v1
Audio-only exploration game

        ↓ PIVOT

Sound Puzzle v2
Spatial-audio stealth puzzle with minimal visual feedback
```

The second version should not simply replace the first score.

It is treated as a new Concept Version with its own evaluation history.

---

# Versioned Scoring

The skill uses:

> **Stable Rubric + Versioned, Evidence-Sensitive Scores**

The scoring criteria and their definitions remain fixed.

However, scores may change as more evidence becomes available.

The skill preserves three main scoring stages:

```text
T0 — Raw Idea Score

T1 — Structured Concept Score

T2 — Refined Concept Score
```

Example:

```text
Sound Puzzle

T0: 7.6
T1: 8.2
T2: 7.8
```

A lower later score is not necessarily a bad result.

It may mean that deeper analysis revealed:

* Closer Prior Art
* Higher Retention Risk
* Larger Scope than expected
* Accessibility problems
* Higher production burden
* Weak Market Readability

Finding these problems early is part of successful validation.

---

# Why the Rubric Stays Stable

If:

> Scope Control = 8

then it should always mean:

> The smallest coherent version of the concept is relatively easy to keep bounded.

The definition must not change just because the evaluator prefers a particular idea.

Therefore:

```text
Rubric Definition = Stable

Evidence = May Change

Concept = May Change

Scores = Recalculated

Ranking = May Change
```

---

# Phase 5 — Schell Game Design Review

Only the strongest candidates receive a deeper Schell-style Game Design Review.

This phase is qualitative rather than another weighted score.

It evaluates:

* Intended Player Experience
* Player Fantasy
* Mechanics
* Story
* Aesthetics
* Technology
* Player Motivation
* Core Loop Sustainability
* Interest Curve
* Meaningful Choice
* Feedback
* Skill vs Chance
* Theme–Mechanic Coherence
* Accessibility

The main question becomes:

> **Even if this idea is feasible and differentiated, does it actually form a coherent game experience?**

---

# Four Core Elements

The review examines:

```text
Mechanics
Story
Aesthetics
Technology
```

The purpose is not to judge them independently.

The important question is:

> **Are all four elements supporting the same Player Promise?**

For example, if a game promises that the player must understand the world through sound, but then relies heavily on clear visual navigation markers, its mechanics and aesthetics may be working against each other.

---

# Core Loop Sustainability

The skill stress-tests the Core Loop across time:

```text
First 30 seconds
↓
5 minutes
↓
20 minutes
↓
Late game
```

It asks:

* What changes?
* What deepens?
* What becomes repetitive?
* Where does mastery emerge?
* Where does novelty decay?

A mechanic can be highly original and still fail to sustain a complete game.

---

# Player Motivation

The review also asks why the player continues after the novelty of the hook fades.

Common motivations include:

* Curiosity
* Mastery
* Discovery
* Narrative
* Collection
* Expression
* Challenge
* Optimization

If the only motivation is:

> This mechanic is unusual the first time.

then the concept may have significant Retention Risk.

---

# Final Status

Each concept receives one final status.

## PROCEED

The concept is coherent, reasonably scoped, sufficiently differentiated, and has no dominant unresolved conceptual flaw.

This means it is worth moving into the next validation or Prototype stage.

It does not mean full production is approved.

---

## VALIDATE FIRST

The concept has meaningful upside, but one major Unverified Assumption dominates the risk.

That assumption should be tested before further investment.

---

## PIVOT

The underlying fantasy or theme has value, but the current Design Nucleus, Core Loop, Scope, or positioning needs to change.

The evaluation should state:

* What should be preserved
* What should change
* Why the Pivot is necessary

---

## PARK

The concept may be good, but it does not currently fit the available:

* Time
* Team
* Scope
* Production Capacity
* Strategic Priorities

The analysis should record what future condition would justify revisiting it.

---

## KILL

The current Concept Version may be killed if:

* No strong Player Promise remains
* Differentiation is weak
* Major risks are expensive to validate
* Scope is too large relative to potential upside
* Another portfolio idea dominates it
* Refinement repeatedly adds complexity without strengthening the Design Nucleus

A KILL decision applies to the current concept version, not necessarily the underlying theme forever.

---

# Final Output

The final report can include:

## Executive Selection

* Best Overall Candidate
* Best Cheap Validation Candidate
* Highest Creative Upside
* Highest Probability of Shipping
* Best Short Demo Candidate
* Most Dangerous Scope Trap

---

## Portfolio Ranking

Example:

```text
1. Project A
2. Project B
3. Project C
```

with T0, T1, and T2 score history preserved.

---

## Prior Art Summary

For finalists:

* Closest Games
* Mechanic Similarity
* Player Promise Similarity
* Competitive Whitespace
* Prior Art Risk
* Why This Version?

---

## Concept Architecture

For finalists:

* Player Promise
* Design Nucleus
* Core Loop
* Design Pillars
* Minimum Coherent Version
* Primary Scope Risk

---

## Adversarial Review

For finalists:

* Riskiest Assumption
* Biggest Blind Spot
* Most Likely Failure Mode
* Kill Criterion
* Pivot Option

---

## Schell Review

For finalists:

* Intended Experience
* Four Elements Coherence
* Motivation Strength
* Core Loop Sustainability
* Interest Curve Risk
* Main Design Contradiction
* Overall Design Confidence

---

# Project Structure

```text
game-concept-validator/
│
├── SKILL.md
│
└── references/
    ├── portfolio-rubric.md
    ├── prior-art-framework.md
    ├── concept-architecture.md
    ├── adversarial-review.md
    └── schell-lenses.md
```

`SKILL.md` defines the overall workflow.

The `references/` directory contains the detailed frameworks used during each evaluation phase.

---

# Example Usage

```text
Use game-concept-validator.

Scan all game project folders in this workspace.

Treat them as a Game Idea Portfolio.

Compare all projects using the same rubric.

Research Prior Art for serious candidates.

Run:

Portfolio Triage
→ Concept Architecture
→ Adversarial Refinement
→ Schell Game Design Review

Keep T0 / T1 / T2 scores separately.

If refinement changes the Design Nucleus or Player Promise,
create a new Concept Version.

Stop before Prototype implementation.
```

---

# Design Philosophy

This skill is not trying to find:

> The objectively best game idea.

It is trying to find:

> **The concept with the strongest current relationship between Player Promise, differentiation, Competitive Whitespace, Scope, production feasibility, uncertainty, and strategic value.**

A useful evaluation should be able to answer:

1. Which idea deserves attention now?
2. Why this idea instead of the alternatives?
3. What existing games are closest to it?
4. Why should a player choose this version?
5. What assumption could kill the concept?
6. Did deeper analysis make the idea stronger or weaker?
7. Was the change a refinement or a true Pivot?
8. What evidence could reverse the ranking?
9. Which ideas should deliberately not be worked on right now?

If these questions cannot be answered, the concept is not ready to advance.

---

# License

This project is released under the MIT License.

See the `LICENSE` file for details.
