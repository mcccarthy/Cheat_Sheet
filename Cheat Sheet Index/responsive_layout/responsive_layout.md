# Responsive Design Cheat Sheet

## Media Queries and Breakpoints

Media queries allow you to apply styles based on the device's characteristics, such as width and height. Below are some common breakpoints:

| Device Type      | Minimum Width (px) | Example Media Query                                      |
|------------------|---------------------|----------------------------------------------------------|
| Mobile           | 320                 | `@media (max-width: 320px) { ... }`                     |
| Mobile (Large)   | 480                 | `@media (max-width: 480px) { ... }`                     |
| Tablet           | 768                 | `@media (max-width: 768px) { ... }`                     |
| Desktop (Small)  | 1024                | `@media (max-width: 1024px) { ... }`                    |
| Desktop          | 1280                | `@media (max-width: 1280px) { ... }`                    |
| Large Desktop    | 1440                | `@media (max-width: 1440px) { ... }`                    |

### Example Media Query

```css
@media (max-width: 768px) {
  body {
    background-color: lightblue;
  }

  .container {
    flex-direction: column;
  }
}

.container {
  display: flex;
  flex-wrap: wrap; /* Allows items to wrap onto the next line */
  justify-content: space-between; /* Distributes space between items */
}

.item {
  flex: 1 1 200px; /* Grow, shrink, basis */
  margin: 10px;
}

@media (max-width: 768px) {
  .item {
    flex: 1 1 100%; /* Full width on small screens */
  }
}

Grid


.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr); /* Three equal columns */
  gap: 20px; /* Space between items */
}

.item {
  background-color: lightgray;
  padding: 20px;
}

@media (max-width: 768px) {
  .container {
    grid-template-columns: repeat(2, 1fr); /* Two columns on small screens */
  }
}

@media (max-width: 480px) {
  .container {
    grid-template-columns: 1fr; /* Single column on very small screens */
  }
}


Mobile-First Design Principles
Start with Mobile: Design for the smallest screen first, then progressively enhance for larger screens.

Use Relative Units: Utilize em, rem, %, and vh/vw for sizing instead of fixed units like px to ensure scalability.

Flexible Images: Use CSS properties like max-width: 100% to ensure images scale within their containers.

Touch Targets: Make buttons and links large enough for easy tapping (minimum 44px by 44px).

Avoid Fixed Widths: Use flexible layouts to ensure your design adapts to different screen sizes.


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