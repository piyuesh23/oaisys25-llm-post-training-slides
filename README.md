# HTML Presentation with Reveal.js

A modern, responsive HTML presentation built with Reveal.js framework.

## 🚀 Quick Start

1. **Open the presentation:**
   - Simply open `index.html` in your web browser
   - Or use a local server for best results:
     ```bash
     python -m http.server 8000
     ```
     Then visit `http://localhost:8000`

2. **Navigate the slides:**
   - **Arrow keys**: Navigate between slides
   - **Space bar**: Next slide
   - **ESC**: Overview mode (see all slides)
   - **F**: Fullscreen mode
   - **S**: Speaker notes view
   - **B**: Pause/blackout
   - **?**: Show keyboard shortcuts

## 📁 Files

- `index.html` - Main presentation file
- `styles.css` - Custom styling
- `README.md` - This file

## ✨ Features Included

### Slide Types
- **Title slide** with gradient background
- **Agenda slide** with bullet points
- **Two-column layouts** for comparisons
- **Vertical slides** for detailed content
- **Image slides** with placeholders
- **Code slides** with syntax highlighting
- **Quote slides** with custom backgrounds
- **Statistics/data slides** with grid layout
- **Animated lists** with progressive reveal

### Customization

#### Change Theme
Replace the theme in `index.html`:
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@4.6.0/dist/theme/[THEME].css">
```

Available themes: `black`, `white`, `league`, `beige`, `sky`, `night`, `serif`, `simple`, `solarized`, `blood`, `moon`

#### Modify Colors
Edit CSS variables in `styles.css`:
```css
:root {
    --primary-color: #4A90E2;
    --secondary-color: #17b2c3;
    --accent-color: #f39c12;
}
```

#### Change Transitions
In `index.html`, modify the Reveal.initialize options:
```javascript
transition: 'slide', // none/fade/slide/convex/concave/zoom
```

## 📝 Adding Your Content

### Add a New Slide
```html
<section>
    <h2>Your Slide Title</h2>
    <p>Your content here</p>
</section>
```

### Add Vertical Slides
```html
<section>
    <section>
        <h2>Main Topic</h2>
    </section>
    <section>
        <h3>Sub-topic</h3>
    </section>
</section>
```

### Add Fragments (Progressive Reveal)
```html
<ul>
    <li class="fragment">Appears first</li>
    <li class="fragment">Appears second</li>
</ul>
```

### Add Images
```html
<img src="path/to/your/image.jpg" alt="Description">
```

### Add Code
```html
<pre><code data-trim class="javascript">
// Your code here
function example() {
    return "Hello World";
}
</code></pre>
```

## 🎨 Advanced Features

### Speaker Notes
Add notes that only appear in speaker view (press 'S'):
```html
<section>
    <h2>Slide Title</h2>
    <aside class="notes">
        These are speaker notes, only visible in presenter mode
    </aside>
</section>
```

### Background Colors/Images
```html
<section data-background-color="#ff0000">
    Content here
</section>

<section data-background-image="image.jpg">
    Content here
</section>
```

### Auto-Animate
```html
<section data-auto-animate>
    <h2>Title</h2>
</section>
<section data-auto-animate>
    <h2>Title</h2>
    <p>New content smoothly animates in</p>
</section>
```

## 📤 Exporting

### Export to PDF
1. Add `?print-pdf` to the URL: `index.html?print-pdf`
2. Open print dialog (Ctrl/Cmd + P)
3. Save as PDF

### Share Online
- Deploy to GitHub Pages
- Upload to Netlify/Vercel
- Host on any web server

## 🔧 Configuration Options

Edit the `Reveal.initialize()` section in `index.html`:

```javascript
Reveal.initialize({
    controls: true,          // Show navigation controls
    progress: true,          // Show progress bar
    center: true,            // Center slides vertically
    hash: true,              // Enable URL hash navigation
    slideNumber: true,       // Show slide numbers
    transition: 'slide',     // Transition style
    autoSlide: 0,           // Auto-slide interval (0 = off)
    loop: false,            // Loop presentation
    rtl: false,             // Right-to-left mode
});
```

## 📚 Resources

- [Reveal.js Documentation](https://revealjs.com/)
- [Reveal.js GitHub](https://github.com/hakimel/reveal.js)
- [More Themes](https://github.com/hakimel/reveal.js/tree/master/css/theme)

## 💡 Tips

1. Keep slides simple and focused
2. Use high-quality images
3. Limit text per slide (6x6 rule: max 6 bullets, 6 words each)
4. Test on the device/screen you'll present on
5. Practice with speaker notes
6. Have a backup (PDF export)

---

**Need help?** Check the Reveal.js documentation or press `?` during the presentation for keyboard shortcuts.
