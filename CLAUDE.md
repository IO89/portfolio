# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static HTML/CSS portfolio website for Ivan Osipov showcasing work experience and projects. No build system or package manager is required.

## Development

**Preview the site:**
Simply open `index.html` or `about.html` in a web browser. For live reloading during development, use any static file server:
```bash
python -m http.server 8000
# or
npx serve
```

## Architecture

**Structure:**
- `index.html` - Main page with intro, projects section, and contact form
- `about.html` - About page with profile photo and bio
- `styles.css` - All styling with CSS custom properties for theming

**Layout System:**
- Mobile-first responsive design
- Flexbox for navigation and list layouts
- CSS Grid for about page article layout (desktop view)
- Media queries at 800px and 850px breakpoints

**Color Scheme:**
Defined in CSS custom properties at `:root`:
- `--dkblue` (#042940) - primary background
- `--dkgreen` (#005C53) - section backgrounds
- `--green` (#9FC131) - links and accents
- `--ltgreen` (#DBF227) - hover states and highlights
- `--sand` (#D6D58E) - primary text color
- `--black` (#171321) - content boxes

**Typography:**
- Uses Google Fonts (Roboto and Roboto Mono) loaded from CDN
- Local Roboto Mono fonts available in `assets/fonts/`
- CSS variables: `--sans` for body text, `--mono` for code-style elements

**External Dependencies:**
- FontAwesome kit for icons (loaded via CDN)
- Google Fonts API
- No npm packages or build tools required

## Common Updates

**Adding a new project:**
Add a new `<h3>` and project block inside `#projects article` in `index.html`, following the existing structure with title, description in `.blackbox`, and technology list.

**Updating contact info:**
- Main page: `index.html` line 304 (email) and footer links
- About page: `about.html` line 67 (email) and footer links
- Update Google Drive resume link in both navigation bars

**Modifying colors:**
Update CSS custom properties in `styles.css` at `:root` (lines 1-11).
