# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.0] - 2025-12-08

### COMPLETE REWRITE - Built on Ultrachromic

This is a **complete rewrite** from the ground up, addressing all UI-breaking issues from previous versions. The theme now uses [Ultrachromic](https://github.com/CTalvio/Ultrachromic) as its proven, stable foundation.

### Added
- **Three CyberPunk Variants:**
  - Blue Preset (Electric Blue #00a4dc + Neon Yellow #ffd700)
  - Dark Preset (Deep Purple #8b00ff + Hot Pink #e6007a)
  - Mono Preset (Light Gray #c8c8c8 + Subtle Cyan #00cccc)
- **Modular Architecture:** Mix and match components like Ultrachromic
- **Single Line Presets:** Install any variant with just one import line
- **Proven Base:** Uses Ultrachromic's tested base.css and accentlist.css
- **UI Fixes:** Includes Ultrachromic's fixes.css for better UI consistency

### Changed
- **Architecture:** Switched from monolithic CSS to modular component system
- **Base Theme:** Now built on Ultrachromic instead of custom implementation
- **Color System:** Uses RGB CSS variables (e.g., `rgba(var(--accent), 0.5)`) for proper transparency
- **Installation:** Simplified to single-line presets or modular imports
- **Documentation:** Complete rewrite following Ultrachromic's clear structure

### Fixed
- **Images Now Fully Visible:** No more black/blacked-out card images
- **No UI Breaking:** Theme enhances Jellyfin's UI instead of fighting it
- **Clean Text:** Removed all problematic text glows and shadows
- **Proper Borders:** Single clean border on hover, no stacking or weird effects
- **Icon Alignment:** All icons properly positioned and centered
- **Card Styling:** Transparent by default, subtle accents on hover
- **Backdrop Filters:** Removed all filters that blocked poster images
- **Mobile Compatibility:** Proper responsive behavior on all devices

### Removed
- **All Previous CSS:** Completely removed broken v1.x implementations
- **Custom Font Loading:** Now optional, not forced
- **Overwhelming Effects:** Removed excessive glows, shadows, and filters
- **Scanline Addons:** Simplified theme, removed optional effects for now
- **Color Variants:** Removed broken purple-haze, neon-nights, tokyo-drift variants
- **Logo Enhancement:** Removed for stability (can be added back if needed)

### Breaking Changes
- **All v1.x imports will break:** URLs have changed to new modular structure
- **Old variants removed:** purple-haze, neon-nights, tokyo-drift no longer exist
- **New presets required:** Use blue_preset, dark_preset, or mono_preset instead
- **dist/ directory removed:** Files now in root with type/ and presets/ subdirectories

### Migration Guide from v1.x

**Old (v1.x):**
```css
@import url("https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk@main/dist/main.css");
```

**New (v2.0.0) - Choose one:**
```css
/* Blue variant */
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/presets/blue_preset.css');

/* Dark variant */
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/presets/dark_preset.css');

/* Mono variant */
@import url('https://cdn.jsdelivr.net/gh/neowara/jellyfin-punk/presets/mono_preset.css');
```

## [1.3.0] - 2025-12-08 [DEPRECATED]

### Changed - COMPLETE REWRITE (Failed Attempt)
- Stripped down to minimal, clean design - still had issues
- Removed ALL text glows and shadows
- Cards transparent by default, border only on hover
- Single clean border on hover
- **Note:** This version still broke the UI, leading to v2.0.0 rewrite

## [1.1.0] - 2025-12-08 [DEPRECATED]

### Changed (Failed Attempt)
- Major visual refinement attempt
- Reduced border brightness and opacity
- Desaturated accent colors
- Softened glow effects
- **Note:** This version had major issues with blacked-out images

## [1.0.0] - 2025-12-08 [DEPRECATED]

### Added (Initial Broken Release)
- Initial release attempt of Jellyfin-Punk theme
- CyberPunk aesthetic with neon colors
- Comprehensive styling for Jellyfin elements
- **Note:** This version completely broke the UI with invisible images

---

## Version History Summary

### Version Numbering
- **Major (X.0.0)**: Breaking changes or complete redesigns
- **Minor (0.X.0)**: New features, variants, or significant improvements
- **Patch (0.0.X)**: Bug fixes, documentation updates, minor tweaks

### Stability Timeline
- **v1.0.0 - v1.4.0**: Unstable, UI-breaking releases (DEPRECATED)
- **v2.0.0+**: Stable releases built on Ultrachromic foundation

### Support
For issues or questions, please open an issue on [GitHub](https://github.com/neowara/jellyfin-punk/issues).

## [Unreleased]

### Planned Features for v2.1.0
- Optional scanline effect addon (if requested)
- Optional logo enhancement (if requested)
- Additional color preset variants
- Performance optimizations
- More customization examples
