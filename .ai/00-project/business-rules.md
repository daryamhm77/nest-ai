# Business Rules

> The invariants the system must never break. Reference these by ID in code comments.

Format: `BR-<area>-<n>: <rule>`

## Example
- **BR-AUTH-1:** A refresh token is single-use; rotation invalidates the previous token.
- **BR-AUTH-2:** A locked account cannot obtain new tokens until unlocked by an admin.
- **BR-BILL-1:** An invoice total must equal the sum of its line items including tax.
- **BR-BILL-2:** Issued invoices are immutable; corrections create a credit note.

> Each rule should have a corresponding test. Tag tests with the BR id.
