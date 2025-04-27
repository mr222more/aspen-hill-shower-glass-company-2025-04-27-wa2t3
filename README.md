# Aspen Hill Shower Glass Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Aspen Hill Shower Glass landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-gray-800 hover:text-blue-600 transition duration-300">
    Aspen Hill Glass
</a>
```
Simply replace "Aspen Hill Glass" with your desired company name.

### Hero Section
The main banner section contains your primary headline and call-to-action:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">
    Anti-scratch shower glass that lasts
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Premium shower enclosures engineered for durability and elegance
</p>
```

**Understanding the Tailwind Classes:**
- `text-4xl`: Base font size
- `md:text-5xl`: Font size on medium screens
- `lg:text-6xl`: Font size on large screens
- `mb-8`: Margin bottom spacing (2rem)

### Modifying Responsive Design
When updating Tailwind classes, maintain the responsive prefixes:
- `sm:` (640px and up)
- `md:` (768px and up)
- `lg:` (1024px and up)

Example:
```html
<!-- Original -->
<div class="text-xl md:text-2xl">

<!-- To make text smaller on mobile but larger on desktop -->
<div class="text-lg md:text-xl lg:text-2xl">
```

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition duration-300">Contact</a>
</div>
```

To update these links:
1. For internal section links, ensure the `href` matches the section's `id` attribute
2. For external links, replace the `href` with the full URL
3. Always include `https://` for external links

### External Links to Update
Current external links that need attention:
```html
<!-- Quote button link -->
<a href="http://www.customeuroglass.com" class="inline-block bg-blue-600...">

<!-- Email link -->
<a href="mailto:info@customeuroglass.com" class="hover:text-white...">
```

Replace these with your actual website and email addresses.

## Linking Privacy and Terms Pages

### Footer Privacy and Terms Links
Located in the footer section:

```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to your policy pages:

1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - Check for typos in IDs
   ```html
   <!-- Example: This won't work -->
   <a href="#FAQ">FAQ</a>
   <section id="faq">...</section>
   ```

2. **Responsive Design Issues**
   - Always maintain the responsive class pattern:
   ```html
   class="base-style sm:medium-style lg:large-style"
   ```
   - Don't remove responsive prefixes without understanding their impact

3. **Image Loading Problems**
   - Verify image URLs are correct and accessible
   - Include proper alt text for accessibility
   ```html
   <img src="path/to/image.jpg" alt="Descriptive text" class="...">
   ```

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all file paths are correct
3. Ensure all HTML tags are properly closed
4. Maintain the existing class structure when making changes

Remember to test all changes across different screen sizes using browser developer tools.