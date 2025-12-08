# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.3.0] - 2025-12-08

### Changed - COMPLETE REWRITE
- **Stripped down to minimal, clean design** - Fixed all UI-breaking issues
- Removed ALL text glows and shadows
- Cards now transparent by default, border only on hover
- Removed all backdrop filters and overlays that blocked images
- Single clean border on hover instead of multiple stacked borders
- Removed card shadows that made images dark
- Simplified all styling to not break Jellyfin's default UI
- Clean, subtle cyberpunk accent color (#00cccc) without overwhelming effects
- No more weird borders or misaligned elements

### Fixed
- **Images now fully visible** - removed all filters and overlays
- **No more text glow** - clean, readable text throughout
- **Single border on hover** - no more stacked border effects
- **Icons properly aligned** - removed custom positioning
- **Clean card styling** - images no longer blacked out
- Theme now enhances instead of breaking the UI

## [1.1.0] - 2025-12-08

### Changed
- **Major visual refinement** - Significantly improved theme appearance
- Reduced border brightness from 0.3 to 0.15 opacity for subtle appearance
- Desaturated accent colors for better readability (#00ffff → #00e5e5, #ff0080 → #e6007a)
- Softened glow effects with new subtle, medium, and strong glow variables
- Improved card backgrounds with dedicated `--background-card` color
- Reduced text shadows on section titles for cleaner look
- Changed buttons from solid gradients to semi-transparent overlays with borders
- Toned down badge colors from harsh pink to softer magenta (0.9 opacity)
- Made borders and accents much more subtle throughout the UI

### Fixed
- Cards no longer have harsh, bright cyan borders
- Badges (unplayed counts) are now less overwhelming
- Text contrast improved for better readability
- Overall theme is more balanced and easier on the eyes
- Reduced visual noise while maintaining cyberpunk aesthetic

## [1.0.0] - 2025-12-08

### Added
- Initial release of Jellyfin-Punk theme
- Core CyberPunk aesthetic with neon colors (cyan, magenta, purple)
- Dark background with high contrast design
- Comprehensive styling for all Jellyfin elements:
  - Cards with hover effects and neon glows
  - Buttons with gradient backgrounds
  - Form elements with cyberpunk styling
  - Navigation bars with transparent blur
  - Media player controls
  - Dialogs and modals
  - Lists and tables
  - Indicators and badges
- Logo enhancement CSS (`logo.css`) with neon glow effects
- Scanlines addon for retro CRT effect
- Three color variants:
  - Purple Haze (purple/violet dominant)
  - Neon Nights (cyan/blue dominant)
  - Tokyo Drift (magenta/pink dominant)
- Custom scrollbar styling
- Smooth animations and transitions
- Responsive design for desktop, tablet, and mobile
- Performance optimizations for lower-end devices
- Accessibility features (focus indicators, reduced motion support)
- Comprehensive documentation:
  - README.md with quick start guide
  - INSTALL.md with detailed installation instructions
  - CUSTOMIZATION.md with customization examples
  - CONTRIBUTING.md with contribution guidelines
- Preview HTML for local testing
- npm package configuration
- MIT License

### Features
- CSS variable-based theming system
- GPU-accelerated animations
- Multiple import methods (CDN, GitHub Pages, local)
- Modular addon system
- Browser compatibility with Chrome 105+, Firefox 121+, Safari 15.4+
- Works with Jellyfin 10.8.0+
- Support for Nginx reverse proxy configurations

### Documentation
- Installation guide with multiple methods
- Troubleshooting section
- Customization examples and guides
- Contribution guidelines
- Color palette documentation
- Performance optimization tips

## [Unreleased]

### Planned Features
- Additional color variants (Matrix Green, Vaporwave, Synthwave)
- More optional addons (grid overlay, particles effect)
- Improved logo positioning options
- Custom font recommendations
- Video player enhancements
- Dashboard customizations
- Theme builder tool

---

## Version History

### Version Numbering
- **Major (X.0.0)**: Breaking changes or complete redesigns
- **Minor (0.X.0)**: New features, variants, or significant improvements
- **Patch (0.0.X)**: Bug fixes, documentation updates, minor tweaks

### Support
For version-specific issues or questions, please refer to the documentation for that version or open an issue on GitHub.
