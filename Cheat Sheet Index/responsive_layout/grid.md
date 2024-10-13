# CSS Grid Cheat Sheet

## Grid Container Properties

| Property                  | Description                                                         | Value Options                                             |
|---------------------------|---------------------------------------------------------------------|----------------------------------------------------------|
| `display`                 | Defines a grid container.                                          | `grid`, `inline-grid`                                   |
| `grid-template-columns`   | Defines columns in the grid.                                      | `<track-size> ...`, `repeat()`                          |
| `grid-template-rows`      | Defines rows in the grid.                                         | `<track-size> ...`, `repeat()`                          |
| `grid-template-areas`     | Defines grid areas by assigning names to cells.                   | `"<area-name> <area-name>"`                             |
| `grid-template`           | Shorthand for defining both rows, columns, and areas.            | `grid-template-rows` + `grid-template-columns` + `grid-template-areas` |
| `grid-column-gap`         | Specifies the gap between columns.                                | `<length>`                                              |
| `grid-row-gap`            | Specifies the gap between rows.                                   | `<length>`                                              |
| `grid-gap`                | Shorthand for `grid-row-gap` and `grid-column-gap`.              | `row-gap column-gap`                                   |
| `justify-items`           | Aligns grid items horizontally.                                   | `start`, `end`, `center`, `stretch`                    |
| `align-items`             | Aligns grid items vertically.                                     | `start`, `end`, `center`, `stretch`                    |
| `justify-content`         | Aligns the entire grid horizontally.                               | `start`, `end`, `center`, `stretch`, `space-between`, `space-around`, `space-evenly` |
| `align-content`           | Aligns the entire grid vertically.                                 | `start`, `end`, `center`, `stretch`, `space-between`, `space-around` |

---

## Grid Item Properties

| Property                  | Description                                                         | Value Options                                             |
|---------------------------|---------------------------------------------------------------------|----------------------------------------------------------|
| `grid-column-start` / `grid-column-end` | Defines where the grid item starts and ends on the column axis. | `<line>`, `span <number>`                               |
| `grid-row-start` / `grid-row-end` | Defines where the grid item starts and ends on the row axis.     | `<line>`, `span <number>`                               |
| `grid-area`               | Assigns a grid item to a specific named area.                     | `<grid-area-name>`                                      |
| `justify-self`            | Aligns a grid item inside its cell horizontally.                   | `start`, `end`, `center`, `stretch`                    |
| `align-self`              | Aligns a grid item inside its cell vertically.                     | `start`, `end`, `center`, `stretch`                    |

---

## Grid Shortcuts

| Property                  | Example                                                           |
|---------------------------|-------------------------------------------------------------------|
| **Shorthand for grid columns/rows** | `grid: auto / 1fr 1fr 1fr;` /* One row, three equal columns */ |
| **Placing items in a grid** | `grid-column: 1 / span 2;` /* Start at column 1, span 2 columns */ <br> `grid-row: 1 / 3;` /* Start at row 1, end at row 3 */ |
| **Shorthand for areas**   | ```css <br> grid-template-areas: <br> "header header" <br> "sidebar content"; <br> ``` |

---

This covers key properties and shortcuts for **CSS Grid Layout**!


Key Command
Ctrl/Cmd + B Toggle bold
Ctrl/Cmd + I Toggle italic
Alt+S (on Windows) Toggle strikethrough1
Ctrl + Shift + ] Toggle heading (uplevel)
Ctrl + Shift + [ Toggle heading (downlevel)
Ctrl/Cmd + M Toggle math environment
Alt + C Check/Uncheck task list item
Ctrl/Cmd + Shift + V Toggle preview
Ctrl/Cmd + K V Toggle preview to side