# INCW_4 — Grid and Flexbox

In-class activity 4 for Web Programming. Two layout exercises in plain HTML and CSS.

## Part 1 — Recipe with Flexbox (`recipe_flexbox/`)

A recipe page laid out with CSS Flexbox, a one-dimensional layout system.

- `header` uses `display: flex` with `justify-content: space-between` to push the
  logo and the sign-in/search links to opposite ends.
- `.content` and `.main-content` use `flex-wrap: wrap` so the columns stack
  instead of squishing when the viewport gets narrow.
- `.ingredients` and `.directions` each use `flex-basis: 45%` with `flex-grow: 1`,
  leaving roughly 10% of the width as the channel between the two columns.
- `.title` uses `align-items: baseline` so the heading and the byline sit on the
  same text baseline despite their different font sizes.
- `.summary > div > div` uses the child combinator twice to reach the four
  label/value pairs inside the facts box, spacing each pair with
  `justify-content: space-between`.

## Part 2 — Tic-Tac-Toe with Grid (`tic_tac_toe_grid/`)

A game board laid out with CSS Grid, a two-dimensional layout system.

- `#board` uses `display: grid` with `repeat(3, 100px)` for both
  `grid-template-columns` and `grid-template-rows`, giving nine equal cells.
- `gap: 10px` creates the channels between cells, and `justify-content: center`
  centres the whole board horizontally.
- Each cell uses `display: flex` with `align-items` and `justify-content` set to
  `center`, so the X or O stays centred regardless of cell size.
- Cells have a hover state for feedback.

## Why each system

The board has a rigid structure known in advance, in two dimensions at once —
that is Grid's job. The recipe's content flows along one axis at a time and
sizes itself from its contents — that is Flexbox's job.
