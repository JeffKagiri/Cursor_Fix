# Cursor_Fix
## Prompt  
identify and fix layout bugs and refactor it into a reusable component (e.g., Card(title, price, features))

## Changes Made

1. **Fixed Layout Bugs**
   - Corrected `box-shdow` typo to `box-shadow`.
   - Properly closed the `<h2>` tag.
   - Added `cursor: pointer` to the button for better UX.

2. **Refactored into a Reusable Component**
   - Moved the card content into a `Card(title, price, features)` JavaScript function.
   - The function generates the HTML dynamically based on the arguments provided.
   - Used `features.map()` to render feature list items dynamically.
   - Appended the generated card into the container with `innerHTML`.

3. **Maintained Original Content**
   - The card still displays **Basic Plan**, **$9.99/month**, and the same list of features.
   - Button functionality and styles remain unchanged.

## How to Use
- Update the `Card` function call in the script with new `title`, `price`, and `features` values to generate different pricing cards.
- Example:
  ```js
  document.getElementById("pricing-container").innerHTML = Card(
    "Pro Plan",
    "$19.99 /month",
    ["10 GB Storage", "Priority Support", "Advanced Features"]
  );
