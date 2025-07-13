# Beautiful Custom Scrollbars 🎨

A collection of stunning, ready-to-use custom scrollbar styles for modern web projects.

## Features

- 8+ unique scrollbar designs
- Works on WebKit browsers (Chrome, Safari, Edge)
- Basic Firefox support where possible
- Easy to implement
- Fully customizable

## Installation

### By cloning Github repo
1. Clone the repository:
```bash
git clone https://github.com/Clementabcd/Beautiful-Custom-Scrollbars.git
```

2. Link the desired CSS file in your HTML:
```html
<link rel="stylesheet" href="path/to/styles/liquid-glass.css">
```

### Via CDN (jsDelivr)
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/Clementabcd/Beautiful-Custom-Scrollbars@main/styles/liquid-glass.css">
```

## Available Styles

| Style | Preview | Description |
|-------|---------|-------------|
| [Liquid Glass](styles/liquid-glass.css) | ![Preview] | Translucent, frosted glass effect |
| [Aurora Borealis](styles/aurora-borealis.css) | ![Preview] | Color-shifting gradient animation |
| [Marble Vein](styles/marble-vein.css) | ![Preview] | Elegant marble texture effect |
| [Cyberpunk Neon](styles/cyberpunk-neon.css) | ![Preview] | Retro-futuristic neon style |
| [Nature Moss](styles/nature-moss.css) | ![Preview] | Organic green tones |
| [Galaxy Swirl](styles/galaxy-swirl.css) | ![Preview] | Deep space cosmic effect |
| [Golden Luxury](styles/golden-luxury.css) | ![Preview] | Luxurious gold accents |
| [Minimal Glass](styles/minimal-glass.css) | ![Preview] | Ultra-clean subtle design |

## Browser Compatibility

| Feature           | Chrome | Firefox | Safari | Edge |
|-------------------|--------|---------|--------|------|
| Basic Styles      | ✅     | ✅      | ✅     | ✅   |
| Blur Effects      | ✅     | ❌      | ✅     | ✅   |
| Animations        | ✅     | ❌      | ✅     | ✅   |
| SVG Backgrounds   | ✅     | ✅      | ✅     | ✅   |

## Customization Guide

All scrollbar styles can be easily customized by editing these common properties:

### **Basic Customization**
```css
::-webkit-scrollbar {
  width: 10px; /* Change thickness */
  height: 10px; /* For horizontal scrollbars */
}
```

### **Color Customization**
```css
::-webkit-scrollbar-thumb {
  background: #yourcolor; /* Solid color */
  background: linear-gradient(...); /* Gradient */
}
```

### **Advanced Effects**
- **Glass Effect**: Adjust `backdrop-filter: blur(Xpx)` and opacity
- **Animations**: Modify `@keyframes` duration or colors
- **Borders**: Change `border` thickness/color
- **Shadows**: Edit `box-shadow` values

### **Firefox Support**
For each style, modify these Firefox-specific properties:
```css
html {
  scrollbar-width: thin | auto | none;
  scrollbar-color: thumb-color track-color;
}
```

## Framework Integration

### React Component
```jsx
import React, { useEffect } from 'react';
import './styles/liquid-glass.css';

const ScrollableComponent = () => {
  useEffect(() => {
    document.documentElement.style.setProperty('--scrollbar-width', '12px');
  }, []);

  return (
    <div className="overflow-y-auto">
      {/* Your content */}
    </div>
  );
};
```

### Vue Directive
```javascript
import './styles/liquid-glass.css';

export default {
  directives: {
    scrollbar: {
      mounted(el) {
        el.classList.add('custom-scrollbar');
      }
    }
  }
}
```

### **Recommended Workflow**
1. Pick a base style from the collection
2. Copy it to your project's CSS
3. Adjust colors to match your brand
4. Test on different backgrounds
5. Fine-tune animation speeds if needed

## Contributing

Found a bug or want to add another beautiful style?

1. Fork the repository
2. Create a new branch (`git checkout -b new-scrollbar-style`)
3. Add your style in the `styles/` directory
4. Include Firefox support if possible
5. Submit a pull request

## License

MIT License - Free for personal and commercial use
