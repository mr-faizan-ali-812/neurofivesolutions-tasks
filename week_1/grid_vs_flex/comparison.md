# Flexbox vs Grid — 3-Column Pricing Layout

Same markup, same visual result, two different layout engines. Here's where each one felt easier or harder.

## Where Flexbox was easier

- **Header and footer.** Both are one-dimensional bars (logo — nav — button; copyright — links). Flexbox's `justify-content: space-between` handles that in one line with no need to think in tracks.
- **Equal-height cards, no extra work.** `align-items: stretch` (the default) just works because Flexbox already thinks of the row as one flex line.
- **Pushing the button to the bottom of each card.** `flex-grow: 1` on the features list is a natural, well-known pattern — it eats the remaining space in that single column direction.

## Where Grid was easier

- **The 3-column pricing row itself.** `grid-template-columns: repeat(3, 1fr)` states the *structure* directly — three equal tracks — rather than Flexbox's `flex: 1 1 0` on each child, which achieves equal widths as a side effect of flex-basis math rather than declaring it.
- **Reasoning about rows within each card.** Grid let me define `grid-template-rows: auto auto auto auto 1fr auto` for name/desc/price/billed/features/button, which makes the vertical rhythm explicit up front. In Flexbox that same effect (features expanding, button pinned to bottom) is implicit and easy to get wrong on a card with a different number of rows.
- **The responsive collapse.** Both approaches collapse to one column in a single line (`flex-direction: column` vs `grid-template-columns: 1fr`), so this was a tie — but Grid's version reads more clearly as "we're changing the *number of tracks*," which is closer to what's conceptually happening.

## Where it got awkward

- **Flexbox** needed `flex-wrap` and manual gap tuning in the footer once it had to wrap on small screens — Flexbox doesn't know about a "grid" of items, so wrapped items don't align into clean columns/rows the way Grid's do.
- **Grid** felt like overkill for the header/footer bars. Naming three grid tracks (`auto 1fr auto`) for what is fundamentally "space three things apart in a row" is more ceremony than the equivalent Flexbox line.

## Rule of thumb this exercise confirmed

- **One-dimensional bars (nav bars, footers, button groups, toolbars) → Flexbox.** You're arranging items along a single axis; Flexbox's content-driven sizing shines here.
- **Two-dimensional, structured regions (the pricing grid itself, page layouts, card internals with a defined vertical rhythm) → Grid.** You're declaring a layout template — Grid lets you state the structure once instead of coordinating sizing rules across children.
- In real projects these get combined constantly: Grid for the page skeleton and card grid, Flexbox for the one-dimensional content inside each card/header/footer. This demo used each in isolation on purpose, which is exactly what made the seams visible.
