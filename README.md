# CSS Specificity Issue with :has()

This repository demonstrates a subtle but important specificity issue that can arise when using the CSS `:has()` pseudo-class. The problem occurs when a selector with higher specificity targets the same element, potentially overriding the styling applied by `:has()`, even if the `:has()` condition is true.

## Bug Description
The `:has()` pseudo-class, while powerful, does not automatically guarantee that its styling will be applied. In this case, a more specific selector can override the `:has()` styling.

## Bug Solution
The solution involves carefully managing specificity using techniques such as adding more specific classes or, less ideally, using `!important` as a last resort.

## How to Reproduce
1. Clone this repository.
2. Open `bug.html` in your browser.
3. Observe that the `.container` element does not have the intended `lightblue` background, despite containing a `<p>` element.
4. Open `bugSolution.html` to see the corrected styling.