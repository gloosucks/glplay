# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project Overview

GLPLAY is a Netflix-inspired streaming website interface built with vanilla HTML, CSS, and JavaScript. It features a professional black and gray color scheme with Netflix's signature red accent color (#e50914) for the GLPLAY branding.

## Development Commands

### Start Development Server
```powershell
# Start live server on default port 8080
npm start

# Start live server on port 3000 with hot reload
npm run dev

# Alternative: Use Python HTTP server
python -m http.server 8000

# Alternative: Open index.html directly in browser (for basic testing)
start index.html
```

### No Build Process
This is a static website with no build step required. All assets are served directly.

### No Testing Framework
Currently no automated tests are configured. Testing is done manually in the browser.

### No Linting
No linting tools are currently configured.

## Architecture Overview

### File Structure
- `index.html` - Main entry point with complete page structure
- `css/style.css` - Single CSS file containing all styles (~560 lines)
- `js/script.js` - Single JavaScript file with all functionality (~403 lines)
- `package.json` - NPM configuration for live-server dependency only

### Core Components

**Navigation System**
- Fixed header with scroll-triggered transparency effects
- GLPLAY logo with Netflix-red styling (#e50914)
- Responsive navigation that hides menu items on tablet/mobile

**Hero Section**
- Large banner area with background image overlay
- Featured content display (currently "Stranger Things")
- Auto-rotating content every 10 seconds with predefined titles
- Play/More Info buttons with modal integration

**Content Rows**
- Horizontal scrolling carousels for "Trending Now", "Popular on GLPLAY", "GLPLAY Originals"
- Each item supports play, add-to-list, and rating interactions
- Smooth scroll navigation with left/right arrow buttons
- Hover effects revealing content controls

**Interactive Features**
- Modal system for detailed content information
- Notification system with slide-in animations
- Keyboard navigation support (arrow keys, Enter, Escape)
- Accessibility features with focus states and tabindex management

### JavaScript Architecture

**Event-Driven Structure**: All functionality is initialized on DOMContentLoaded with modular functions:

- `initializeCarousel()` - Handles horizontal scrolling and navigation buttons
- `setupContentInteractions()` - Manages play, add-to-list, and rating buttons
- `showContentModal()` - Modal display system
- `showNotification()` - Toast notification system
- `makeItemsFocusable()` - Accessibility and keyboard navigation
- `setupLazyLoading()` - Image optimization (placeholder-based)
- `autoScrollHeroContent()` - Hero section content rotation

**State Management**: Simple DOM-based state for user interactions (button text changes, visual feedback)

### Styling Architecture

**CSS Organization**: Single file structured with:
1. Reset and base styles
2. Navigation components
3. Hero section
4. Content rows and carousels
5. Modal system
6. Footer
7. Responsive breakpoints (1024px, 768px, 480px)
8. Utility classes and animations

**Color Scheme**:
- Primary background: #141414 (Netflix black)
- GLPLAY brand color: #e50914 (Netflix red)
- Text hierarchy: #ffffff, #e5e5e5, #b3b3b3, #737373

**Responsive Design**: Mobile-first approach with progressive enhancement

## Content Management

**Image Assets**: Currently uses placeholder.com for all images. Replace with actual content images by updating `src` attributes in HTML and JavaScript.

**Content Data**: Hard-coded in HTML and JavaScript. To add new content:
1. Add new `.content-item` divs in HTML content rows
2. Update `heroTitles` array in JavaScript for hero rotation
3. Ensure consistent image dimensions (16:9 aspect ratio recommended)

## Browser Compatibility

Supports modern browsers with ES6+ features:
- Chrome, Firefox, Safari, Edge (latest versions)
- Uses modern APIs: IntersectionObserver, querySelector, addEventListener
- No polyfills included

## Performance Considerations

- Images use lazy loading with IntersectionObserver
- Debounced resize events (250ms)
- CSS transitions for smooth interactions
- GPU-accelerated animations with `transform` properties
- Service Worker registration included but no sw.js file present

## Key Development Patterns

**Responsive Carousel Logic**: Content items are 300px wide with dynamic scroll calculations based on visible items

**Interactive State Management**: Button states toggle between symbols (+ ↔ ✓, 👍 ↔ 👎)

**Modal System**: Centralized modal with dynamic content injection and proper focus management

**Notification System**: Programmatically created DOM elements with CSS transitions for slide animations

## Customization Points

**Branding**: Change "GLPLAY" throughout HTML/CSS and update the red accent color (#e50914)

**Content**: Replace placeholder images and update content titles/descriptions in HTML and JavaScript arrays

**Styling**: Modify color variables in CSS for different themes while maintaining contrast ratios

**Features**: Add new content rows by duplicating the HTML structure and ensuring JavaScript event binding includes new elements