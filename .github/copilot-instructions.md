# GREDA Corporate Website - AI Assistant Instructions

## Project Overview
This is a **Polish corporate business card website** for GREDA company featuring a distinctive black logo with red accent branding. The site uses vanilla JavaScript, CSS3, and semantic HTML5 without external frameworks.

## Key Architecture Patterns

### Visual Brand System
- **Logo**: Black background (`#000`) with red border (`#dc2626`) and glowing effects
- **Typography**: 'Orbitron' for logo, 'Roboto' for content, Polish language (`lang="pl"`)
- **Color scheme**: Dark gradient background with red accent (`--accent-color: #dc2626`)
- **Logo effects**: Multi-layer box-shadow, text-shadow, and hover glow animations

### Animation System (`script.js`)
- **Staggered loading**: Logo → hero content → service cards with 200ms delays
- **Intersection Observer**: Scroll-based animations with `fade-in` class
- **Hover effects**: Dynamic box-shadow manipulation on logo container
- **Smooth scrolling**: Custom implementation for anchor links

### Layout Architecture
```
Header (logo-container > logo > company-name)
Main (hero-section + services-preview)
Footer (contact-info)
```

## Development Workflows

### Local Development
```powershell
# Start development server (preferred method)
python -m http.server 8000
# Or use VS Code task: "Start HTTP Server"
```

### Deployment Structure
- **Source files**: Root directory (`index.html`, `styles.css`, `script.js`)
- **Production files**: `/deployment/` directory (identical copies)
- **Live site**: https://greda.pl

### File Organization
- `DEPLOYMENT.md` - FTP credentials and hosting instructions
- `GITHUB_UPLOAD.md` - Repository setup guide
- CSS uses mobile-first responsive approach (768px, 480px breakpoints)

## Code Conventions

### CSS Structure
1. Reset and base styles
2. Header/logo styling with complex shadow effects
3. Main content sections
4. Interactive states (hover, focus)
5. Media queries (mobile-first)

### JavaScript Patterns
- **DOM-ready pattern**: `DOMContentLoaded` event handling
- **Animation timing**: Uses `setTimeout` chains for sequencing
- **Element selection**: Query selectors with class-based targeting
- **Console branding**: Welcome message with company emojis

### Responsive Design
- **Grid system**: `grid-template-columns: repeat(auto-fit, minmax(250px, 1fr))`
- **Flexible logo**: Font-size scales from 4rem → 2.5rem → 2rem
- **Backdrop blur**: `backdrop-filter: blur(10px)` on service cards

## Critical Integrations

### Font Loading
Uses Google Fonts with preconnect optimization:
- Orbitron (400, 700, 900) for logo
- Roboto (300, 400, 500) for content

### Browser Support
- Modern CSS features: `backdrop-filter`, CSS Grid, CSS custom properties
- ES6+ JavaScript: `forEach`, `setTimeout`, Intersection Observer API
- No polyfills or fallbacks included

## Polish Language Context
- All content in Polish language
- Business terminology: "firma", "usługi", "rozwiązania"
- Meta tags and SEO optimized for Polish market
- Currency/contact info follows Polish conventions

When modifying this codebase:
- Maintain the red (`#dc2626`) brand color consistency
- Preserve the staggered animation timing system
- Keep Polish language in all user-facing content
- Test responsive behavior on mobile devices
- Ensure logo shadow effects remain visually consistent