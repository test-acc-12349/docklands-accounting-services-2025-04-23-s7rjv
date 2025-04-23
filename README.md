# Docklands Landing Page Maintenance Guide

This guide will help you maintain and customize the Docklands Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To modify:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Docklands <!-- Replace this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a> <!-- Replace menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
The main landing section includes:

1. **Main Heading:**
```html
<h1 class="text-4xl md:text-5xl lg:text-7xl font-bold leading-tight bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent mb-6">
    Docklands accounting services <!-- Update heading here -->
</h1>
```

2. **Subheading:**
```html
<p class="text-xl md:text-2xl text-gray-300 mb-10">
    Partners in your financial journey <!-- Update subheading here -->
</p>
```

### Understanding Tailwind Classes
Key classes explained:
- `text-4xl`: Large text (increases with screen size)
- `md:text-5xl`: Medium screen text size
- `bg-gray-900`: Dark background color
- `text-gray-100`: Light text color
- `hover:scale-105`: Enlarges element on hover
- `transition-transform`: Smooth animation effects

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://theaccountants.com" class="...">
    Get Started
</a>
```

### Updating Links
1. To update internal section links:
- Ensure the `href` matches the section's `id` attribute
- Example: `<a href="#features">` links to `<section id="features">`

2. To update external links:
```html
<!-- Replace https://theaccountants.com with your desired URL -->
<a href="https://your-new-url.com" class="...">
```

## Linking Privacy and Terms Pages

### Current Footer Structure
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Adding Privacy and Terms Links
1. Create your privacy.html and terms.html files
2. Update the footer links:
```html
<ul class="space-y-2">
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Check that section IDs match exactly with href attributes
- Example: `href="#features"` must match `id="features"`
- IDs are case-sensitive

2. **Responsive Design Issues**
- Verify mobile classes are present:
  ```html
  class="text-4xl md:text-5xl lg:text-7xl"
  ```
- Test on different screen sizes using browser dev tools

3. **Gradient Text Not Showing**
- Ensure all three classes are present:
  ```html
  class="bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent"
  ```

### Best Practices
- Always test changes in multiple browsers
- Keep consistent spacing in the HTML structure
- Maintain the existing color scheme (purple/pink gradients)
- Preserve responsive design classes (`md:`, `lg:` prefixes)

Remember to backup your files before making any changes, and test thoroughly on different devices and browsers after modifications.