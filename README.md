# Jellyfin-Punk 🌆

A high-quality CyberPunk-themed CSS customization for Jellyfin with neon aesthetics and modern UI/UX design.

![Theme Preview](https://img.shields.io/badge/Status-Beta-cyan?style=for-the-badge)
![CSS](https://img.shields.io/badge/CSS-100%25-ff0080?style=for-the-badge)

## ✨ Features

- **Neon CyberPunk Aesthetics**: Electric cyan, hot magenta, and neon purple color scheme
- **Glowing Effects**: Beautiful neon glow on buttons, cards, and interactive elements
- **Dark Mode Optimized**: Deep black background with high contrast for comfortable viewing
- **Scanline Effects**: Optional retro-futuristic scanline overlay
- **Modern UI/UX**: Smooth animations and transitions throughout
- **Responsive Design**: Works seamlessly across desktop, mobile, and TV apps
- **Logo Support**: Enhanced media logos with neon glow effects
- **Multiple Color Variants**: Choose from different CyberPunk color schemes

## 🚀 Quick Start

### Requirements

Jellyfin-Punk requires:
- **Jellyfin** 10.8.0 or newer
- **Browsers**: Chrome 105+, Edge 105+, Safari 15.4+, Firefox 121+, Opera 91+
- Any browser supporting Baseline 23 CSS features

### Installation

1. **Navigate to Jellyfin Dashboard**
   - Go to `Dashboard → General → Custom CSS`

2. **Copy and paste the following line:**

```css
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/main.css");
```

3. **Click Save** - The theme will apply immediately server-wide!

### Optional Enhancements

#### Enable Logo Support
Add neon glow effects to media logos:

```css
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/logo.css");
```

#### Enable Scanline Effect
Add retro CRT scanline overlay:

```css
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/addons/scanlines.css");
```

#### Color Variants

Choose from alternative color schemes:

**Purple Haze** (Purple/Violet dominant):
```css
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/variants/purple-haze.css");
```

**Neon Nights** (Cyan/Blue dominant):
```css
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/variants/neon-nights.css");
```

**Tokyo Drift** (Magenta/Pink dominant):
```css
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/variants/tokyo-drift.css");
```

## 🎨 Color Palette

The default theme uses the following color scheme:

| Color | Hex Code | Usage |
|-------|----------|-------|
| Deep Black | `#070014` | Primary background |
| Midnight Blue | `#0a0a1f` | Secondary background |
| Electric Cyan | `#00ffff` | Primary accent |
| Hot Magenta | `#ff0080` | Secondary accent |
| Neon Purple | `#cc11f0` | Tertiary accent |
| Acid Green | `#b0ff00` | Success/highlight |
| Neon Yellow | `#ffdf6b` | Warning/info |

## 🔧 Customization

You can customize the theme by overriding CSS variables. Add this after the main import:

```css
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/main.css");

:root {
    --accent-cyan: #00ffff;
    --accent-magenta: #ff0080;
    --accent-purple: #cc11f0;
    --glow-intensity: 15px;
    --background-primary: #070014;
}
```

## 🐛 Known Issues

### Nginx Reverse Proxy
If using Nginx as a reverse proxy, you may need to update your Content-Security-Policy headers:

```nginx
add_header Content-Security-Policy "style-src 'self' 'unsafe-inline' cdn.jsdelivr.net;";
```

### Performance
- Glowing effects use CSS filters which may impact performance on older devices
- Consider disabling scanlines on lower-end hardware
- Logo effects require proper metadata from Fanart

## 📸 Screenshots

Screenshots coming soon!

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Share your customizations

## 📜 License

MIT License - Feel free to use and modify as you wish!

## 🙏 Credits

Inspired by:
- [JellySkin](https://github.com/prayag17/JellySkin)
- [JellyFlix](https://github.com/prayag17/JellyFlix)
- [Scyfin](https://github.com/loof2736/scyfin)

Color palettes sourced from:
- [ColorMagic](https://colormagic.app/palette/explore/cyberpunk)
- [ColorsWall](https://colorswall.com/palette/549002)
- [DepositPhotos Blog](https://blog.depositphotos.com/15-cyberpunk-color-palettes-for-dystopian-designs.html)

Free SVG assets from:
- [Vecteezy](https://www.vecteezy.com/free-vector/cyberpunk)
- [SVG Repo](https://www.svgrepo.com/vectors/cyberpunk/)
- [Flaticon](https://www.flaticon.com/packs/cyberpunk-11)

## ⭐ Support

If you enjoy this theme, please consider:
- Starring the repository
- Sharing with the Jellyfin community
- [Buying me a coffee](https://buymeacoffee.com/your-username)

---

Made with 💜 for the Jellyfin community
