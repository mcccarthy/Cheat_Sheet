# CSS Cheat Sheet

## CSS Selectors and Specificity

| Selector                   | Description                                       | Example                                  |
|----------------------------|---------------------------------------------------|------------------------------------------|
| `*`                        | Universal selector, selects all elements.       | `* { margin: 0; padding: 0; }`         |
| `element`                 | Selects all specified elements.                  | `p { color: blue; }`                    |
| `.class`                  | Selects all elements with the specified class.   | `.btn { background-color: green; }`    |
| `#id`                     | Selects the element with the specified ID.       | `#header { font-size: 24px; }`         |
| `element1, element2`      | Selects multiple elements.                        | `h1, h2 { color: red; }`                |
| `element element`         | Selects descendants of an element.               | `ul li { list-style: none; }`          |
| `element > element`       | Selects direct children of an element.           | `div > p { margin-bottom: 10px; }`     |
| `element + element`       | Selects the next sibling of an element.          | `h1 + p { color: grey; }`               |
| `element ~ element`       | Selects all siblings after the specified element. | `h1 ~ p { font-weight: bold; }`        |
| `:hover`, `:focus`        | Pseudo-classes for interactive states.           | `a:hover { text-decoration: underline; }` |

### Specificity Calculation

- **Inline styles**: 1000 (e.g., `style="color: red;"`)
- **IDs**: 100 (e.g., `#header`)
- **Classes, attributes, and pseudo-classes**: 10 (e.g., `.btn`, `[type="text"]`, `:hover`)
- **Elements and pseudo-elements**: 1 (e.g., `div`, `::before`)

* * *

## Box Model Properties

| Property                  | Description                                       | Example                                  |
|---------------------------|---------------------------------------------------|------------------------------------------|
| `margin`                  | Space outside the element.                        | `margin: 20px;`                         |
| `padding`                 | Space inside the element, between content and border. | `padding: 10px;`                       |
| `border`                  | Defines border around the element.                | `border: 1px solid black;`              |
| `width`                   | Width of the element.                             | `width: 100px;`                          |
| `height`                  | Height of the element.                            | `height: 200px;`                         |
| `box-sizing`              | Controls box model calculations.                  | `box-sizing: border-box;`               |

### Box Model Calculation

- **Content Box**: Width/Height = `content`
- **Padding Box**: Width/Height = `content + padding`
- **Border Box**: Width/Height = `content + padding + border`
- **Margin Box**: Width/Height = `content + padding + border + margin`

* * *

## Positioning

| Property                   | Description                                       | Example                                  |
|----------------------------|---------------------------------------------------|------------------------------------------|
| `position`                 | Defines the type of positioning method.          | `position: relative;`                    |
| `static`                   | Default positioning.                             | `position: static;`                      |
| `relative`                 | Positioned relative to its normal position.      | `position: relative; top: 10px;`        |
| `absolute`                 | Positioned relative to the nearest positioned ancestor. | `position: absolute; left: 20px;`      |
| `fixed`                    | Positioned relative to the viewport.             | `position: fixed; bottom: 0;`           |
| `sticky`                   | Toggles between relative and fixed.              | `position: sticky; top: 0;`             |
| `z-index`                  | Controls stacking order of positioned elements.  | `z-index: 10;`                          |

* * *

## Common CSS Properties

| Property                   | Description                                       | Example                                  |
|----------------------------|---------------------------------------------------|------------------------------------------|
| `background`               | Sets background color, image, or gradient.       | `background: #f0f0f0;`                  |
| `color`                    | Sets text color.                                 | `color: black;`                          |
| `font-family`              | Sets font type for the text.                     | `font-family: 'Arial', sans-serif;`     |
| `font-size`                | Sets the size of the text.                       | `font-size: 16px;`                       |
| `line-height`              | Sets space between lines of text.                | `line-height: 1.5;`                     |
| `text-align`               | Aligns text within an element.                   | `text-align: center;`                    |
| `display`                  | Specifies the display behavior of an element.    | `display: block;`                        |
| `flex`                     | Sets a flexible length for a flex item.          | `flex: 1;`                               |
| `grid`                     | Defines a grid layout.                           | `display: grid; grid-template-columns: repeat(3, 1fr);` |
| `overflow`                 | Controls overflow content.                        | `overflow: hidden;`                      |
| `opacity`                  | Sets the transparency level of an element.       | `opacity: 0.5;`                          |

---

This cheat sheet provides an overview of essential CSS selectors, the box model, positioning techniques, and common CSS properties. You can expand it with more detailed properties or examples as you continue your web development learning journey!

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
