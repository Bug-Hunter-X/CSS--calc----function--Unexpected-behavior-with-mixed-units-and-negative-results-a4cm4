# CSS `calc()` Function: Unexpected Behavior with Mixed Units and Negative Results

This repository demonstrates an uncommon error related to the CSS `calc()` function, specifically concerning inconsistent units and the potential for negative values.

## Problem

The `calc()` function in CSS provides a way to perform calculations directly within CSS properties. However, there are subtle issues that can arise. The primary problem here involves mixing percentage units with pixel units within the same calculation. Additionally, using `vh` (viewport height) can lead to negative calculated values under certain conditions (viewport height less than 20px in example).   This will result in either 0px or potential unexpected layout issues.

## Solution

The solution involves ensuring consistent units within the calculation.  Convert all values to a single unit (pixels or percentages) before using `calc()`.  For a more robust solution, you may add conditional logic to handle the situation where `calc()` might produce a negative value.