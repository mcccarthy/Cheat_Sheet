Here’s a **cheatsheet** for **CSS Grid**:

### Grid Container Properties:

1. **display**:
    `grid` | `inline-grid`

    * Defines a grid container.
2. **grid-template-columns**:
    `<track-size> ...` | `repeat()`

    * Defines columns in the grid.
3. **grid-template-rows**:
    `<track-size> ...` | `repeat()`

    * Defines rows in the grid.
4. **grid-template-areas**:
    `"<area-name> <area-name>"`

    * Defines grid areas by assigning names to cells.
5. **grid-template**:
    `grid-template-rows` + `grid-template-columns` + `grid-template-areas`

    * Shorthand for defining both rows, columns, and areas.
6. **grid-column-gap**: (or `column-gap`)
    `<length>`

    * Specifies the gap between columns.
7. **grid-row-gap**: (or `row-gap`)
    `<length>`

    * Specifies the gap between rows.
8. **grid-gap**:
    `row-gap column-gap`

    * Shorthand for `grid-row-gap` and `grid-column-gap`.
9. **justify-items**:
    `start` | `end` | `center` | `stretch`

    * Aligns grid items horizontally.
10. **align-items**:
    `start` | `end` | `center` | `stretch`

    * Aligns grid items vertically.
11. **justify-content**:
    `start` | `end` | `center` | `stretch` | `space-between` | `space-around` | `space-evenly`

    * Aligns the entire grid horizontally.
12. **align-content**:
    `start` | `end` | `center` | `stretch` | `space-between` | `space-around`

    * Aligns the entire grid vertically.

* * *

### Grid Item Properties:

1. **grid-column-start** / **grid-column-end**:
    `<line>` | `span <number>`

    * Defines where the grid item starts and ends on the column axis.
2. **grid-row-start** / **grid-row-end**:
    `<line>` | `span <number>`

    * Defines where the grid item starts and ends on the row axis.
3. **grid-area**:
    `<grid-area-name>`

    * Assigns a grid item to a specific named area.
4. **justify-self**:
    `start` | `end` | `center` | `stretch`

    * Aligns a grid item inside its cell horizontally.
5. **align-self**:
    `start` | `end` | `center` | `stretch`

    * Aligns a grid item inside its cell vertically.

* * *

### Grid Shortcuts:

1. **Shorthand for grid columns/rows**:

    ```css
    grid: auto / 1fr 1fr 1fr; /* One row, three equal columns */
    ```

2. **Placing items in a grid**:

    ```css
    grid-column: 1 / span 2; /* Start at column 1, span 2 columns */
    grid-row: 1 / 3; /* Start at row 1, end at row 3 */
    ```

3. **Shorthand for areas**:

    ```css
    grid-template-areas:
      "header header"
      "sidebar content";
    ```


* * *

This covers key properties and shortcuts for **CSS Grid Layout**!