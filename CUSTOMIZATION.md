# Customization Guide for Jellyfin-Punk

This guide provides detailed instructions for customizing the Jellyfin-Punk theme to match your preferences.

## Table of Contents
- [Color Customization](#color-customization)
- [Glow Effects](#glow-effects)
- [Typography](#typography)
- [Layout Adjustments](#layout-adjustments)
- [Creating Your Own Variant](#creating-your-own-variant)
- [Advanced Customizations](#advanced-customizations)

## Color Customization

### Basic Color Override

Add this after your theme import to override specific colors:

```css
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/main.css");

:root {
    /* Primary accent colors */
    --accent-cyan: #00ffff !important;
    --accent-magenta: #ff0080 !important;
    --accent-purple: #cc11f0 !important;
    --accent-green: #b0ff00 !important;
    --accent-yellow: #ffdf6b !important;

    /* Background colors */
    --background-primary: #070014 !important;
    --background-secondary: #0a0a1f !important;
    --background-tertiary: #12122e !important;

    /* Text colors */
    --text-primary: #ffffff !important;
    --text-secondary: #b8b8d1 !important;
}
```

### Popular Color Schemes

#### Matrix Green
```css
:root {
    --accent-cyan: #00ff00 !important;
    --accent-magenta: #00ff41 !important;
    --accent-purple: #00ff88 !important;
    --background-primary: #0d0208 !important;
    --background-secondary: #001a00 !important;
}
```

#### Vaporwave
```css
:root {
    --accent-cyan: #ff71ce !important;
    --accent-magenta: #01cdfe !important;
    --accent-purple: #b967ff !important;
    --accent-green: #05ffa1 !important;
    --background-primary: #0a0612 !important;
    --background-secondary: #1a0a2e !important;
}
```

#### Synthwave
```css
:root {
    --accent-cyan: #ff6c11 !important;
    --accent-magenta: #ff0a54 !important;
    --accent-purple: #fe00fe !important;
    --accent-green: #00f0ff !important;
    --background-primary: #0d0221 !important;
    --background-secondary: #0f0f23 !important;
}
```

#### Blade Runner
```css
:root {
    --accent-cyan: #ff9e00 !important;
    --accent-magenta: #ff3864 !important;
    --accent-purple: #9f00ff !important;
    --background-primary: #0a0a0a !important;
    --background-secondary: #1a1a1a !important;
}
```

## Glow Effects

### Adjust Glow Intensity

#### Subtle Glow (Better Performance)
```css
:root {
    --glow-intensity: 8px !important;
    --glow-cyan: 0 0 5px var(--accent-cyan), 0 0 10px var(--accent-cyan) !important;
    --glow-magenta: 0 0 5px var(--accent-magenta), 0 0 10px var(--accent-magenta) !important;
    --glow-purple: 0 0 5px var(--accent-purple), 0 0 10px var(--accent-purple) !important;
}
```

#### Intense Glow
```css
:root {
    --glow-intensity: 25px !important;
    --glow-cyan: 0 0 15px var(--accent-cyan), 0 0 30px var(--accent-cyan), 0 0 45px var(--accent-cyan) !important;
    --glow-magenta: 0 0 15px var(--accent-magenta), 0 0 30px var(--accent-magenta), 0 0 45px var(--accent-magenta) !important;
    --glow-purple: 0 0 15px var(--accent-purple), 0 0 30px var(--accent-purple), 0 0 45px var(--accent-purple) !important;
}
```

#### Disable Glows Completely
```css
:root {
    --glow-cyan: none !important;
    --glow-magenta: none !important;
    --glow-purple: none !important;
}

.card:hover,
.cardBox:hover,
.itemDetailImage {
    box-shadow: none !important;
}
```

### Custom Glow Colors

```css
.card:hover {
    box-shadow: 0 0 20px #your-color, 0 0 40px #your-color !important;
}

.button-flat:hover {
    box-shadow: 0 0 15px #your-color !important;
}
```

## Typography

### Change Font Family

```css
body {
    font-family: "Your Font Name", sans-serif !important;
}

/* For headings */
h1, h2, h3, h4, h5, h6,
.sectionTitle {
    font-family: "Your Heading Font", sans-serif !important;
}
```

### Popular Font Combinations

#### Futuristic
```css
@import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Rajdhani:wght@300;400;600&display=swap');

body {
    font-family: "Rajdhani", sans-serif !important;
}

h1, h2, h3, h4, h5, h6,
.sectionTitle {
    font-family: "Orbitron", sans-serif !important;
}
```

#### Cyberpunk
```css
@import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=Electrolize&display=swap');

body {
    font-family: "Electrolize", sans-serif !important;
}

h1, h2, h3, h4, h5, h6 {
    font-family: "Share Tech Mono", monospace !important;
}
```

### Adjust Font Sizes

```css
:root {
    --font-size-small: 12px;
    --font-size-normal: 14px;
    --font-size-large: 18px;
    --font-size-xlarge: 24px;
}

body {
    font-size: var(--font-size-normal) !important;
}

.sectionTitle {
    font-size: var(--font-size-xlarge) !important;
}
```

## Layout Adjustments

### Card Spacing

```css
.card,
.cardBox {
    margin: 15px !important; /* Increase spacing between cards */
}
```

### Border Radius

```css
:root {
    --border-radius-sm: 2px !important;
    --border-radius-md: 6px !important;
    --border-radius-lg: 10px !important;
}

/* Or make everything rounded */
.card,
.cardBox,
.emby-input,
.button-flat {
    border-radius: 20px !important;
}
```

### Card Hover Effects

#### Disable Hover Animations
```css
.card:hover,
.cardBox:hover {
    transform: none !important;
}
```

#### Stronger Hover Effect
```css
.card:hover,
.cardBox:hover {
    transform: translateY(-10px) scale(1.08) !important;
}
```

### Navigation Bar

#### Transparent Header
```css
.skinHeader {
    background: rgba(7, 0, 20, 0.7) !important;
    backdrop-filter: blur(15px) !important;
}
```

#### Solid Header
```css
.skinHeader {
    background: var(--background-primary) !important;
    backdrop-filter: none !important;
}
```

## Creating Your Own Variant

To create a custom color variant:

1. Choose your color palette
2. Create a new CSS file with your colors
3. Import it after the main theme

### Example: "Arctic Blue" Variant

Create a file named `arctic-blue.css`:

```css
/**
 * Arctic Blue Variant
 */
:root {
    --accent-cyan: #00d9ff !important;
    --accent-magenta: #0099cc !important;
    --accent-purple: #006699 !important;
    --accent-green: #00ffcc !important;
    --accent-yellow: #66ffff !important;

    --background-primary: #000a14 !important;
    --background-secondary: #001428 !important;
    --background-tertiary: #001e3c !important;
    --background-elevated: #002850 !important;

    --text-primary: #e0f7ff !important;
    --text-secondary: #b0d9f0 !important;
}

.skinHeader {
    border-bottom-color: #00d9ff !important;
}

.card:hover,
.cardBox:hover {
    border-color: #00d9ff !important;
}
```

Then import it:
```css
@import url("path/to/main.css");
@import url("path/to/arctic-blue.css");
```

## Advanced Customizations

### Background Patterns

#### Grid Pattern
```css
body::before {
    content: "" !important;
    position: fixed !important;
    top: 0 !important;
    left: 0 !important;
    width: 100% !important;
    height: 100% !important;
    pointer-events: none !important;
    z-index: 1 !important;
    background-image:
        linear-gradient(rgba(0, 255, 255, 0.1) 1px, transparent 1px),
        linear-gradient(90deg, rgba(0, 255, 255, 0.1) 1px, transparent 1px) !important;
    background-size: 50px 50px !important;
}
```

#### Diagonal Lines
```css
body::before {
    content: "" !important;
    position: fixed !important;
    top: 0 !important;
    left: 0 !important;
    width: 100% !important;
    height: 100% !important;
    pointer-events: none !important;
    z-index: 1 !important;
    background-image: repeating-linear-gradient(
        45deg,
        transparent,
        transparent 10px,
        rgba(0, 255, 255, 0.05) 10px,
        rgba(0, 255, 255, 0.05) 20px
    ) !important;
}
```

### Custom Button Styles

#### Outlined Buttons
```css
.button-flat,
.raised {
    background: transparent !important;
    border: 2px solid var(--accent-cyan) !important;
    color: var(--accent-cyan) !important;
}

.button-flat:hover,
.raised:hover {
    background: var(--accent-cyan) !important;
    color: var(--background-primary) !important;
}
```

#### Gradient Buttons with Animation
```css
.button-flat,
.raised {
    background: linear-gradient(
        135deg,
        var(--accent-cyan) 0%,
        var(--accent-magenta) 50%,
        var(--accent-purple) 100%
    ) !important;
    background-size: 200% 200% !important;
    animation: gradientShift 3s ease infinite !important;
}

@keyframes gradientShift {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
}
```

### Animated Backgrounds

#### Particle Effect
```css
body::after {
    content: "" !important;
    position: fixed !important;
    width: 100% !important;
    height: 100% !important;
    background-image:
        radial-gradient(2px 2px at 20% 30%, var(--accent-cyan), transparent),
        radial-gradient(2px 2px at 60% 70%, var(--accent-magenta), transparent),
        radial-gradient(1px 1px at 50% 50%, var(--accent-purple), transparent) !important;
    background-size: 200% 200% !important;
    animation: particleFloat 20s ease-in-out infinite !important;
    pointer-events: none !important;
    opacity: 0.3 !important;
}

@keyframes particleFloat {
    0%, 100% { transform: translate(0, 0); }
    33% { transform: translate(30px, -30px); }
    66% { transform: translate(-20px, 20px); }
}
```

### Custom Scrollbar Styles

#### Minimalist Scrollbar
```css
::-webkit-scrollbar {
    width: 8px !important;
}

::-webkit-scrollbar-track {
    background: transparent !important;
}

::-webkit-scrollbar-thumb {
    background: var(--accent-cyan) !important;
    border-radius: 10px !important;
}
```

#### Glowing Scrollbar
```css
::-webkit-scrollbar-thumb {
    background: linear-gradient(var(--accent-cyan), var(--accent-magenta)) !important;
    box-shadow: 0 0 10px var(--accent-cyan) !important;
}

::-webkit-scrollbar-thumb:hover {
    box-shadow: 0 0 20px var(--accent-cyan), 0 0 30px var(--accent-magenta) !important;
}
```

## Performance Tips

### Optimize for Lower-End Devices

```css
/* Disable animations */
* {
    animation: none !important;
}

/* Simplify transitions */
* {
    transition: none !important;
}

/* Reduce glow effects */
:root {
    --glow-cyan: none !important;
    --glow-magenta: none !important;
    --glow-purple: none !important;
}

/* Disable backdrop filters */
.skinHeader,
.nowPlayingBar {
    backdrop-filter: none !important;
}
```

### Mobile-Specific Customizations

```css
@media (max-width: 768px) {
    /* Larger touch targets */
    .button-flat,
    .paper-icon-button-light {
        min-width: 44px !important;
        min-height: 44px !important;
    }

    /* Simplified effects */
    .card:hover {
        transform: none !important;
        box-shadow: none !important;
    }

    /* Larger fonts */
    body {
        font-size: 16px !important;
    }
}
```

## Testing Your Customizations

1. **Use Browser DevTools**: Press F12 to inspect elements and test CSS changes live
2. **Test on Multiple Devices**: Check desktop, mobile, and tablet views
3. **Check Different Pages**: Test home, library, detail pages, and settings
4. **Verify Performance**: Use browser performance tools to check for slowdowns

## Sharing Your Customization

If you've created a great customization:

1. Create a new CSS file with your changes
2. Add documentation explaining what it does
3. Share on GitHub or Jellyfin forums
4. Consider submitting a pull request to add it as an official variant

## Need Help?

- **CSS Basics**: [MDN CSS Guide](https://developer.mozilla.org/en-US/docs/Web/CSS)
- **Color Tools**: [Coolors.co](https://coolors.co/), [Adobe Color](https://color.adobe.com/)
- **Font Pairing**: [Google Fonts](https://fonts.google.com/)
- **Ask the Community**: [Jellyfin Forums](https://forum.jellyfin.org/)

---

**Have you created an awesome customization?** Share it with the community!
