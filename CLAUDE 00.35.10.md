# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the Sarum Digital company website - a static HTML/CSS/JavaScript site that showcases digital services including web development, AI solutions, and software development. The site uses modern web technologies with animations and responsive design.

## Architecture

### Directory Structure
- **Root level**: Contains main `index.html` entry point that redirects to the main site
- **Digitaal/html.kodesolution.com/2025/digitaal-html/**: Main website directory containing all assets
  - `index.html`: Main homepage
  - `css/`: Stylesheets including Bootstrap, custom styles, and third-party libraries
  - `js/`: JavaScript files including jQuery, GSAP animations, and custom scripts  
  - `images/`: All image assets organized by type (background, banner, icons, projects, etc.)
  - `fonts/`: Custom fonts and icon fonts
  - Page templates: `page-about.html`, `page-services.html`, `portfolio.html`, etc.

### Technology Stack
- **Frontend Framework**: Bootstrap 5 for responsive layout
- **Animation Libraries**: 
  - GSAP (GreenSock) with ScrollTrigger for scroll animations
  - AOS (Animate On Scroll) for reveal animations
  - Custom CSS animations
- **UI Components**: 
  - jQuery for DOM manipulation
  - Swiper.js for carousels/sliders
  - Fancybox for modals/lightboxes
  - Select2 for enhanced dropdowns
- **Icons**: FontAwesome and custom Flaticon set
- **Fonts**: Custom web fonts loaded via CSS

## Key Features

### Animation System
The site heavily uses GSAP for sophisticated animations:
- ScrollTrigger for scroll-based animations
- SplitText for text animations
- Timeline animations for complex sequences
- Smooth scrolling implementation

### Responsive Design
- Mobile-first approach with Bootstrap grid
- Custom mobile navigation with hamburger menu
- Responsive images and typography scaling
- Touch-friendly interactions

### Content Sections
- Hero banner with animated elements
- Services showcase
- Portfolio/projects gallery
- Team profiles
- Client testimonials
- Contact forms with validation

## Development Workflow

### Local Development
Since this is a static site, serve it using any HTTP server:
```bash
# Using Python (recommended)
python3 -m http.server 8000

# Using Node.js http-server (if available)
npx http-server

# Using PHP (if available)  
php -S localhost:8000
```

### File Editing
- Edit HTML files directly for content changes
- Modify `css/style.css` for custom styling
- Update `js/script.js` for custom JavaScript functionality
- Replace images in respective `images/` subdirectories

### Performance Considerations
- Images are optimized but should be compressed further if adding new ones
- CSS and JS files are minified in production
- Consider lazy loading for images below the fold
- GSAP animations may impact performance on slower devices

## Common Tasks

### Content Updates
- Company information: Edit `index.html` and relevant page templates
- Services: Update `page-services.html` and service detail pages
- Portfolio: Modify `portfolio.html` and add project images to `images/projects/`
- Team: Update `page-team.html` and team member images in `images/resource/`

### Styling Changes
- Primary colors and brand styling: `css/style.css`
- Layout modifications: Bootstrap classes in HTML templates
- Animation timing: GSAP configurations in `js/script.js`

### Adding New Pages
- Create new HTML file following existing template structure
- Add navigation links in header section of all pages
- Include all required CSS/JS assets
- Test responsive design across devices

## Contact Integration
The site includes contact forms that may require backend integration:
- Contact form: `page-contact.html`
- Email configuration may be needed for form submission
- Current setup appears to use client-side validation only