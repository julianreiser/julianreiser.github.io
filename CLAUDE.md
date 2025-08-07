# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Hugo-based academic website using the PaperMod theme, hosted on GitHub Pages. The site showcases research papers, courses, data, and other academic content for Julian Elias Reiser's personal website.

## Architecture

- **Static Site Generator**: Hugo v0.142.0+ (production uses v0.147.2)
- **Theme**: PaperMod (located in `themes/PaperMod/` as a Git submodule)
- **Hosting**: GitHub Pages with automated deployment
- **Content Structure**:
  - `content/papers/` - Research papers with PDFs and metadata
  - `content/courses/` - Course materials and lecture notes
  - `content/books/` - Book chapters and related materials
  - `content/data/` - Research data and datasets
  - `static/` - Static assets (CV, images, favicons)
  - `layouts/` - Custom Hugo templates (overrides theme defaults)

## Key Commands

### Local Development
```bash
hugo server
```
Starts local development server at http://localhost:1313 with live reload.

### Build Production Site
```bash
hugo --minify
```
Generates static site in `public/` directory ready for deployment.

### Content Management
- Content files use Hugo's front matter (YAML) for metadata
- Academic papers follow the archetype in `archetypes/paper.md`
- Courses follow the archetype in `archetypes/course.md`

## Configuration

- **Main config**: `config.yml` - Contains site settings, menu structure, theme parameters
- **Base URL**: Currently set to `https://julianreiser.github.io`
- **Theme customization**: Override theme templates by placing files in `layouts/`
- **Profile mode**: Enabled in config with custom buttons and social icons

## Deployment

Automatic deployment via GitHub Actions (`.github/workflows/hugo.yml`):
- Triggers on pushes to `main` branch
- Uses Hugo v0.147.2 in production
- Deploys to GitHub Pages automatically

## Content Structure Patterns

- Each content section (`papers/`, `courses/`, etc.) has an `_index.md` file
- Individual items are in subdirectories with `index.md` and associated files (PDFs, images)
- Academic papers include: main PDF, presentation slides, appendices, cover images
- Courses include: lecture PDFs, problem sets, course materials

## Theme Customizations

- Custom CSS in `assets/css/` overrides theme defaults
- Custom layouts in `layouts/` extend PaperMod functionality
- Math rendering enabled via theme parameters
- Custom social icons for academic platforms (Google Scholar, ResearchGate, etc.)