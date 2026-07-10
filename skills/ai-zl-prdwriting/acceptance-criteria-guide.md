# Acceptance Criteria Guide

## Purpose

Acceptance criteria exist to make a PRD executable and testable.

If acceptance cannot be checked, the requirement is not yet clear enough.

## Good Acceptance Criteria

Good criteria are:

- observable
- testable
- bounded
- specific

## Bad Examples

- the page feels smoother
- the process is more convenient
- users can easily understand it

These are not testable.

## Good Examples

- when the user enters a valid amount and taps the primary CTA, the flow moves to the payment method step
- when the amount is below the minimum threshold, the CTA remains disabled and an error hint is displayed
- when no available payment method exists, the page shows an empty-state message and does not allow submission

## Writing Pattern

Use one of these patterns:

### Pattern A

- when the user does `X`, the system does `Y`

### Pattern B

- given `X`, when `Y`, then `Z`

### Pattern C

- the page must display `X` under `Y` condition

## Coverage Checklist

Acceptance should usually cover:

- happy path
- invalid input
- unavailable data
- state transition
- permission or eligibility rule

## Page Requirement Reminder

For page-related PRDs, acceptance should include:

- page entry condition
- required visible modules
- CTA behavior
- error or empty state handling
