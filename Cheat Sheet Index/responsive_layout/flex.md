# CSS Flexbox Cheat Sheet

## Flex Container Properties

| Property               | Description                                                          | Default | Value Options                                     |
|-----------------------|----------------------------------------------------------------------|---------|--------------------------------------------------|
| `display`             | Defines a flex container.                                           | `block` | `flex`, `inline-flex`                            |
| `flex-direction`      | Defines the direction of the flex items.                            | `row`   | `row`, `row-reverse`, `column`, `column-reverse`|
| `flex-wrap`           | Defines whether flex items should wrap onto multiple lines.         | `nowrap`| `nowrap`, `wrap`, `wrap-reverse`                |
| `flex-flow`           | Shorthand for `flex-direction` and `flex-wrap`.                    |         | `row wrap`, `column nowrap`, etc.                |
| `justify-content`     | Aligns flex items along the main axis.                             | `flex-start` | `flex-start`, `flex-end`, `center`, `space-between`, `space-around`, `space-evenly` |
| `align-items`         | Aligns flex items along the cross axis.                             | `stretch` | `flex-start`, `flex-end`, `center`, `baseline`, `stretch` |
| `align-content`       | Aligns flex lines when there is extra space in the cross axis.     | `stretch` | `flex-start`, `flex-end`, `center`, `space-between`, `space-around`, `stretch` |
| `align-self`          | Overrides `align-items` for individual flex items.                  | `auto`  | `flex-start`, `flex-end`, `center`, `baseline`, `stretch` |

---

## Flex Item Properties

| Property              | Description                                                          | Default | Value Options                                     |
|-----------------------|----------------------------------------------------------------------|---------|--------------------------------------------------|
| `flex-grow`           | Defines the ability for a flex item to grow if necessary.           | `0`     | `0` or a positive number                          |
| `flex-shrink`         | Defines the ability for a flex item to shrink if necessary.         | `1`     | `0` or a positive number                          |
| `flex-basis`          | Defines the default size of an element before the remaining space is distributed. | `auto` | Length (px, em, etc.), `auto`                   |
| `flex`                | Shorthand for `flex-grow`, `flex-shrink`, and `flex-basis`.        |         | `none`, `auto`, `1 1 auto`, etc.                 |
| `align-self`          | Allows the default alignment (or the one specified by `align-items`) to be overridden for individual flex items. | `auto`  | `flex-start`, `flex-end`, `center`, `baseline`, `stretch` |
| `order`               | Defines the order of the flex items.                                | `0`     | Integer values                                   |

---

## Shorthand Properties

| Property              | Description                                                          | Example                       |
|-----------------------|----------------------------------------------------------------------|-------------------------------|
| `flex`                | Shorthand for `flex-grow`, `flex-shrink`, and `flex-basis`.        | `flex: 1 0 20%`              |
| `flex-flow`           | Shorthand for `flex-direction` and `flex-wrap`.                    | `flex-flow: row wrap`        |
| `align`               | Shorthand for `align-items` and `align-content`.                   | `align: center`              |

---

# Quick Reference

- **Container Commands**: Use the container properties to define the overall behavior of the flex items.
- **Child Commands**: Use the child properties to define how individual items behave within the flex container.
- **Shorthand Properties**: Use shorthand properties for concise code.

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
