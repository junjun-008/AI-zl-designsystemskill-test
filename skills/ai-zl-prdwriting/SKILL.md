---
name: ai-zl-prdwriting
description: Use this AI-zl project skill when writing or reviewing PRDs, feature requirement docs, page requirement docs, product briefs, user stories, scope definitions, acceptance criteria, or PM handoff documents that need to be professional, structured, and execution-ready.
metadata:
  version: v1.0
  project: AI-zl
  short-description: AI-zl project PRD writing skill
---

# AI-zl PRD Writing Skill

Use this skill when the user wants a professional PRD instead of an informal feature note.

This skill is optimized for:

- new feature PRDs
- new page PRDs
- flow change PRDs
- requirement clarification
- PM-to-design handoff
- PM-to-engineering handoff
- requirement review and completion

## Output Standard

Every PRD produced with this skill should be:

- clear enough for PM, design, and engineering to read without translation
- concrete enough to execute
- scoped enough to avoid uncontrolled interpretation
- structured enough to review quickly

## Trigger Phrases

Use this skill when the request includes ideas like:

- write a PRD
- product requirements document
- 需求文档
- 产品需求文档
- 功能需求
- 页面需求
- 用户故事
- 验收标准
- 需求整理
- 帮我把需求写专业一点

## Read Order

### Always Read

1. `SKILL.md`
2. `prd-template.md`
3. `review-checklist.md`

### Read When Needed

- terminology alignment: `GLOSSARY.md`
- acceptance criteria writing: `acceptance-criteria-guide.md`
- governance updates: `CHANGELOG.md`

### Joint Usage Rule

If the requirement involves UI, Figma pages, screens, components, or prototypes, and the project also has `stock-trading-design-system`, use both skills together.

Use:

- `ai-zl-prdwriting` for requirement structure, scope, and acceptance
- `stock-trading-design-system` for page rules, components, tokens, and design constraints

## Required PRD Structure

Unless the user explicitly asks for a shorter format, every PRD should include:

1. Background
2. Goal
3. Problem Statement
4. Target Users
5. User Scenario
6. Scope
7. Functional Requirements
8. Interaction Or Page Notes
9. Edge Cases
10. Acceptance Criteria
11. Out Of Scope
12. Risks And Open Questions

## Hard Rules

### Always

1. Always state what business or user problem is being solved.
2. Always distinguish `in scope` from `out of scope`.
3. Always separate objective facts from assumptions.
4. Always write requirements in a way that design and engineering can act on.
5. Always include acceptance criteria for every meaningful feature block.
6. Always identify open questions instead of hiding ambiguity in vague wording.
7. Always define the target user or target scenario.
8. Always make the primary user task obvious.
9. Always describe changes against the current product state when that context exists.
10. Always keep wording short, direct, and testable.

### Never

1. Never write a PRD that is only background plus a list of features.
2. Never use vague phrases like `optimize experience`, `improve interaction`, or `make it better` without defining what changes.
3. Never mix requirement statements with design speculation unless marked as recommendation.
4. Never leave page-level requirements without page goals or acceptance criteria.
5. Never treat a design reference as a substitute for written requirements.
6. Never hide unresolved dependencies; move them into `Risks And Open Questions`.

## Writing Method

### Step 1: Normalize The Request

Clarify:

- what is changing
- why it matters
- who is affected
- whether this is a new feature, a new page, or an optimization

### Step 2: Define Scope

Break the request into:

- required
- optional
- explicitly excluded

### Step 3: Write Requirement Blocks

Each block should contain:

- user intent
- system behavior
- visible output
- failure or exception handling

### Step 4: Add Acceptance

Use observable and testable language.

Bad:

- user experience is smooth

Good:

- after the user submits a valid amount, the page advances to payment method selection within the same flow

### Step 5: Add Open Questions

If something is not defined, do not fake certainty. Record it.

## Default Output Style

- use concise Chinese
- use section headers
- prefer short paragraphs and flat bullets
- avoid marketing language
- avoid long narrative prose

## PRD Quality Bar

A PRD is not complete unless:

- the problem is clear
- the main flow is clear
- the boundaries are clear
- acceptance is testable
- unresolved issues are visible

## If The Request Is Page-Oriented

Also include:

- page objective
- primary user task
- required modules
- entry and exit points
- page states if relevant

When the design-system skill is available, align module names to the real component and page system.

## If The Request Is Optimization-Oriented

Also include:

- current issue
- expected change
- non-goals
- measurable or observable difference after release

## Final Self Check

Before delivering the PRD, verify:

- Is the goal explicit?
- Is the problem statement concrete?
- Is the scope bounded?
- Can design act on it?
- Can engineering implement it?
- Can QA validate it?
- Are open questions isolated instead of hidden?
