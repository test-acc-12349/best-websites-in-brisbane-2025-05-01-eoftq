# Brisbane Web Landing Page - Maintenance Guide

This guide will help you maintain and customize the Brisbane Web landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. Change the logo text:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-gray-800">
    Brisbane Web  <!-- Replace this text -->
</a>
```

2. Modify navigation menu items:
```html
<div class="hidden md:flex space-x-8">
    <!-- Each link can be updated here -->
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
```

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    Best Websites In Brisbane  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600">
    Custom Websites For Your Business  <!-- Subheadline -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this page:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-bold`: Makes text bold
- `mb-[size]`: Adds margin bottom (e.g., `mb-4`, `mb-8`)
- `py-[size]`: Adds padding top and bottom
- `bg-[color]`: Sets background color

Example of modifying styles:
```html
<!-- Original -->
<section class="py-24 bg-white">

<!-- To change padding and background -->
<section class="py-16 bg-gray-50">
```

## Managing Links

### Navigation Links
Current navigation links in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update a link:
1. Locate the `<a>` tag
2. Change the `href` attribute
3. Update the text between the tags

Example:
```html
<!-- From -->
<a href="#features">Features</a>

<!-- To -->
<a href="#services">Services</a>
```

### Call-to-Action Buttons
The page has two main CTA buttons:
```html
<!-- Hero section button -->
<a href="https://sigmaseo.io" class="inline-block bg-blue-600 text-white">
    Get Started Today
</a>

<!-- CTA section button -->
<a href="https://sigmaseo.io" class="inline-block bg-white text-blue-600">
    Contact Us Now
</a>
```

To update:
1. Replace `https://sigmaseo.io` with your desired URL
2. Update the button text between the tags

## Adding Privacy and Terms Pages

### Footer Links Setup
Locate the legal section in the footer:
```html
<div>
    <h3 class="text-white text-lg font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To link to privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your website folder
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check that all `href` attributes point to valid pages
   - Ensure internal links (starting with #) match section IDs
   - Test all links after updating

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from Tailwind classes
   - Keep the mobile menu button in the header
   - Test on different screen sizes after making changes

3. **Style Problems**
   - Maintain the existing class structure
   - Don't remove important utility classes like `container` or `mx-auto`
   - Keep padding and margin classes to maintain spacing

### Need Help?
If you encounter issues:
1. Check the Tailwind CSS documentation
2. Verify all changes against the original code
3. Test the page in multiple browsers
4. Ensure all required files (Font Awesome, Tailwind) are properly linked

Remember to always make a backup of your files before making changes!