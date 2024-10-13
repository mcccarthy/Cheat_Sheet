
# CSS Long-Winded Properties and Animations Cheat Sheet

## 1. **Complex CSS Properties**

### Text Shadow
- **Syntax**: `text-shadow: h-shadow v-shadow blur-radius color;`

**Example**:
```css
text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
```
* Creates a shadow effect below the text.

### Box Shadow
- **Syntax**: `box-shadow: h-shadow v-shadow blur-radius spread-radius color;`

**Example**:
```css
box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
```
* Creates a shadow effect around the element.

### Gradient Backgrounds
- **Syntax**: `background: linear-gradient(direction, color-stop1, color-stop2, ...);`

**Example**:
```css
background: linear-gradient(to right, #ff7e5f, #feb47b);
```
* Creates a smooth transition between colors.

### Transformations
- **Syntax**: `transform: transform-function;`

**Examples**:
```css
transform: rotate(45deg);
transform: scale(1.5);
transform: translate(20px, 30px);
```

### Transition
- **Syntax**: `transition: property duration timing-function delay;`

**Example**:
```css
transition: all 0.3s ease-in-out;
```
* Smoothly animates changes to properties.

### Custom Properties (CSS Variables)
- **Syntax**: `--variable-name: value;`

**Example**:
```css
:root {
    --main-color: #3498db;
}
.element {
    background-color: var(--main-color);
}
```

---

## 2. **Loading Animations (Spinners)**

### Simple CSS Spinner
```css
.spinner {
    border: 4px solid rgba(0, 0, 0, 0.1);
    border-top: 4px solid #3498db;
    border-radius: 50%;
    width: 40px;
    height: 40px;
    animation: spin 1s linear infinite;
}

@keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}
```

### Bouncing Loader
```css
.bounce {
    width: 20px;
    height: 20px;
    background-color: #3498db;
    border-radius: 50%;
    animation: bounce 0.6s infinite alternate;
}

@keyframes bounce {
    0% { transform: translateY(0); }
    100% { transform: translateY(-30px); }
}
```

### Fading Loader
```css
.loader {
    width: 20px;
    height: 20px;
    background-color: #3498db;
    border-radius: 50%;
    animation: fade 1s infinite alternate;
}

@keyframes fade {
    0% { opacity: 1; }
    100% { opacity: 0; }
}
```

---

## 3. **Common CSS Shortcuts**

### Multiple Backgrounds
- **Syntax**: `background: url(image1), url(image2);`

**Example**:
```css
background: url(image1.png), url(image2.png);
```

### Centering an Element
- **Flexbox Method**:
```css
.parent {
    display: flex;
    justify-content: center;
    align-items: center;
}
```

### Responsive Font Size
- **Using `vw` Units**:
```css
font-size: 2vw; /* 2% of the viewport width */
```

### Quick Margin and Padding
- **Shorthand**:
```css
margin: 10px 15px; /* top-bottom, left-right */
padding: 5px; /* all sides */
```

### Hide Element
```css
display: none; /* completely removes element from flow */
opacity: 0; /* makes it invisible but retains space */
visibility: hidden; /* makes it invisible but retains space */
```

---

## 4. **Best Practices for Writing CSS**

- **Organize with Comments**: Use comments to separate sections for better readability.
- **Use BEM Methodology**: Block Element Modifier for class naming to avoid clashes and maintain consistency.

**Example**:
```css
.block__element--modifier { }
```

- **Avoid Over-Specificity**: Use simple selectors to keep your CSS maintainable.

- **Use Shorthand Properties**: Whenever possible, utilize shorthand to reduce redundancy.

**Example**:
```css
margin: 10px 20px 15px; /* top, left-right, bottom */
```

---

This **CSS Cheat Sheet** covers complex properties, loading animations, shortcuts, and best practices to help streamline your CSS development process.

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