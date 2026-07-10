# Common Breakages

This file records the recurring failure patterns already seen in this Figma file and the rule that prevents each one.

## 1. Core Buttons Not Componentized

### Problem

Visual button frames were used in screens without a complete reusable component model.

### Risk

- inconsistent states
- harder updates
- multiple button styles drift apart

### Rule

Buttons are always components with stable size, state, and icon properties.

## 2. Icon Instances Became Mismatched

### Problem

Icons inside components were replaced or detached incorrectly, leading to wrong icons on page instances.

### Risk

- navigation confusion
- incorrect visual meaning
- brittle screen maintenance

### Rule

Use instance-swap icon slots. Do not paste ad hoc icons into component instances.

## 3. Stock Logos Disappeared

### Problem

Stock list rows lost their stock-specific logos and fell back to generic shapes.

### Risk

- information loss
- lower scanning efficiency
- weaker product realism

### Rule

Stock rows and market cards must preserve local logo components. Logo integrity is part of the component contract.

## 4. Handbook Sections Overflowed

### Problem

Documentation frames in `Design System / Handbook` overflowed their containers and became hard to read.

### Risk

- poor onboarding quality
- documentation loses trust
- readers cannot understand the system

### Rule

Handbook content must be built with bounded panels, readable spacing, and visual-first explanation. Documentation pages are product assets too.

## 5. Section Components Mixed Into The Wrong Page

### Problem

Section-level patterns were placed directly into the main components page and made the library harder to scan.

### Risk

- unclear library hierarchy
- weak discoverability
- review friction

### Rule

Atomic components, section patterns, and examples stay on separate pages unless there is a clear reason to merge them.
