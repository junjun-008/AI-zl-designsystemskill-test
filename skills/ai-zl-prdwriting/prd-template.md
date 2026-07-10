# PRD Template

Use this as the default template unless the user requests a different format.

## 1. Background

- current product context
- what triggered this request
- why now

## 2. Goal

- the business or user outcome this requirement is intended to achieve
- write in one or two sentences only

## 3. Problem Statement

- what is currently missing, broken, unclear, or inefficient
- describe the current gap, not the future solution

## 4. Target Users

- primary user group
- optional secondary user group
- note if this is for all users or a subset

## 5. User Scenario

Describe the real usage context:

- when the user enters
- what the user wants to do
- what the user expects to happen

## 6. Scope

### In Scope

- itemized requirement blocks

### Out Of Scope

- explicitly excluded content

## 7. Functional Requirements

Write by requirement block.

### Requirement Block Name

- user action
- system response
- displayed content
- validation or state handling

## 8. Interaction Or Page Notes

Use when the requirement affects a page, flow, or UX pattern.

Include only what is necessary:

- page objective
- page entry
- page exit
- required modules
- critical states

## 9. Edge Cases

List non-happy-path situations:

- empty state
- invalid input
- unavailable data
- permission or account limits
- repeated operations

## 10. Acceptance Criteria

Write as testable bullets.

Example style:

- Given `X`, when the user does `Y`, the system shows `Z`
- After the user completes `A`, the system must `B`

## 11. Out Of Scope

Repeat if needed to protect the boundary. This section is mandatory when the request is likely to expand.

## 12. Risks And Open Questions

- unresolved dependency
- unclear policy
- pending metric decision
- pending design decision

## 13. Suggested Next Step

Optional. Use only when helpful:

- design output
- technical assessment
- metric definition
- policy confirmation
