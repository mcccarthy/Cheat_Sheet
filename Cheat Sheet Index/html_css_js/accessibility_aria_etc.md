# Accessibility (a11y) Cheat Sheet

## Key Accessibility Practices

| Practice                      | Description                                         |
|-------------------------------|-----------------------------------------------------|
| **ARIA Roles**                | Use `role` attributes to enhance accessibility where native HTML elements fall short (e.g., `role="button"`, `role="navigation"`). |
| **Keyboard Navigation**       | Ensure all interactive elements (links, buttons, forms) can be navigated via keyboard (`Tab`, `Enter`, `Space`). Use `tabindex` to control focus. |
| **Focus Management**          | Properly manage focus states, especially during dynamic content updates. Use `focus()` and `aria-live` to guide screen reader users. |
| **Color Contrast**            | Ensure sufficient contrast between text and background. Follow WCAG's minimum contrast ratio of 4.5:1 for normal text and 3:1 for large text. |
| **Alt Text for Images**       | Provide meaningful `alt` text for images to describe their purpose or content to users relying on screen readers. Decorative images should have `alt=""`. |
| **Form Labels**               | Use `<label>` elements for all form inputs, making them accessible to screen readers and touch devices. Ensure labels are descriptive and clear. |
| **Skip Links**                | Provide a "Skip to Content" link at the top of the page to allow keyboard users to bypass repetitive navigation. |
| **Avoid Auto-Play Media**     | Do not auto-play audio or video. If needed, provide controls to pause, stop, or mute media content. |
| **Responsive Text**           | Ensure text is scalable using relative units like `em` or `%` instead of fixed units like `px`. |

* * *

## Common Screen Reader Considerations

| Consideration                  | Description                                         |
|--------------------------------|-----------------------------------------------------|
| **Use of ARIA Landmarks**      | Use ARIA landmarks like `role="banner"`, `role="main"`, `role="navigation"` to help screen readers navigate the page structure. |
| **Descriptive Links**          | Ensure links are descriptive and make sense out of context. Avoid vague text like "click here" or "read more." |
| **Heading Structure**          | Use headings (`<h1>`, `<h2>`, etc.) in a logical and hierarchical manner to improve navigation for screen reader users. |
| **aria-live Regions**          | Use `aria-live="polite"` or `aria-live="assertive"` to announce dynamic content updates (e.g., loading indicators, notifications) to screen readers. |
| **Screen Reader Testing**      | Test your application using screen readers like NVDA, JAWS, or VoiceOver to ensure proper interaction. |
| **Labels for Custom Widgets**  | Ensure custom elements (e.g., dropdowns, sliders) have appropriate labels using ARIA attributes like `aria-label`, `aria-labelledby`, and `aria-describedby`. |

* * *

## Semantic HTML for Improved Accessibility

| Element        | Usage                                          |
|----------------|------------------------------------------------|
| **\<article\>**  | Represents self-contained content that can be independently distributed or reused. Useful for blogs, news articles, etc. |
| **\<section\>**  | Groups related content within a larger context, often with a heading. |
| **\<header\>**   | Represents the introductory content, typically a group of introductory or navigational aids. |
| **\<nav\>**      | Defines a section containing navigation links, helping users and screen readers understand page structure. |
| **\<main\>**     | Represents the main content of the document, distinct from navigation, sidebars, footers, etc. |
| **\<aside\>**    | Represents complementary content that is tangentially related to the main content (e.g., sidebars, pull quotes). |
| **\<footer\>**   | Represents the footer of a section or page, usually containing metadata or links to related documents. |
| **\<button\>**   | Use the native `<button>` element for all clickable actions instead of `div` or `span`, as it is natively focusable and accessible. |
| **\<fieldset\> & \<legend\>** | Group related form controls with `<fieldset>` and use `<legend>` to give them a label for better screen reader interaction. |

---

This cheat sheet provides key practices, ARIA roles, and semantic HTML usage for improving web accessibility, making it easier to develop inclusive applications.


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


