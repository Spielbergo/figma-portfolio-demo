# Dezign Portfolio Website

A pixel-perfect, responsive portfolio website built with vanilla HTML, CSS, and JavaScript. Features a modern dark theme, smooth animations, and comprehensive accessibility support.

## ✨ Features

- **Pixel-Perfect Design**: Faithfully recreated from Figma design
- **Mobile-First**: Responsive design that works on all devices
- **Accessibility**: WCAG 2.1 compliant with full keyboard navigation
- **SEO Optimized**: Complete meta tags for search engines and social media
- **Smooth Animations**: Intersection Observer API for performant scroll animations
- **Mobile Navigation**: Sliding menu from the right with focus trapping
- **Zero Dependencies**: Pure vanilla JavaScript, no frameworks needed

## 🎨 Design Features

- Dark theme with purple accent colors
- Smooth scroll navigation
- Animated project cards
- Responsive grid layouts
- Custom hamburger menu animation
- Hover effects and transitions

## 📱 Responsive Breakpoints

- **Mobile**: 320px - 767px
- **Tablet**: 768px - 1023px
- **Desktop**: 1024px+

## ♿ Accessibility Features

- Semantic HTML5 elements
- ARIA labels and roles
- Skip to main content link
- Keyboard navigation support
- Focus visible indicators
- Screen reader friendly
- Reduced motion support
- High contrast mode support
- Focus trap in mobile menu

## 🔍 SEO Features

- Complete meta tags
- Open Graph tags for Facebook
- Twitter Card tags
- Semantic heading hierarchy
- Alt text for images
- Canonical URL
- Mobile-friendly viewport

## 📁 Project Structure

```
figma-portfolio-wp/
├── index.html          # Main HTML file
├── styles.css          # All styles (mobile-first)
├── script.js           # Interactive functionality
├── README.md           # Project documentation
├── .gitignore          # Git ignore file
└── images/             # Image assets folder
    ├── airbnb-logo.svg
    ├── google-logo.svg
    ├── microsoft-logo.svg
    ├── fedex-logo.svg
    ├── project-real-estate.jpg
    ├── project-plant-app.jpg
    ├── project-smart-home.jpg
    ├── project-logo-animation.jpg
    ├── about-1.jpg
    ├── about-2.jpg
    ├── about-3.jpg
    └── about-4.jpg
```

## 🚀 Getting Started

1. **Clone or download** this repository
2. **Add your images** to the `images/` folder
3. **Update content** in `index.html` with your information
4. **Customize colors** in `styles.css` (CSS variables in `:root`)
5. **Open** `index.html` in a browser

### Quick Start

Simply open `index.html` in your browser - no build process needed!

```bash
# If you want to use a local server (recommended)
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js (with npx)
npx serve

# Then visit http://localhost:8000
```

## 🎨 Customization

### Colors

Edit CSS variables in `styles.css`:

```css
:root {
    --color-background: #0A0A0A;
    --color-text-primary: #FFFFFF;
    --color-text-secondary: #999999;
    --color-accent-purple: #8B5CF6;
    --color-accent-green: #86EFAC;
}
```

### Typography

The project uses Inter font from Google Fonts. To change:

```html
<!-- In index.html, update the Google Fonts link -->
<link href="https://fonts.googleapis.com/css2?family=YourFont:wght@300;400;600;700&display=swap" rel="stylesheet">
```

```css
/* In styles.css, update the font family */
--font-family: 'YourFont', sans-serif;
```

### Content

- Update text content directly in `index.html`
- Replace placeholder images in the `images/` folder
- Update social media links in the contact section
- Modify meta tags for SEO

## 📝 Image Requirements

### Client Logos
- Format: SVG (recommended) or PNG
- Size: ~150px width
- Background: Transparent

### Project Images
- Format: JPG or WebP
- Aspect Ratio: 16:10
- Recommended Size: 1600x1000px
- Optimize for web (< 200KB per image)

### About Images
- Format: JPG or WebP
- Size: 800x800px minimum
- Optimize for web (< 150KB per image)

## 🌐 Browser Support

- Chrome (last 2 versions)
- Firefox (last 2 versions)
- Safari (last 2 versions)
- Edge (last 2 versions)
- Mobile browsers (iOS Safari, Chrome Android)

## ⚡ Performance

- Lazy loading images
- Minimal JavaScript
- Optimized animations
- No external dependencies
- Mobile-first CSS

## 📄 License

This project is open source and available for personal and commercial use.

## 🤝 Contributing

Feel free to submit issues and enhancement requests!

## 📞 Contact

Update the contact section in `index.html` with your:
- Email address
- Behance profile
- Instagram profile
- LinkedIn profile

---

**Built with ❤️ using Vanilla HTML, CSS, and JavaScript**
