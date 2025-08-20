# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based GitHub Pages site for g0ld2k.com, serving as a portfolio/showcase for iOS apps. The site features two main apps:

- **Contadino**: A Pomodoro-style focus tracking app for macOS, iOS, iPadOS, and watchOS
- **Distance Track**: A fitness tracking app for iOS and iPadOS that integrates with Apple Health

## Architecture

The site uses a simple Jekyll structure with the Tactile theme:

- `index.md` - Main landing page with app links
- `Contadino/` - App page with features, TestFlight link, privacy policy, and terms
- `DistanceTrack/` - App page with features, TestFlight link, and privacy policy
- `assets/images/` - App icons, hero images, and marketing assets
- `_config.yml` - Jekyll configuration with site metadata
- `_site/` - Generated static site (auto-generated, don't edit)

## Development Commands

### Local Development
```bash
bundle install          # Install Ruby dependencies
bundle exec jekyll serve # Start local development server
```

The development server runs on `http://localhost:4000` and automatically rebuilds when files change.

### Dependency Management
```bash
bundle update           # Update all gems
bundle update github-pages  # Update just GitHub Pages gem
```

## Content Guidelines

- App pages follow consistent structure: hero image, TestFlight link, feature list, privacy policy link
- Images are stored in `assets/images/` and referenced with absolute paths
- Privacy policies and terms of use are separate markdown files in each app directory
- Contact information uses app-specific email addresses (contadino@g0ld2k.com, distance.track@g0ld2k.com)

## Deployment

The site auto-deploys to GitHub Pages when changes are pushed to the `main` branch. GitHub Actions handles the Jekyll build process using the `github-pages` gem.