# FusionPBX Custom Theme v2

## Overview

This repository contains a modernized FusionPBX theme featuring Apple Human Interface Design principles, micro-animations, glass morphism effects, and a responsive widget-based layout. FusionPBX is a web-based multi-tenant PBX system that provides a complete telephony solution with features like call routing, voicemail, conferencing, and call detail records (CDR).

This theme transforms the traditional FusionPBX interface into a modern, Apple-inspired design with smooth animations and contemporary UI patterns.

## What is FusionPBX?

FusionPBX is a full-featured PBX system built on FreeSWITCH that includes:
- Multi-tenant support
- Web-based administration interface
- Call routing and management
- Voicemail system
- Conference calling
- Call detail records (CDR)
- Extension management
- IVR (Interactive Voice Response) systems
- And much more

## Repository Structure

```
fusion-custom-v2/
├── css.php                 # Modern CSS framework with Apple HIG design system
├── template.php            # Updated Smarty template with modern grid layout
├── demo.html              # Standalone demo showcasing modern features
├── MODERN_DESIGN.md       # Comprehensive design system documentation
├── app_config.php         # Theme configuration and settings
├── app_defaults.php       # Default theme settings and background images
├── app_languages.php      # Multi-language support definitions
├── config.php             # UI element definitions (buttons, icons)
├── favicon.ico            # Theme favicon
└── images/                # Theme assets
    ├── backgrounds/       # Background images for the theme
    ├── logo*.png         # Various logo files for different contexts
    ├── icon_cdr_*.png    # Call Detail Record status icons
    └── *.png, *.gif      # Other UI elements and backgrounds
```

## Key Features

### Modern Design System
- **Apple Human Interface Design**: Clean typography, consistent spacing, rounded corners
- **Glass Morphism**: Translucent backgrounds with backdrop blur effects
- **CSS Grid Layout**: Modern 3-column layout (sidebar, main content, widgets)
- **Dark Mode**: Full dark/light mode support with CSS custom properties
- **Micro-animations**: 200ms fade-ins, 100ms button press effects, staggered animations

### Interactive Elements
- **Widget Dashboard**: Modular widgets for system status, stats, and quick actions
- **Responsive Navigation**: Smooth sidebar with hover effects and active states
- **Modern Buttons**: Ripple effects and scaling animations
- **Status Indicators**: Color-coded system status with glow effects

### Technical Features
- **Responsive Design**: Mobile-first approach with breakpoints at 768px and 1200px
- **Performance Optimized**: Hardware-accelerated animations and efficient CSS
- **Accessibility**: Reduced motion support and proper focus indicators
- **Browser Compatibility**: Modern browsers with graceful degradation

## How to Run

### Option 1: FusionPBX Integration

#### Prerequisites
1. **FusionPBX Installation**: This theme requires a working FusionPBX installation
2. **Web Server**: Apache or Nginx with PHP support
3. **PHP**: Version 7.4 or higher
4. **Database**: PostgreSQL (recommended) or MySQL

#### Installing the Theme
1. **Locate FusionPBX Themes Directory**:
   ```bash
   # Typically located at:
   /var/www/fusionpbx/themes/
   # or
   /usr/share/fusionpbx/themes/
   ```

2. **Install the Theme**:
   ```bash
   # Navigate to the themes directory
   cd /var/www/fusionpbx/themes/
   
   # Clone this repository as a new theme
   git clone https://github.com/mikan-senpai/fusion-custom-v2.git custom-v2
   
   # Set proper permissions
   chown -R www-data:www-data custom-v2/
   chmod -R 755 custom-v2/
   ```

3. **Activate the Theme**:
   - Log into FusionPBX web interface as an administrator
   - Navigate to: **Advanced** → **Default Settings**
   - Find the **theme** category
   - Set **template** to `custom-v2`
   - Save the changes

### Option 2: Standalone Demo

1. **Clone the repository**:
   ```bash
   git clone https://github.com/mikan-senpai/fusion-custom-v2.git
   cd fusion-custom-v2
   ```

2. **Start a local web server**:
   ```bash
   python3 -m http.server 8000
   ```

3. **Open your browser and navigate to**:
   ```
   http://localhost:8000/demo.html
   ```

### Option 3: Live Demo
Visit the hosted demo at: `https://work-1-eilxtnhsffrgwbcw.prod-runtime.all-hands.dev/demo.html`

## Interactive Features
- **Dark Mode Toggle**: Click the toggle in the header to switch between light and dark themes
- **Navigation**: Click sidebar items to see smooth active state transitions
- **Buttons**: Hover and click buttons to experience micro-animations and ripple effects
- **Responsive Design**: Resize browser window to see mobile layout adaptations
- **Widget Interactions**: Observe staggered animations and loading states

## Configuration

### Theme Settings

The theme can be customized through the FusionPBX web interface:

1. Go to **Advanced** → **Default Settings**
2. Look for settings in the **theme** category
3. Available customizations include:
   - Background colors and images
   - Menu colors and styles
   - Header customization
   - Font settings
   - Logo customization

### Key Configuration Options

- **Background**: Set custom background colors, gradients, or images
- **Menu Style**: Choose between top, side, or inline menu layouts
- **Colors**: Customize text, link, and UI element colors
- **Logos**: Replace default logos with custom branding
- **Domain Visibility**: Control display of domain information

## Development

### Modern Architecture

The theme uses a modern CSS architecture with:
- **CSS Custom Properties**: Dynamic theming with CSS variables
- **CSS Grid Layout**: Modern 3-column responsive layout
- **Hardware-accelerated Animations**: Transform and opacity-based animations
- **Glass Morphism**: Backdrop-filter effects for modern UI

### File Structure Explanation

- **css.php**: Contains 4000+ lines of modern CSS framework with Apple HIG design system
- **template.php**: Updated Smarty template with modern grid layout and JavaScript interactions
- **demo.html**: Standalone HTML demo showcasing all modern features
- **MODERN_DESIGN.md**: Comprehensive design system documentation
- **app_config.php**: Defines theme metadata and default settings
- **config.php**: Contains UI element definitions and button styles

### Customization

#### Color Customization
Modify CSS custom properties in `css.php`:
```css
:root {
    --primary-blue: #007AFF;        /* Apple's signature blue */
    --background-primary: #F2F2F7;  /* iOS background */
    --spacing-md: 16px;             /* 8-point grid system */
    --duration-normal: 200ms;       /* Animation timing */
}
```

#### Layout Adjustments
Modify grid template in `css.php`:
```css
.modern-layout {
    grid-template-columns: 280px 1fr 320px; /* sidebar, main, widgets */
    grid-template-rows: 80px 1fr;           /* header, content */
}
```

#### Animation Timing
Adjust animation durations:
```css
:root {
    --duration-fast: 100ms;    /* Button press */
    --duration-normal: 200ms;  /* Fade transitions */
    --duration-slow: 300ms;    /* Complex animations */
}
```

### Development Environment

1. **Local Development**:
   ```bash
   # Clone and serve locally
   git clone https://github.com/mikan-senpai/fusion-custom-v2.git
   cd fusion-custom-v2
   python3 -m http.server 8000
   ```

2. **FusionPBX Integration**:
   ```bash
   # Create symbolic link for development
   ln -s /path/to/your/dev/fusion-custom-v2 /var/www/fusionpbx/themes/dev-theme
   ```

3. **Live Reload**: Use browser dev tools to test responsive breakpoints and animations

## Browser Compatibility

### Modern Features Support
- **CSS Grid Layout**: Chrome 57+, Firefox 52+, Safari 10.1+, Edge 16+
- **CSS Custom Properties**: Chrome 49+, Firefox 31+, Safari 9.1+, Edge 15+
- **Backdrop Filter**: Chrome 76+, Firefox 103+, Safari 9+, Edge 79+
- **CSS Animations**: All modern browsers

### Graceful Degradation
- Grid layout falls back to flexbox on older browsers
- Backdrop filter gracefully degrades without blur effect
- Animations respect `prefers-reduced-motion` user preference
- Progressive enhancement ensures basic functionality on all browsers

## License

This theme is licensed under the Mozilla Public License 1.1 (MPL 1.1), the same license as FusionPBX.

## Support

For issues related to:
- **FusionPBX**: Visit [FusionPBX Documentation](https://docs.fusionpbx.com/)
- **This Theme**: Create an issue in this repository

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test with a FusionPBX installation
5. Submit a pull request

## Related Links

- [FusionPBX Official Website](https://www.fusionpbx.com/)
- [FusionPBX Documentation](https://docs.fusionpbx.com/)
- [FusionPBX GitHub Repository](https://github.com/fusionpbx/fusionpbx)
- [FreeSWITCH](https://freeswitch.org/) (underlying telephony engine)