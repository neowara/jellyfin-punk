# Contributing to Jellyfin-Punk

Thank you for your interest in contributing to Jellyfin-Punk! This document provides guidelines for contributing to the project.

## Ways to Contribute

- **Report Bugs**: Submit detailed bug reports with reproduction steps
- **Suggest Features**: Propose new features or improvements
- **Submit Pull Requests**: Fix bugs or implement new features
- **Improve Documentation**: Help make the docs clearer and more comprehensive
- **Create Variants**: Design new color schemes and share them
- **Test**: Help test the theme on different devices and browsers

## Getting Started

### Prerequisites

- Git installed on your computer
- A text editor (VS Code, Sublime Text, etc.)
- Basic knowledge of CSS
- A Jellyfin server for testing (can be local)

### Setting Up Development Environment

1. **Fork the repository** on GitHub

2. **Clone your fork**:
   ```bash
   git clone https://github.com/YOUR-USERNAME/jellyfin-punk.git
   cd jellyfin-punk
   ```

3. **Create a new branch**:
   ```bash
   git checkout -b feature/your-feature-name
   ```

4. **Make your changes** in the `src/` directory

5. **Test your changes**:
   - Copy the CSS from `src/main.css`
   - Paste into Jellyfin Custom CSS field
   - Test on multiple pages and devices

## Code Style Guidelines

### CSS Formatting

```css
/* Use consistent formatting */
.selector {
    property: value !important;
    another-property: value !important;
}

/* Add comments for sections */
/* ============================================
   SECTION NAME
   ============================================ */

/* Group related selectors */
.selector1,
.selector2,
.selector3 {
    property: value !important;
}

/* Use CSS variables for colors */
color: var(--accent-cyan) !important;
/* NOT: color: #00ffff !important; */
```

### Naming Conventions

- Use existing Jellyfin class names when possible
- Keep variable names clear and descriptive
- Follow the established color naming pattern (--accent-*, --background-*, --text-*)

### Comments

- Add section headers for major sections
- Comment complex selectors
- Explain "why" not just "what" for non-obvious code

## Creating New Features

### Adding a New Color Variant

1. Create a new file in `dist/variants/your-variant-name.css`
2. Use this template:

```css
/**
 * Jellyfin-Punk Theme - Your Variant Name
 * Description of the variant
 * Version: 1.0.0
 * Import this AFTER main.css to override colors
 */

:root {
    --accent-cyan: #your-color !important;
    --accent-magenta: #your-color !important;
    --accent-purple: #your-color !important;
    /* etc. */
}

/* Additional specific overrides if needed */
```

3. Update README.md with your variant
4. Add to INSTALL.md instructions
5. Submit a pull request

### Adding a New Addon

1. Create a new file in `dist/addons/your-addon-name.css`
2. Add clear comments explaining what it does
3. Include usage instructions in the file header
4. Test for conflicts with existing features
5. Update documentation

## Testing Checklist

Before submitting a pull request, test your changes on:

### Pages
- [ ] Home page
- [ ] Library view
- [ ] Item detail page
- [ ] Settings page
- [ ] Dashboard (admin)
- [ ] Search results
- [ ] Video player

### Browsers
- [ ] Chrome/Edge (latest)
- [ ] Firefox (latest)
- [ ] Safari (latest)
- [ ] Mobile browsers

### Devices
- [ ] Desktop/Laptop
- [ ] Tablet
- [ ] Mobile phone
- [ ] TV app (if possible)

### Features
- [ ] Cards display correctly
- [ ] Buttons are clickable and styled
- [ ] Hover effects work
- [ ] Animations are smooth
- [ ] Text is readable
- [ ] No performance issues
- [ ] Works with other addons

## Submitting Changes

### Pull Request Process

1. **Update your branch**:
   ```bash
   git pull origin main
   ```

2. **Copy changes to dist**:
   ```bash
   cp src/main.css dist/main.css
   # Or for specific files
   cp src/your-file.css dist/your-file.css
   ```

3. **Commit your changes**:
   ```bash
   git add .
   git commit -m "feat: Add your feature description"
   ```

4. **Push to your fork**:
   ```bash
   git push origin feature/your-feature-name
   ```

5. **Open a Pull Request** on GitHub

### Commit Message Format

Use clear, descriptive commit messages:

- `feat: Add new color variant`
- `fix: Resolve button hover issue`
- `docs: Update installation guide`
- `style: Improve CSS formatting`
- `perf: Optimize glow effects`
- `refactor: Reorganize card styles`

### Pull Request Template

When opening a PR, include:

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Performance improvement
- [ ] Other (specify)

## Testing
- [ ] Tested on desktop
- [ ] Tested on mobile
- [ ] Tested multiple browsers
- [ ] No console errors
- [ ] Works with existing variants/addons

## Screenshots
Add screenshots showing your changes

## Related Issues
Fixes #(issue number)
```

## Reporting Bugs

### Before Reporting

1. Check if the issue already exists in GitHub Issues
2. Verify it's not a Jellyfin issue (test with default theme)
3. Clear your browser cache and test again
4. Try a different browser

### Bug Report Template

```markdown
**Describe the bug**
Clear description of what's wrong

**To Reproduce**
Steps to reproduce:
1. Go to '...'
2. Click on '....'
3. See error

**Expected behavior**
What you expected to happen

**Screenshots**
Add screenshots if applicable

**Environment:**
- Jellyfin Version: [e.g. 10.8.9]
- Browser: [e.g. Chrome 120]
- OS: [e.g. Windows 11]
- Theme Version: [e.g. 1.0.0]
- Using variants/addons: [yes/no, which ones]

**Additional context**
Console errors, other themes tested, etc.
```

## Suggesting Features

### Feature Request Template

```markdown
**Is your feature request related to a problem?**
Description of the problem

**Describe the solution you'd like**
Clear description of what you want

**Describe alternatives considered**
Other approaches you've thought about

**Additional context**
Mockups, examples from other themes, etc.
```

## Code Review Process

1. Maintainers will review your PR
2. They may request changes or ask questions
3. Make requested changes and push updates
4. Once approved, your PR will be merged
5. You'll be credited in the project!

## Community Guidelines

- Be respectful and constructive
- Help others when possible
- Give credit where credit is due
- Follow the Jellyfin community guidelines
- Have fun and be creative!

## Questions?

- Open a Discussion on GitHub
- Ask in Jellyfin Forums
- Check existing Issues and PRs

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

**Thank you for contributing to Jellyfin-Punk!** 🎉
