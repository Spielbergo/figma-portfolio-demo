# Development Guide

## Project Overview

This is a vanilla HTML/CSS/JS portfolio website with no build process or dependencies. It's designed to be simple, fast, and easy to maintain.

## Development Workflow

### 1. Local Development

The easiest way to develop is to use a local server:

**Option A: VS Code Live Server Extension**
- Install "Live Server" extension in VS Code
- Right-click `index.html` and select "Open with Live Server"
- Auto-reloads on file changes

**Option B: Python**
```bash
python -m http.server 8000
```

**Option C: Node.js**
```bash
npx serve
```

### 2. File Organization

```
├── index.html      # Main HTML - semantic structure
├── styles.css      # All styles - mobile-first approach
├── script.js       # Vanilla JavaScript - no frameworks
└── images/         # All image assets
```

## Code Standards

### HTML

- Use semantic HTML5 elements (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`)
- Include ARIA labels for accessibility
- Keep proper heading hierarchy (h1 → h2 → h3)
- Add `alt` attributes to all images
- Use `loading="lazy"` for images below the fold

### CSS

- **Mobile-first**: Base styles for mobile, media queries for larger screens
- **CSS Variables**: Use custom properties in `:root` for consistency
- **BEM-like naming**: `.component-element--modifier` pattern
- **No preprocessors**: Pure CSS for simplicity
- **Performance**: Minimize layout shifts, use `transform` for animations

```css
/* Good - uses transform */
.element:hover {
    transform: translateY(-4px);
}

/* Avoid - causes layout reflow */
.element:hover {
    margin-top: -4px;
}
```

### JavaScript

- **ES6+**: Use modern JavaScript features
- **IIFE**: Wrap code to avoid global scope pollution
- **Event delegation**: Efficient event handling
- **Accessibility**: Keyboard navigation, focus management
- **Performance**: Use throttling/debouncing for scroll events

## Accessibility Checklist

- [ ] Semantic HTML structure
- [ ] ARIA labels where needed
- [ ] Keyboard navigation works
- [ ] Focus visible on interactive elements
- [ ] Skip to main content link
- [ ] Alt text on images
- [ ] Color contrast meets WCAG AA standards
- [ ] Reduced motion support
- [ ] Screen reader tested

## Performance Optimization

### Images

1. **Compress all images**
   - JPG: 70-80% quality
   - Use WebP when possible
   - Target: < 200KB per image

2. **Lazy loading**
   - Use `loading="lazy"` attribute
   - Fallback handled in `script.js`

3. **Responsive images** (optional enhancement)
```html
<img 
  srcset="image-480.jpg 480w, image-800.jpg 800w, image-1200.jpg 1200w"
  sizes="(max-width: 768px) 100vw, 50vw"
  src="image-800.jpg"
  alt="Description"
>
```

### CSS

- Critical CSS is inlined (optional future enhancement)
- Use `will-change` sparingly
- Prefer `transform` and `opacity` for animations
- Minimize repaints and reflows

### JavaScript

- Minimal external scripts
- Use `async` or `defer` for scripts
- Intersection Observer for scroll animations
- RequestAnimationFrame for smooth animations

## Testing

### Browser Testing

Test in:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile: iOS Safari, Chrome Android

### Accessibility Testing

Tools:
- **Lighthouse** (Chrome DevTools)
- **axe DevTools** (browser extension)
- **WAVE** (web accessibility evaluation tool)
- **Screen readers**: NVDA (Windows), VoiceOver (Mac)

### Performance Testing

Tools:
- **Lighthouse** (Performance score)
- **PageSpeed Insights**
- **WebPageTest**

Target metrics:
- First Contentful Paint: < 1.5s
- Largest Contentful Paint: < 2.5s
- Time to Interactive: < 3.5s
- Cumulative Layout Shift: < 0.1

## Common Customizations

### Change Colors

Edit CSS variables in `styles.css`:
```css
:root {
    --color-background: #0A0A0A;
    --color-accent-purple: #8B5CF6;
    /* etc... */
}
```

### Add New Section

1. Add HTML in `index.html`:
```html
<section class="new-section" id="new-section">
    <h2>New Section</h2>
    <!-- content -->
</section>
```

2. Add styles in `styles.css`:
```css
.new-section {
    padding: var(--spacing-xl) var(--spacing-md);
    /* styles */
}
```

3. Add nav link in header
4. JavaScript will handle active state automatically

### Modify Animation Duration

All animations use CSS variables:
```css
:root {
    --transition-speed: 0.3s;
}
```

Or target specific elements:
```css
.project-card {
    transition: transform 0.5s ease;
}
```

## Deployment

### GitHub Pages

1. Push to GitHub
2. Go to Settings → Pages
3. Select branch and folder
4. Site will be live at `https://username.github.io/repo-name`

### Netlify

1. Drag and drop the folder
2. Or connect GitHub repo
3. No build command needed
4. Auto-deploys on push

### Vercel

```bash
npx vercel
```

### Traditional Hosting

1. Upload all files via FTP
2. Ensure file permissions are correct
3. Point domain to folder

## SEO Checklist

- [ ] Update all meta tags in `<head>`
- [ ] Add Google Analytics (optional)
- [ ] Create `robots.txt`
- [ ] Create `sitemap.xml`
- [ ] Add Open Graph image (1200x630px)
- [ ] Test with Google Search Console
- [ ] Submit to search engines

## Troubleshooting

### Images not loading
- Check file paths (case-sensitive on Linux servers)
- Verify files exist in `images/` folder
- Check browser console for 404 errors

### Mobile menu not working
- Check browser console for JavaScript errors
- Verify script.js is loading
- Test in different browsers

### Layout issues
- Clear browser cache
- Check CSS is loading
- Validate HTML at validator.w3.org
- Use browser DevTools inspector

## Future Enhancements

Optional improvements:
- [ ] Add contact form functionality
- [ ] Integrate CMS (Netlify CMS, Forestry)
- [ ] Add blog section
- [ ] Create case study pages for projects
- [ ] Add smooth page transitions
- [ ] Implement dark/light mode toggle
- [ ] Add loading animations
- [ ] Create 404 page
- [ ] Add schema.org markup for rich snippets

## Resources

- [MDN Web Docs](https://developer.mozilla.org/)
- [Web.dev](https://web.dev/)
- [A11y Project](https://www.a11yproject.com/)
- [CSS Tricks](https://css-tricks.com/)
- [Can I Use](https://caniuse.com/)

---

**Happy Coding! 🚀**
