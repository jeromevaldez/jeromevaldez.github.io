# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal GitHub Pages website for Jerome Valdez, a UX designer. The site is a static website that showcases personal information, experiments, music recommendations, and AI workshops for UX designers.

## Repository Structure

- **Root files**: Main landing page (`index.html`), global styles (`styles.css`, `tokens.css`), and alternative style themes (`style1.css`, `style2.css`, `style3.css`)
- **workshop-v2/**: Current workshop presentation files for "AI for UX Designers"  
- **workshop/**: Legacy workshop files
- **ides151/** & **ides252/**: Course materials and teaching resources from design courses
- **bootstrap-tests/**: Bootstrap CSS testing/experimentation
- **breakpoints/**: Responsive design experiments

## Development Workflow

This is a static site hosted on GitHub Pages. No build process or package manager is required.

### Deployment
- Site automatically deploys to GitHub Pages when changes are pushed to the `master` branch
- Live site: https://jeromevaldez.github.io

### File Serving
- All HTML files can be opened directly in browser
- CSS and JS files are referenced directly (no compilation needed)
- External dependencies loaded via CDN

## Architecture & Design System

### CSS Architecture
- **tokens.css**: Design system tokens based on Radix UI color system
  - Contains CSS custom properties for colors, spacing, and semantic tokens
  - Supports both light and dark modes
  - Use semantic color tokens (e.g., `--color-primary`, `--color-text-primary`) rather than direct color values

### Navigation System
- **Left sidebar navigation**: Fixed position navigation with responsive mobile hamburger menu
- **Style switcher**: Dynamic CSS theme switching with localStorage persistence
- **Mobile-first responsive design**: Breakpoints at 480px and 768px

### JavaScript Functionality
- Style switching system with localStorage persistence
- Mobile menu toggle functionality  
- No external JavaScript frameworks - vanilla JS only

## Content Areas

### Main Site (`index.html`)
- Personal landing page with navigation
- Links to experiments, music recommendations, and LinkedIn
- Style switcher demo functionality

### Workshop Content (`workshop-v2/`)
- Large-format presentation slides optimized for teaching
- Self-contained HTML with embedded CSS
- Responsive typography using `clamp()` for scalability
- Slide-based layout for presentation format

### Course Materials (`ides151/`, `ides252/`)
- Teaching resources and course websites
- Bootstrap-based responsive layouts
- Various HTML templates and CSS experiments

## Styling Guidelines

### CSS Custom Properties
- Always use semantic tokens from `tokens.css` for colors
- Example: `color: var(--color-text-primary)` instead of `color: #333`
- Maintain consistency with the established design system

### Responsive Design
- Mobile-first approach with progressive enhancement
- Use relative units (`rem`, `em`, `vw`, `vh`) for scalability
- Typography uses `clamp()` for fluid scaling across devices

### Typography
- Primary font: Inter (Google Fonts)
- Additional fonts available: Crimson Pro, Merriweather, IBM Plex Mono
- Use `clamp()` for responsive font sizing

## File Management

### Adding New Content
- HTML files can be added at any level - they'll be accessible via direct URL
- CSS files should reference the existing design token system
- Images should be organized in `img/` subdirectories within each section

### Style Modifications
- Modify `styles.css` for global changes
- Use `tokens.css` for design system updates
- Alternative themes go in separate CSS files (`style1.css`, etc.)

## External Dependencies

### CDN Resources
- Google Fonts: Inter, Crimson Pro, Merriweather, IBM Plex Mono
- Phosphor Icons: `<script src="https://unpkg.com/phosphor-icons"></script>`
- Bootstrap (in course materials): Various versions loaded via CDN

### No Package Manager
- This project intentionally avoids Node.js, npm, or build tools
- All dependencies loaded via CDN or included directly
- Keep external dependencies minimal

## Common Tasks

### Adding a New Page
1. Create HTML file in appropriate directory
2. Include standard CSS references: `tokens.css` and `styles.css`
3. Follow existing HTML structure and semantic patterns
4. Test responsive behavior at different breakpoints

### Updating Styles
1. Use existing CSS custom properties from `tokens.css`
2. Add new tokens to `tokens.css` if needed for consistency
3. Test both light and dark modes if applicable
4. Verify mobile responsiveness

### Workshop Updates
- Workshop slides in `workshop-v2/` are self-contained
- Large viewport-optimized typography for classroom presentation
- Embedded styles for portability

## Content Guidelines

- Personal portfolio site showcasing UX design work and teaching
- Workshop content focuses on AI tools for UX designers
- Course materials support design education
- Maintain professional tone while keeping content accessible