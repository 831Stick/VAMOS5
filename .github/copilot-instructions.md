# VAMOS5 Website - AI Agent Instructions

## Project Overview
This is a Japanese restaurant/bar website for VAMOS5, a poker & shisha bar in Mizonokuchi, Kawasaki. The site is built with vanilla HTML, CSS, and JavaScript, optimized for SEO and responsive design.

## Architecture & File Structure
```
/
├── index.html          # Homepage with background slideshow & image gallery
├── system.html         # Pricing/services page with expandable details
├── event.html          # Events page with calendar integration
├── css/
│   ├── reset.css       # CSS reset
│   └── style.css       # Main stylesheet (1300+ lines, responsive)
├── images/             # All assets (photos, logos, icons)
├── videos/             # Video assets
└── analytics-setup.html # GA4 integration template
```

## Key Design Patterns

### CSS Architecture
- **Mobile-first responsive design** with breakpoints at 900px and 600px
- **Color scheme**: Primary `#8fd3d6` (teal), accent `#ff69b4` (pink), dark `#000/#222`
- **Typography**: 'Noto Serif JP' for Japanese text
- **Layout**: Flexbox-based with viewport-aware sizing (`100vw`, `95vw`)

### JavaScript Components
- **Background slideshow** (5-second intervals) on homepage
- **Image gallery slider** with 3-image preview and lightbox
- **Hamburger menu** for mobile navigation
- **Expandable pricing details** with `toggleDetails()` function
- **Touch/swipe support** for mobile interactions

### HTML Structure Conventions
- **Semantic markup** with proper heading hierarchy (H1 > H2 > H3)
- **SEO-optimized** with comprehensive meta tags, Open Graph, Twitter Cards
- **Accessibility** with ARIA labels and semantic navigation
- **Structured data** (Local Business schema) for search engines

## Content Management

### Image Assets
- **Photo naming**: `photo1.JPG` to `photo9.jpg`, `H1.JPG` to `H12.JPG`
- **Icons**: Coin logo, social media icons (Instagram, LINE, X/Twitter)
- **Backgrounds**: Used in slideshows and section headers

### Navigation Structure
- **Fixed header** with coin logo and horizontal nav
- **Mobile hamburger** menu with overlay
- **Consistent footer** across all pages with social links
- **Internal linking**: Home (`#access` anchor), System, Events

## Development Workflow

### CSS Modifications
- **Responsive behavior**: Changes in mobile breakpoints affect layout significantly
- **List styling**: Custom markers using `::before` pseudo-elements (recently removed from pricing details)
- **Animation timing**: CSS transitions typically 0.3s ease

### JavaScript Features
- **Event delegation**: Click handlers with `stopPropagation()` for menu interactions
- **Image management**: Arrays of image objects with src/alt properties
- **State management**: Simple index-based tracking for sliders

### SEO Implementation
- **Meta tags**: Unique per page with Japanese content descriptions
- **Sitemap**: XML sitemap with priority/frequency settings
- **Analytics**: Ready for GA4 integration via `analytics-setup.html`

## Common Tasks

### Adding New Images
1. Add to `/images/` directory
2. Update image arrays in JavaScript (e.g., `sliderImages`)
3. Ensure proper alt text for accessibility

### Modifying Pricing
- Edit `system.html` content within `.pricing-item` containers
- Update corresponding `.pricing-details` for expanded information
- Maintain consistent structure for `toggleDetails()` functionality

### Responsive Adjustments
- Primary breakpoint: `@media (max-width: 900px)` for tablet/mobile
- Secondary: `@media (max-width: 600px)` for small screens
- Always test Google Maps iframe centering in mobile view

## Business Context
- **Location**: Mizonokuchi Station area, Kawasaki City
- **Services**: Poker games, Shisha, Darts, Food & Drinks
- **Hours**: 12:00-24:00 (Café: 12:00-17:00, Bar: 17:00-24:00)
- **Social presence**: X, Instagram, LINE for customer engagement

## Critical Files for Understanding
- `css/style.css` lines 1030-1100: Pricing details component styling
- `index.html` lines 290-400: Image slideshow implementation
- `system.html` lines 370-420: Interactive pricing toggles
- `SEO-CHECKLIST.md`: Comprehensive SEO implementation status
