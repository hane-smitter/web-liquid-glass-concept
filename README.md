# Liquid Glass

A sophisticated glassmorphism effect demonstrating advanced CSS and SVG filters to create a viscous, liquid glass backdrop with interactive features.

## Overview

This project showcases a modern web design technique that combines:
- **SVG Filters**: Complex color packing/unpacking and displacement mapping
- **CSS Backdrop Filters**: Real-time background blur and glass effects
- **Advanced Blending**: Multiple blend modes and composite operations

The centerpiece is an animated header with a liquid glass effect that distorts the background, creating a dynamic, organic appearance.

## Features

### Visual Effects
- **Liquid Glass Backdrop**: Sophisticated SVG-based glass effect with color channel encoding
- **Fresnel Lighting**: Simulates light refraction on curved surfaces
- **Displacement Mapping**: Real-time distortion of background elements
- **Animated Background**: Smooth vertical parallax animation
- **Drop Shadows**: Subtle depth enhancement

### Technical Highlights
- **7-bit Color Packing**: Encodes multiple data channels in color values for advanced filtering
- **Normal Mapping**: Creates surface-like lighting effects
- **Component Transfer**: Customized color manipulation and quantization
- **Morphology Filters**: Edge detection and thickness control

## Technologies

- **HTML5**: Semantic markup with embedded SVG filters
- **CSS3**: 
  - Grid layout system
  - Backdrop filters
  - Custom animations and transitions
  - CSS variables for styling
- **SVG**: 
  - Filter effects (feComponentTransfer, feGaussianBlur, etc.)
  - Displacement mapping
  - Diffuse lighting simulation
  - Shape definitions for icons

## Getting Started

1. Clone or download this repository
2. Open `index.html` in a modern web browser
3. Interact with the navigation and theme toggle to see effects in action

### Browser Support

Requires modern browser support for:
- CSS Grid
- Backdrop filters
- SVG filters
- CSS animations

> **Tested on**: _Chrome Version 144.0.7559.132 (Official Build) (64-bit)_. Test on _firefox 147.0.3 (64-bit)_ **failed** due to lack of support for `backdrop-filter: url(...)` syntax.

## Key SVG Filters

### `liquid-glass-new`
The main effect filter featuring:
- Background unpacking (7-bit color channels)
- Diffuse lighting from multiple angles
- Normal map generation
- Displacement mapping for refraction
- Fresnel-like edge lighting

### `fresnel`
Adds edge highlights and outline effects to enhance the glass appearance.

### Supporting Filters
- `pack-lower` / `pack-upper`: Color channel encoding
- `unpack-lower` / `unpack-upper`: Color channel decoding
- `glass`: Simpler glass effect alternative
- `round`: Gaussian blur with alpha adjustments

## Customization

### Colors
Modify the SVG filter color matrices to change the glass effect appearance:
- Red, green, yellow, and black sides can be adjusted
- Flood colors control normal map background

### Animation Speed
Adjust the background animation in CSS:
```css
animation: bg-move 20s ease-in-out infinite alternate;
```

### Glass Intensity
Control displacement scale in the SVG:
```html
<feDisplacementMap scale="100" ... />
```

### Background Image
Replace the background URL in `styles.css`:
```css
background-image: url("your-image-url");
```

## Credits

- **Concept**: Liquid glass/glassmorphism design pattern
- **SVG Techniques**: Color packing/unpacking from [Cubiq pen](https://codepen.io/Cubiq/pen/yyYYRzP)
- **Icons**: Lucide icons integration
- **Typography**: Manrope font from Google Fonts

## Performance Notes

- SVG filters are computationally intensive
- Use in modern browsers for best performance
- Consider reducing filter complexity on lower-end devices
- Backdrop filters may have performance impact on some systems

## Future Enhancements

- Add animation controllers for interactive filter adjustment
- Implement mouse-following parallax effects
- Create variations with different glass qualities
- Add theme presets with different color schemes
- Optimize SVG filter performance
