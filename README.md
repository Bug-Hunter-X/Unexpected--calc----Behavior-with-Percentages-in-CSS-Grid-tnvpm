# Unexpected calc() Behavior with Percentages in CSS Grid

This repository demonstrates a subtle bug involving the CSS `calc()` function when used with percentage values within a `grid-template-columns` property.  Specifically, the issue arises when combining `calc()` with percentage values and `fr` units.  The expected layout is not rendered correctly.

## Bug Description
The `calc()` function doesn't always behave predictably when used with percentages within `grid-template-columns`.  This can lead to unexpected grid layouts.  The issue is particularly noticeable when the parent container is not explicitly sized.

## Solution
The primary solution is to ensure the parent container has explicit dimensions. The `calc()` function will only calculate based on the known dimensions of the container. If these dimensions are dynamic, consider alternative approaches like using viewport units (vw, vh) or JavaScript to calculate the dimensions and then apply them to the parent grid container.