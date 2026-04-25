# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static portfolio website for Hussain Shamkhani, deployed via GitHub Pages at `hussainshamkhani.github.io`. Built on the "Massively" template by HTML5 UP (CCA 3.0 licensed).

## Development

No build system, package manager, or test framework. The site is pure static HTML/CSS/JS served directly by GitHub Pages. To preview locally, open `index.html` in a browser or use any static file server.

SASS source lives in `assets/sass/` but the compiled CSS (`assets/css/main.css`) is committed directly — there is no SASS compilation step configured. Edit `main.css` for style changes, or set up a SASS compiler if modifying the `.scss` files.

## Architecture

- **index.html** — Single-page portfolio (intro, projects grid, contact/footer)
- **generic.html / elements.html** — Template reference pages from HTML5 UP
- **assets/css/main.css** — All styles (compiled from SASS source); `noscript.css` for JS-disabled fallback
- **assets/js/main.js** — Site behavior (scroll effects, mobile nav panel, form handling). Depends on jQuery, jquery.scrollex, jquery.scrolly, breakpoints.js, browser.js, and util.js
- **assets/sass/** — SCSS source organized into `base/`, `components/`, `layout/`, and `libs/` (variables, mixins, breakpoints, grid)
- **images/** — Profile photo, project screenshots, favicon (`code.png`)

## Key Details

- Responsive breakpoints defined in `assets/sass/libs/_vars.scss`: xxsmall (360px) through xlarge (1680px)
- Fonts: Merriweather (serif) and Source Sans Pro (sans-serif) via Google Fonts
- Icons: FontAwesome (bundled in `assets/css/fontawesome-all.min.css` + `assets/webfonts/`)
- Base href is set to `https://hussainshamkhani.github.io/` in index.html
