# GLPLAY - Netflix-like Streaming Website

A professional Netflix-inspired streaming website interface built with HTML, CSS, and JavaScript. Features a sleek black and gray color scheme with all the modern UI elements you'd expect from a premium streaming platform.

## 🎬 Features

- **Netflix-like Interface**: Authentic design matching Netflix's professional look and feel
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices
- **Interactive Carousels**: Smooth horizontal scrolling content rows with navigation buttons
- **Hero Section**: Eye-catching banner with featured content
- **Modal Windows**: Detailed content information popups
- **Hover Effects**: Rich interactions when hovering over content items
- **Professional Branding**: GLPLAY branding with Netflix's signature red accent color
- **Keyboard Navigation**: Full keyboard accessibility support
- **Loading Animations**: Smooth transitions and animations throughout
- **Search Functionality**: Interactive search feature
- **My List Management**: Add/remove content from personal lists
- **Rating System**: Like/dislike content functionality

## 🎨 Design

- **Color Scheme**: Professional black (#141414) and gray (#333, #666, #999) palette
- **Typography**: Netflix Sans font family with proper fallbacks
- **Layout**: Netflix-inspired grid layout with content rows
- **Branding**: GLPLAY logo with signature red color (#e50914)

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Node.js (optional, for live server)

### Installation

1. Clone or download this repository
2. Navigate to the project directory:
   ```bash
   cd glplay-website
   ```

3. Option A: Use a simple HTTP server
   ```bash
   # If you have Python installed
   python -m http.server 8000
   
   # If you have Node.js and live-server
   npm install -g live-server
   live-server .
   ```

4. Option B: Open directly in browser
   - Simply open `index.html` in your web browser

### Development

To run the development server:
```bash
npm run dev
```

This will start a live-reloading server on `http://localhost:3000`

## 📁 Project Structure

```
glplay-website/
├── index.html          # Main HTML file
├── css/
│   └── style.css      # All CSS styles
├── js/
│   └── script.js      # JavaScript functionality  
├── images/            # Image assets (placeholder structure)
├── assets/            # Additional assets
├── package.json       # Project configuration
└── README.md         # This file
```

## 🔧 Features & Functionality

### Navigation Bar
- Fixed position header with transparent-to-solid transition on scroll
- GLPLAY logo with Netflix-red styling
- Navigation menu items (Home, TV Shows, Movies, etc.)
- Search icon, notifications, and profile dropdown

### Hero Section
- Large background image/video area
- Featured content title and description
- Play and More Info buttons
- Gradient fade to main content

### Content Rows
- **Trending Now**: Current popular content
- **Popular on GLPLAY**: Platform-specific popular content
- **GLPLAY Originals**: Exclusive original content
- Horizontal scrolling with navigation arrows
- Hover effects revealing content controls

### Interactive Elements
- Play buttons for immediate content playback
- Add to List functionality with toggle states
- Rating system (thumbs up/down)
- Content detail modals
- Keyboard navigation support

### Responsive Design
- Mobile-first approach
- Breakpoints at 480px, 768px, and 1024px
- Adaptive content sizing
- Touch-friendly interactions on mobile

## 🎯 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 🛠 Customization

### Colors
The color scheme can be modified in `css/style.css`:
```css
/* Primary background */
background-color: #141414;

/* Accent color (Netflix red) */
color: #e50914;

/* Secondary grays */
color: #333333; /* Dark gray */
color: #666666; /* Medium gray */
color: #999999; /* Light gray */
```

### Content
- Modify content in `index.html`
- Replace placeholder images with actual content images
- Update titles and descriptions
- Add more content rows as needed

### Branding
- Change "GLPLAY" to your brand name
- Update logo styling in CSS
- Modify color scheme to match your brand

## 📱 Performance

- Optimized CSS with minimal unused styles
- Lazy loading for images
- Smooth animations with GPU acceleration
- Debounced resize events
- Efficient DOM manipulation

## 🔒 Security

- No external dependencies loaded from CDN
- All images use placeholder services (replace with your own)
- No sensitive data exposure
- Content Security Policy ready

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🎉 Acknowledgments

- Inspired by Netflix's user interface design
- Built with modern web standards
- Optimized for performance and accessibility

## 📞 Support

For support, please open an issue in the repository or contact the development team.

---

**GLPLAY** - Experience entertainment like never before! 🍿✨