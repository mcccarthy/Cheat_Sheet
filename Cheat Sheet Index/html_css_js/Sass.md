# SASS Cheat Sheet

## 1. **Basic Syntax**

| Feature                | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Variables**           | Store values in variables for reuse.         | ```scss $primary-color: #3498db; ```  |
| **Nesting**            | Nest selectors for cleaner code.             | ```scss .nav { ul { li { color: $primary-color; } } } ``` |
| **Partials**           | Break styles into smaller files (prefix with `_`). | ```scss @import 'variables'; ```     |
| **Mixins**             | Create reusable blocks of code.              | ```scss @mixin border-radius($radius) { border-radius: $radius; } ``` |
| **Extend**             | Inherit styles from other selectors.          | ```scss .error { color: red; } .alert { @extend .error; } ``` |

---

## 2. **Variables**

| Variable Type          | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Color Variable**     | Define a color variable.                      | ```scss $link-color: #3498db; ```     |
| **Font Variable**      | Define a font variable.                       | ```scss $font-stack: 'Helvetica', sans-serif; ``` |
| **Breakpoints**        | Store media query breakpoints.                | ```scss $mobile: 480px; ```           |

---

## 3. **Nesting**

| Nesting Level          | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Single Level**       | Nest selectors one level deep.               | ```scss .header { .logo { height: 50px; } } ``` |
| **Multiple Levels**    | Nest selectors multiple levels deep.         | ```scss .sidebar { ul { li { a { color: $link-color; } } } } ``` |

---

## 4. **Mixins**

| Mixin Feature           | Description                                   | Example                                |
|-------------------------|-----------------------------------------------|----------------------------------------|
| **Mixin with Parameters** | Define a mixin that accepts parameters.    | ```scss @mixin button($color) { background-color: $color; color: white; } ``` |
| **Using Mixins**        | Use a mixin with parameters.                  | ```scss .btn { @include button($primary-color); } ``` |

---

## 5. **Extend/Inheritance**

| Extend Feature          | Description                                   | Example                                |
|-------------------------|-----------------------------------------------|----------------------------------------|
| **Basic Extend**        | Extend styles from another class.            | ```scss .message { padding: 10px; } .success { @extend .message; color: green; } ``` |

---

## 6. **Operators**

| Operator                | Description                                   | Example                                |
|-------------------------|-----------------------------------------------|----------------------------------------|
| **Addition**            | Add values together.                          | ```scss $width: 100px + 50px; ```     |
| **Subtraction**         | Subtract values.                              | ```scss $height: 100px - 20px; ```    |
| **Multiplication**      | Multiply values.                              | ```scss $area: 10px * 5px; ```        |
| **Division**            | Divide values.                                | ```scss $size: 100px / 4; ```         |

---

## 7. **Control Directives**

| Control Directive       | Description                                   | Example                                |
|-------------------------|-----------------------------------------------|----------------------------------------|
| **If Statement**        | Conditional styles based on a condition.     | ```scss @if $theme == 'dark' { background: black; } ``` |
| **For Loop**            | Loop through a range of values.              | ```scss @for $i from 1 through 3 { .item-#{$i} { width: 50px * $i; } } ``` |
| **Each Loop**           | Loop through lists or maps.                  | ```scss $colors: (red, green, blue); @each $color in $colors { .#{$color} { color: $color; } } ``` |

---

## 8. **Maps**

| Map Feature             | Description                                   | Example                                |
|-------------------------|-----------------------------------------------|----------------------------------------|
| **Define a Map**        | Create a map of key-value pairs.             | ```scss $fonts: (body: 'Helvetica', heading: 'Arial'); ``` |
| **Accessing Map Values**| Retrieve values from a map.                   | ```scss $body-font: map-get($fonts, body); ``` |

---

## 9. **Media Queries**

| Media Query Feature     | Description                                   | Example                                |
|-------------------------|-----------------------------------------------|----------------------------------------|
| **Basic Media Query**   | Apply styles based on screen size.           | ```scss @media (max-width: $mobile) { body { font-size: 12px; } } ``` |
| **Nested Media Query**  | Nest media queries within selectors.         | ```scss .container { @media (max-width: $mobile) { width: 100%; } } ``` |

---

## 10. **Built-in Functions**

| Function                | Description                                   | Example                                |
|-------------------------|-----------------------------------------------|----------------------------------------|
| **darken()**            | Darken a color by a percentage.              | ```scss $color: darken($primary-color, 10%); ``` |
| **lighten()**           | Lighten a color by a percentage.             | ```scss $color: lighten($primary-color, 10%); ``` |
| **mix()**               | Mix two colors together.                      | ```scss $color: mix($color1, $color2, 50%); ``` |
| **rgba()**              | Create a color with an alpha channel.        | ```scss $color: rgba(255, 0, 0, 0.5); ``` |

---

This **SASS Cheat Sheet** provides an overview of essential features and commands for effective styling using SASS.

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