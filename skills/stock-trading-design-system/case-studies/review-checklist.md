# Review Checklist

Use this when reviewing new Figma output, PM prototype requests, or implementation prompts.

## Foundations

- Does the screen stay on the approved `375px` mobile grid?
- Are margins and content widths aligned with the current system?
- Are radius and stroke values from the existing token scale?

## Components

- Are buttons, tabs, navigation, stock rows, and payment controls real components?
- Are all required states present where needed?
- Are icon and logo slots still local component instances?

## Semantics

- Is green used only for positive, selected, success, or key active states?
- Is red used only for decline, error, or risk?
- Is typography named and used by role rather than ad hoc labels?

## Page Logic

- Does the page match one of the approved shells?
- Is the primary task obvious in the first viewport?
- Is there only one primary CTA per task section?

## Collaboration

- Can PM, design, and engineering read the output without guessing terminology?
- Are the component property names still stable?
- If something changed, was `CHANGELOG.md` updated?
