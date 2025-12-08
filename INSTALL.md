# Installation Guide for Jellyfin-Punk Theme

This guide will walk you through installing and customizing the Jellyfin-Punk theme for your Jellyfin server.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation Methods](#installation-methods)
- [Configuration Options](#configuration-options)
- [Troubleshooting](#troubleshooting)

## Prerequisites

Before installing the theme, ensure you have:

1. **Jellyfin Server** version 10.8.0 or newer
2. **Admin access** to your Jellyfin dashboard
3. **Compatible browser**:
   - Chrome/Edge 105+
   - Safari 15.4+
   - Firefox 121+
   - Opera 91+

## Installation Methods

### Method 1: Using CDN (Recommended)

This is the easiest method and ensures you always have access to updates.

1. **Log in to Jellyfin** as an administrator
2. Navigate to **Dashboard → General**
3. Scroll down to the **Custom CSS** section
4. Copy and paste the following code:

```css
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/main.css");
```

5. Click **Save**
6. Refresh your browser to see the changes

### Method 2: Using GitHub Pages

If you fork this repository and enable GitHub Pages:

1. Fork this repository to your GitHub account
2. Enable GitHub Pages in repository settings
3. Use the following import in Custom CSS:

```css
@import url("https://YOUR-USERNAME.github.io/jellyfin-punk/dist/main.css");
```

### Method 3: Local Installation

For offline or development use:

1. Download the repository
2. Copy the contents of `dist/main.css`
3. Paste the entire CSS directly into the Custom CSS field
4. Click Save

**Note**: This method requires manual updates when new versions are released.

## Configuration Options

### Basic Setup (Core Theme Only)

```css
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/main.css");
```

### Full Setup (With All Features)

```css
/* Main theme */
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/main.css");

/* Logo enhancements */
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/logo.css");

/* Scanline effect */
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/addons/scanlines.css");
```

### Color Variants

Choose ONE of the following variants (optional):

#### Purple Haze (Purple/Violet theme)
```css
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/main.css");
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/variants/purple-haze.css");
```

#### Neon Nights (Cyan/Blue theme)
```css
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/main.css");
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/variants/neon-nights.css");
```

#### Tokyo Drift (Magenta/Pink theme)
```css
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/main.css");
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/variants/tokyo-drift.css");
```

### Custom Color Configuration

You can override specific colors by adding this AFTER the imports:

```css
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@main/dist/main.css");

/* Custom color overrides */
:root {
    --accent-cyan: #your-color !important;
    --accent-magenta: #your-color !important;
    --accent-purple: #your-color !important;
    --background-primary: #your-color !important;
    --glow-intensity: 20px !important;
}
```

## Advanced Configuration

### Disable Specific Features

#### Reduce Glow Intensity (Better for performance)
```css
:root {
    --glow-intensity: 5px !important;
}

.card:hover,
.cardBox:hover {
    box-shadow: none !important;
}
```

#### Disable Animations (Better for accessibility)
```css
* {
    animation: none !important;
    transition: none !important;
}
```

#### Simplify Scrollbars (Better for performance)
```css
::-webkit-scrollbar-thumb {
    background: #00ffff !important;
    box-shadow: none !important;
}
```

## Nginx Reverse Proxy Configuration

If you're using Nginx as a reverse proxy and the theme doesn't load, add this to your Nginx configuration:

```nginx
location / {
    # ... your existing config ...

    # Allow external CSS imports
    add_header Content-Security-Policy "default-src 'self'; style-src 'self' 'unsafe-inline' cdn.jsdelivr.net *.github.io; script-src 'self' 'unsafe-inline'; img-src 'self' data: https:; font-src 'self' data:; connect-src 'self'; media-src 'self' blob:; object-src 'none'; frame-ancestors 'self';" always;
}
```

Then restart Nginx:
```bash
sudo systemctl restart nginx
```

## Troubleshooting

### Theme Not Loading

1. **Check browser console** (F12) for errors
2. **Verify the URL** is accessible in a new browser tab
3. **Clear browser cache** (Ctrl+Shift+Delete)
4. **Try a different browser** to rule out compatibility issues

### Theme Looks Broken

1. **Clear Jellyfin cache**:
   - Dashboard → Advanced → Clear Cache
2. **Check for conflicting CSS**:
   - Remove any other custom CSS temporarily
3. **Verify import order**:
   - Main theme should always be imported first
   - Variants come after main.css

### Performance Issues

1. **Disable scanlines addon** if enabled
2. **Reduce glow intensity** using custom CSS
3. **Disable animations** on lower-end devices
4. **Use simplified configuration** without logo.css

### Logo Enhancements Not Working

1. **Verify Fanart metadata** is enabled:
   - Dashboard → Plugins → Fanart
2. **Refresh metadata** for your media:
   - Right-click media → Refresh Metadata
3. **Check if logos exist** in your media folder

### Colors Look Different

1. **Check color variant imports** - only use one variant
2. **Verify import order** - variants must come after main.css
3. **Check for custom overrides** that might conflict

### Mobile Issues

1. **Update your app** to the latest version
2. **Clear app cache** in app settings
3. **Try web browser** on mobile as alternative
4. **Disable performance-heavy features** like scanlines

## Version Pinning

To prevent automatic updates, pin to a specific version:

```css
/* Instead of @main, use a specific version tag */
@import url("https://cdn.jsdelivr.net/gh/YOUR-USERNAME/jellyfin-punk@v1.0.0/dist/main.css");
```

Replace `v1.0.0` with the desired version number.

## Updating the Theme

### If using CDN with @main
Themes update automatically. Clear browser cache to see changes immediately.

### If using version pinning
1. Check for new releases on GitHub
2. Update version number in your import URL
3. Clear browser cache

### If using local installation
1. Download new version
2. Copy contents of new `dist/main.css`
3. Replace old CSS in Custom CSS field
4. Save and refresh

## Getting Help

If you encounter issues not covered here:

1. **Check the Issues page** on GitHub
2. **Search Jellyfin forums** for similar problems
3. **Create a new issue** with:
   - Jellyfin version
   - Browser and version
   - Error messages from console
   - Your CSS configuration

## Additional Resources

- [Jellyfin Documentation](https://jellyfin.org/docs/)
- [CSS Customization Guide](https://jellyfin.org/docs/general/clients/css-customization/)
- [Jellyfin Forums](https://forum.jellyfin.org/)
- [Project GitHub](https://github.com/YOUR-USERNAME/jellyfin-punk)

---

**Need more help?** Open an issue on GitHub or visit the Jellyfin community forums.
