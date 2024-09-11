# Custom CSS Reset - README

This CSS reset is inspired by Josh W. Comeau's article on creating a custom CSS reset to ensure a consistent and accessible design across all browsers. It focuses on resetting common default browser styles while improving usability, accessibility, and maintainability in your projects.

## Why Use This Reset?

Browsers come with their own default styles, which often differ from one another. This reset helps normalize these styles, giving you better control over your design by establishing a consistent baseline. It also includes accessibility enhancements and optimizations for typography, media, and forms.

### Features of This Reset

1. **Intuitive Box-Sizing Model:**
   The default `box-sizing` behavior makes width calculations unintuitive, especially when adding padding or borders. This reset changes the `box-sizing` to `border-box` for all elements, ensuring that padding and border are included within the element's width and height.
   ```css
   *, *::before, *::after {
     box-sizing: border-box;
   }
   ```

2. **Remove Default Margin:**
   Browser-default margins can introduce unexpected spacing in layouts. This reset removes the default margin from all elements.
   ```css
   * {
     margin: 0;
   }
   ```

3. **Accessible Typography and Improved Text Rendering:**
   The line height is set to `1.5`, ensuring readability. In addition, `-webkit-font-smoothing: antialiased;` improves the appearance of text, especially on macOS.
   ```css
   body {
     line-height: 1.5;
     -webkit-font-smoothing: antialiased;
   }
   ```

4. **Optimized Media Elements:**
   Images, videos, and other media elements (like canvas and SVG) are reset to have a block display by default and a maximum width of `100%`, preventing them from overflowing their container.
   ```css
   img, picture, video, canvas, svg {
     display: block;
     max-width: 100%;
   }
   ```

5. **Form Typography Reset:**
   In many browsers, form elements like `input`, `button`, `textarea`, and `select` use a different font style from the rest of the page. This reset ensures that form elements inherit the font from their parent container for consistent typography.
   ```css
   input, button, textarea, select {
     font: inherit;
   }
   ```

6. **Prevent Text Overflow:**
   When text content exceeds the container, this reset ensures that the text wraps cleanly instead of overflowing.
   ```css
   p, h1, h2, h3, h4, h5, h6 {
     overflow-wrap: break-word;
   }
   ```

7. **Root Stacking Context:**
   Creating a root stacking context on the `#root` or `#__next` element ensures isolation of stacking contexts, preventing z-index conflicts between root and child elements in modern JavaScript frameworks (like React).
   ```css
   #root, #__next {
     isolation: isolate;
   }
   ```

### How to Use

Include this reset at the beginning of your CSS to ensure that it applies globally to all elements. You can either copy the code directly or create a separate CSS file for this reset and import it at the start of your stylesheet.

```html
<link rel="stylesheet" href="path/to/reset.css">
```

### Benefits

- Ensures cross-browser consistency
- Improves typography accessibility
- Enhances the rendering of text and media
- Provides a cleaner slate for form elements
- Addresses common layout issues such as overflowing text and element sizing

### Acknowledgment

This reset is inspired by Josh W. Comeau's article on creating custom CSS resets: [Custom CSS Reset](https://www.joshwcomeau.com/css/custom-css-reset/).
