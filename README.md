# Nosebleed Capital

Ticket arbitrage trade log. Single-file HTML site, one tab per trade, published via GitHub Pages.

## Structure

`index.html` is self-contained: markup, CSS, and the tiny tab-switching script all live in that one file.

- Each trade is a `<section class="tab" id="...">` block.
- Each trade has a matching `<button role="tab" data-tab="...">` in the `<nav>` at the top, in the same order as the sections.
- The `data-tab` attribute on the button must match the `id` on the section.

## Adding a trade

1. Copy an existing `<section class="tab">...</section>` block (the US Open 2026 tab is the fullest example).
2. Give the copy a new, unique `id`.
3. Add a `<button role="tab" data-tab="your-new-id">Trade Name</button>` to the `<nav>`, matching the `data-tab` to the new `id`.
4. Fill in the section's content — position, P&L, what happened, and (if there's a next step) a playbook.

No build step. Edit `index.html` directly and push.
