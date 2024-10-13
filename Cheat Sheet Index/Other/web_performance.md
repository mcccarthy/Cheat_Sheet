# Web Performance Optimization Cheat Sheet

## Tips for Reducing Load Times

| Technique                     | Description                                         |
|-------------------------------|-----------------------------------------------------|
| **Minification**              | Remove unnecessary characters from CSS, JavaScript, and HTML files to reduce file size. Tools: UglifyJS, CSSNano, HTMLMinifier. |
| **Compression**               | Enable Gzip or Brotli compression on your server to reduce the size of files sent over the network. |
| **Image Optimization**        | Compress and resize images without losing quality. Use formats like WebP, and tools like ImageOptim or TinyPNG. |
| **Reduce HTTP Requests**      | Minimize the number of elements on a page (combine CSS/JS files, use CSS sprites). |
| **Use a Content Delivery Network (CDN)** | Serve content from servers located closer to users, reducing latency and load times. |
| **Asynchronous Loading**      | Load JavaScript files asynchronously (`async` or `defer` attributes) to prevent blocking rendering. |
| **Critical CSS**              | Inline critical CSS for above-the-fold content to speed up initial rendering. |

* * *

## Best Practices for Caching

| Technique                     | Description                                         |
|-------------------------------|-----------------------------------------------------|
| **Browser Caching**           | Set `Cache-Control` and `Expires` headers to instruct browsers to cache static resources. |
| **Server-Side Caching**       | Implement caching mechanisms like Redis or Memcached to store database query results and reduce load times. |
| **Page Caching**              | Store entire rendered pages for frequently accessed content to serve users faster. |
| **Content Versioning**        | Use versioning in your asset URLs (e.g., `/style.v1.css`) to ensure users receive the latest files after updates. |
| **Cache Busting**             | Append a query string or hash to asset URLs to force cache refresh when files are updated. |

* * *

## Lazy Loading Techniques

| Technique                     | Description                                         |
|-------------------------------|-----------------------------------------------------|
| **Lazy Loading Images**       | Defer loading images that are not visible in the viewport until they are needed (use the `loading="lazy"` attribute or Intersection Observer API). |
| **Lazy Loading Resources**    | Delay loading of scripts and styles that are not immediately necessary for the initial render. |
| **Responsive Images**         | Use the `<picture>` element and `srcset` attribute to load appropriately sized images based on screen size and resolution. |
| **Deferred JavaScript**       | Load non-critical JavaScript files after the main content has loaded, using `defer` or `async` attributes. |

---

This cheat sheet provides essential tips and best practices for optimizing web performance, ensuring faster load times, efficient caching, and better user experiences. Feel free to modify or expand it according to your specific needs!


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