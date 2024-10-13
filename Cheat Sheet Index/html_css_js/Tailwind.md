# Tailwind Cheat Sheet

## 1. **Installation**

| Method                  | Description                                   | Command                                |
|-------------------------|-----------------------------------------------|----------------------------------------|
| **npm**                 | Install via npm.                             | ```bash npm install tailwindcss ```    |
| **CDN**                 | Use Tailwind via CDN (for quick prototyping). | ```html <link href="https://cdn.tailwindcss.com" rel="stylesheet"> ``` |

---

## 2. **Basic Configuration**

| Feature                | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Tailwind Config File**| Create a configuration file.                 | ```bash npx tailwindcss init ```      |
| **PurgeCSS**           | Remove unused styles in production.           | ```javascript module.exports = { purge: ['./src/**/*.{js,jsx,ts,tsx}', './public/index.html'], } ``` |

---

## 3. **Utility Classes**

| Utility Class          | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Spacing**            | Control margin and padding.                   | ```html <div class="m-4 p-2">Content</div> ``` |
| **Colors**             | Set background and text colors.               | ```html <div class="bg-blue-500 text-white">Content</div> ``` |
| **Typography**         | Adjust font sizes and styles.                 | ```html <h1 class="text-2xl font-bold">Heading</h1> ``` |

---

## 4. **Flexbox and Grid**

| Feature                | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Flexbox**            | Create flex containers.                       | ```html <div class="flex justify-between">...</div> ``` |
| **Grid**               | Create grid layouts.                         | ```html <div class="grid grid-cols-3 gap-4">...</div> ``` |

---

## 5. **Responsive Design**

| Feature                | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Responsive Classes** | Apply different styles at different breakpoints. | ```html <div class="text-sm md:text-lg">Responsive Text</div> ``` |

---

## 6. **Hover and Focus States**

| Feature                | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Hover States**       | Change styles on hover.                      | ```html <button class="bg-blue-500 hover:bg-blue-700">Button</button> ``` |
| **Focus States**       | Change styles on focus.                      | ```html <input class="border focus:border-blue-500"> ``` |

---

## 7. **Customizing Colors and Fonts**

| Feature                | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Custom Colors**      | Extend Tailwind colors in `tailwind.config.js`. | ```javascript theme: { extend: { colors: { primary: '#3498db' } } } ``` |
| **Custom Fonts**       | Add custom fonts.                            | ```javascript theme: { extend: { fontFamily: { sans: ['Helvetica', 'Arial'] } } } ``` |

---

## 8. **Using Plugins**

| Plugin                 | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Forms Plugin**       | Add form styles.                             | ```bash npm install @tailwindcss/forms ``` |
| **Aspect Ratio Plugin**| Maintain aspect ratios for elements.        | ```html <div class="aspect-w-16 aspect-h-9">...</div> ``` |

---

## 9. **Components**

| Component              | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Buttons**            | Create button styles.                        | ```html <button class="bg-blue-500 text-white px-4 py-2 rounded">Button</button> ``` |
| **Cards**              | Create card components.                      | ```html <div class="bg-white shadow-lg rounded-lg p-4">Card Content</div> ``` |

---

## 10. **Utilities**

| Utility Feature        | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Visibility**         | Control visibility of elements.              | ```html <div class="hidden md:block">Visible on Medium Screens</div> ``` |
| **Z-Index**            | Control stacking order of elements.          | ```html <div class="z-10">Overlay</div> ``` |

---

This **Tailwind Cheat Sheet** provides a quick reference for using Tailwind CSS effectively in your projects.


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