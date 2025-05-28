# FusionPBX Custom Theme v2

## Overview

This repository contains a custom theme for FusionPBX, an open-source VoIP (Voice over IP) PBX system. FusionPBX is a web-based multi-tenant PBX system that provides a complete telephony solution with features like call routing, voicemail, conferencing, and call detail records (CDR).

This theme provides a modern, customizable user interface for the FusionPBX web administration panel and user portal.

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
├── app_config.php          # Theme configuration and settings
├── app_defaults.php        # Default theme settings and background images
├── app_languages.php       # Multi-language support definitions
├── config.php              # UI element definitions (buttons, icons)
├── css.php                 # Dynamic CSS generation with theme variables
├── template.php            # Main Smarty template file
├── favicon.ico             # Theme favicon
└── images/                 # Theme assets
    ├── backgrounds/        # Background images for the theme
    ├── logo*.png          # Various logo files for different contexts
    ├── icon_cdr_*.png     # Call Detail Record status icons
    └── *.png, *.gif       # Other UI elements and backgrounds
```

## Key Features

- **Responsive Design**: Modern, mobile-friendly interface
- **Customizable Colors**: Extensive color customization options
- **Multiple Background Options**: Various background images and colors
- **CDR Icons**: Visual indicators for different call statuses (answered, missed, failed, etc.)
- **Multi-language Support**: Internationalization support
- **Bootstrap Integration**: Uses Bootstrap framework for consistent styling
- **FontAwesome Icons**: Modern icon set integration

## Installation

### Prerequisites

1. **FusionPBX Installation**: This theme requires a working FusionPBX installation
2. **Web Server**: Apache or Nginx with PHP support
3. **PHP**: Version 7.4 or higher
4. **Database**: PostgreSQL (recommended) or MySQL

### Installing the Theme

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

4. **Clear Cache** (if applicable):
   ```bash
   # Clear any cached files
   rm -rf /var/cache/fusionpbx/*
   ```

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

### File Structure Explanation

- **template.php**: Main Smarty template that defines the HTML structure
- **css.php**: Dynamic CSS file that reads theme settings and generates styles
- **app_config.php**: Defines theme metadata and default settings
- **config.php**: Contains UI element definitions and button styles

### Customization

To customize the theme:

1. **Modify CSS**: Edit `css.php` to change styles
2. **Update Template**: Modify `template.php` for structural changes
3. **Add Images**: Place custom images in the `images/` directory
4. **Configure Settings**: Update `app_config.php` for new theme options

### Development Environment

For development, you can:

1. Set up a local FusionPBX development environment
2. Create a symbolic link to your development directory:
   ```bash
   ln -s /path/to/your/dev/fusion-custom-v2 /var/www/fusionpbx/themes/dev-theme
   ```
3. Activate the development theme in FusionPBX settings

## Browser Compatibility

This theme supports:
- Chrome/Chromium (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Internet Explorer 11+ (limited support)

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