# Jellyfin-Punk 🌆

A minimal and clean CyberPunk-themed CSS customization for Jellyfin. Built on the proven foundation of [Ultrachromic](https://github.com/CTalvio/Ultrachromic), Jellyfin-Punk adds subtle cyberpunk aesthetics without overwhelming effects or breaking the UI.

![Theme Preview](https://img.shields.io/badge/Status-Stable-cyan?style=for-the-badge)
![CSS](https://img.shields.io/badge/CSS-Modular-ff0080?style=for-the-badge)

## ✨ Features

- **Three CyberPunk Variants**: Blue & Yellow, Dark Purple & Magenta, Monochrome with Cyan
- **Minimal & Clean**: Subtle accents that enhance rather than overwhelm
- **Built on Ultrachromic**: Uses proven, stable base that respects Jellyfin's UI
- **Fully Modular**: Mix and match components to create your perfect theme
- **No UI Breaking**: Images stay visible, text stays readable, everything just works
- **Responsive Design**: Works seamlessly across desktop, mobile, and TV apps

## 🚀 Quick Start

### Requirements

- **Jellyfin** 10.8.0 or newer
- **Browsers**: Chrome 105+, Edge 105+, Safari 15.4+, Firefox 121+, Opera 91+

### Single Line Presets

These let you use Jellyfin-Punk with one line of CSS. Choose your favorite variant:

#### Blue Preset (Electric Blue & Neon Yellow)
Classic cyberpunk aesthetic inspired by Blade Runner.

```css
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/presets/blue_preset.css');
```

#### Dark Preset (Deep Purple & Magenta)
Darker, more intense cyberpunk with rich purple tones.

```css
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/presets/dark_preset.css');
```

#### Mono Preset (Black & White with Cyan)
Minimalist cyberpunk with monochrome palette and subtle cyan accents.

```css
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/presets/mono_preset.css');
```

## 🎨 Color Palettes

### Blue Variant
| Element | Color | Hex Code |
|---------|-------|----------|
| Primary Accent | Electric Blue | `#00a4dc` |
| Secondary Accent | Neon Yellow | `#ffd700` |
| Background | Deep Blue-Black | `#0a0a15` |

### Dark Variant
| Element | Color | Hex Code |
|---------|-------|----------|
| Primary Accent | Deep Purple | `#8b00ff` |
| Secondary Accent | Hot Pink | `#e6007a` |
| Background | Deep Purple-Black | `#0a0015` |

### Mono Variant
| Element | Color | Hex Code |
|---------|-------|----------|
| Primary Accent | Light Gray | `#c8c8c8` |
| Secondary Accent | Subtle Cyan | `#00cccc` |
| Background | True Black | `#000000` |

## 🔧 Customization Using Multiple Import Lines

Jellyfin-Punk is composed of multiple "parts" allowing you to theme only what you want. Simply add imports in order. Omit options you don't want.

### 1. Recommended

`fixes.css` contains various small UI tweaks and alignments from Ultrachromic.

```css
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/fixes.css');
```

### 2. Required

These lines are required for the theme to work.

```css
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/base.css');
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/accentlist.css');
```

### 3. Choose Type (Required)

You must use one of these. Each provides a different cyberpunk aesthetic.

**Blue & Yellow** (Classic cyberpunk):
```css
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/type/cyberpunk_blue.css');
```

**Dark Purple & Magenta** (Intense cyberpunk):
```css
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/type/cyberpunk_dark.css');
```

**Black & White with Cyan** (Minimalist cyberpunk):
```css
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/type/cyberpunk_mono.css');
```

### 4. Manual Options

Add this after the imports to customize rounding and backdrop styling:

```css
/*Rounding*/
:root {--rounding: 4px;}

/*Style backdrop*/
.backdropImage {
  filter: blur(18px) saturate(110%) contrast(110%) brightness(35%);
}

/*Custom accent (optional)*/
:root {--accent: 0, 255, 255;} /* Custom cyan: #00ffff */
```

## 📖 Example Combinations

### Minimal Blue Setup
```css
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/fixes.css');
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/base.css');
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/accentlist.css');
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/type/cyberpunk_blue.css');
```

### Dark with Custom Rounding
```css
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/fixes.css');
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/base.css');
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/accentlist.css');
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/type/cyberpunk_dark.css');

:root {--rounding: 8px;}
```

## 🐛 Known Issues

### Nginx Reverse Proxy

When using the Nginx reverse proxy config from the [Jellyfin docs](https://jellyfin.org/docs/general/networking/nginx.html), you need to add the theme URLs to Content-Security-Policy:

```nginx
add_header Content-Security-Policy "default-src https: data: blob:; style-src 'self' 'unsafe-inline' https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/; script-src 'self' 'unsafe-inline' https://www.gstatic.com/cv/js/sender/v1/cast_sender.js worker-src 'self' blob:; connect-src 'self'; object-src 'none'; frame-ancestors 'self'";
```

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new color variants
- Submit pull requests
- Share your customizations

## 📜 License

MIT License - Feel free to use and modify as you wish!

## 🙏 Credits

**Built on:**
- [Ultrachromic](https://github.com/CTalvio/Ultrachromic) by CTalvio - The proven, stable base theme

**Inspired by:**
- [JellySkin](https://github.com/prayag17/JellySkin) by prayag17
- [JellyFlix](https://github.com/prayag17/JellyFlix) by prayag17
- [Scyfin](https://github.com/loof2736/scyfin) by loof2736

**Color Research:**
- [ColorMagic](https://colormagic.app/palette/explore/cyberpunk)
- [ColorsWall](https://colorswall.com/palette/549002)
- [DepositPhotos](https://blog.depositphotos.com/15-cyberpunk-color-palettes-for-dystopian-designs.html)

## ⭐ Support

If you enjoy this theme, please consider:
- Starring the repository ⭐
- Sharing with the Jellyfin community
- Contributing improvements

---

Made with 💜 for the Jellyfin community
