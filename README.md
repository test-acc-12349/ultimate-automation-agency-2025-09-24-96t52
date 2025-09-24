# Ultimate Automation Agency Landing Page - Maintenance Guide

This guide will help you maintain and customize the Ultimate Automation Agency landing page. Whether you're new to web development or need a quick reference, follow these instructions to make updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**: Find this line and replace "UAA":
```html
<div class="text-2xl font-bold text-blue-600">UAA</div>
```

2. **Navigation Menu Items**: Located in the header's `<nav>` section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Find the main headline and subheading in the first `<section>` after `<main>`:
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-gray-900 mb-6">
    Ultimate Automation Agency
</h1>
<p class="text-2xl md:text-3xl text-blue-600 font-semibold mb-8">
    We are the n8n Experts
</p>
```

### Tailwind CSS Classes Explained
Common classes you might need to modify:

- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`
- Colors: `text-blue-600`, `bg-white`, `text-gray-900`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom), `mb-6` (margin bottom)
- Responsive design: Classes starting with `md:` or `lg:` apply at those breakpoints

Example of changing text size and color:
```html
<!-- Original -->
<h1 class="text-5xl text-gray-900">

<!-- Modified -->
<h1 class="text-4xl text-blue-800">
```

## Managing Links

### Identifying Current Links
The page contains several types of links:

1. **Navigation Menu Links** (internal):
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. **Call-to-Action Links** (external):
```html
<!-- Update this URL -->
<a href="https://test.com" class="bg-blue-600 text-white px-6 py-2 rounded-full">
    Get Started
</a>
```

### Updating Links
To update any link:

1. Locate the `<a>` tag
2. Modify the `href` attribute
3. For internal links (same page sections), use `#section-name`
4. For external links, use the full URL

Example:
```html
<!-- Before -->
<a href="https://test.com">Get Started</a>

<!-- After -->
<a href="https://your-actual-domain.com/signup">Get Started</a>
```

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to your policy pages:

1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in IDs
   - IDs should not contain spaces

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Ensure responsive classes (md:, lg:) are correct
   - Test at different screen sizes

3. **Style Changes Not Applying**
   - Verify Tailwind CSS is loading (check network tab)
   - Check for typos in class names
   - Ensure classes are space-separated

### Need Help?
- Use browser developer tools (F12) to inspect elements
- Check the Tailwind CSS documentation for class references
- Verify all changes in multiple browsers
- Test all links after making changes

Remember to always backup your files before making changes, and test thoroughly on a development environment before pushing to production.