# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static HTML portfolio website for Majd Iskandarani, a NanoEngineering researcher at UCSD. The portfolio showcases research projects, technical skills, and equipment authorizations in nanofabrication and characterization.

## Project Structure

- **Code/index.html** - Main portfolio website (self-contained HTML with embedded CSS and JavaScript)
- **Research Project Directories:**
  - **Algae/** - Contains algae research images (Pico Algae/, Regular Algae/)
  - **MgAu/** - Mg-Au nanoparticle synthesis project images (Fabrication/, MgAu SEM/)
  - **Microneedles/** - Conductive microneedle array project images (Fabrication/, SEM/)
  - **Lithography/** - E-beam lithography and microfluidics project (single image file)

## Architecture

The portfolio is built as a single-page application using:
- **Pure HTML/CSS/JavaScript** - No build system or dependencies
- **Responsive design** - Mobile-first approach with CSS Grid and Flexbox
- **Interactive project cards** - Expandable sections with image galleries
- **Lightbox functionality** - For viewing project images in detail
- **Smooth animations** - CSS transitions and keyframe animations

### Key Features
- Project gallery system with expandable cards
- Image lightbox with keyboard navigation (Escape to close)
- Sticky navigation with smooth scrolling
- Equipment authorization showcase
- Technical skills categorization
- Publication display

## Development

### Running the Portfolio
Since this is a static HTML file, you can:
1. Open `Code/index.html` directly in a web browser
2. Serve it using a simple HTTP server for full functionality:
   ```bash
   cd Code
   python -m http.server 8000
   # or
   npx serve .
   ```

### Working with Images
The portfolio references images using relative paths like `images/algae/algae-1.jpg`. The actual project images are stored in:
- Algae research: `Algae/Pico Algae/` and `Algae/Regular Algae/`
- MgAu nanoparticles: `MgAu/MgAu SEM/` and `MgAu/Fabrication/`
- Microneedles: `Microneedles/SEM/` and `Microneedles/Fabrication/`
- Lithography: `Lithography/`

To properly display images, you would need to:
1. Create an `images/` directory structure in the `Code/` folder
2. Organize and rename project images to match the HTML references
3. Or update the HTML image paths to point to the existing directory structure

### Code Style
- Uses modern CSS with custom properties for theming
- Semantic HTML structure
- Vanilla JavaScript for interactivity
- Color scheme: earth tones (#5d4e37, #8b7355, #fdfcfb)
- Typography: Nunito and system fonts

No build tools, package managers, or frameworks are used - this is intentionally a simple, self-contained portfolio.