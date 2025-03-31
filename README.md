# GovConsult Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the GovConsult landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Company Name and Logo
```html
<!-- Located in the header -->
<div class="text-2xl font-bold">GovConsult</div>
```
To update:
1. Replace "GovConsult" with your company name
2. Adjust text size using Tailwind classes:
   - `text-2xl` (current size)
   - `text-3xl` (larger)
   - `text-xl` (smaller)

### Hero Section Text
```html
<h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">
    Business Consultancy for Government Transactions
</h1>
<p class="text-xl md:text-2xl mb-8 text-gray-200">
    Bright. Precise. Professional. Minimalist
</p>
```
To modify:
1. Replace heading text between `<h1>` tags
2. Update tagline between `<p>` tags
3. Responsive classes explained:
   - `md:text-6xl`: Large text on medium screens and up
   - `text-4xl`: Default size on mobile

### Features Section
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Consultancy</h3>
    <p class="text-gray-600">Expert guidance through complex government procedures...</p>
</div>
```
To customize:
1. Locate each feature card in the features section
2. Update heading text in `<h3>` tags
3. Modify description in `<p>` tags
4. Key styling classes:
   - `shadow-lg`: Adds box shadow
   - `hover:shadow-xl`: Increases shadow on hover
   - `rounded-xl`: Rounds corners
   - `p-8`: Adds padding

## Fixing Broken Links

### Navigation Menu Links
Current structure:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-700 hover:text-gray-900">Features</a>
    <a href="#benefits" class="text-gray-700 hover:text-gray-900">Benefits</a>
    <a href="#faq" class="text-gray-700 hover:text-gray-900">FAQ</a>
</div>
```
To update:
1. Internal links (current page sections):
   - Keep the `#` prefix
   - Match the `id` of the target section
   - Example: `href="#features"` links to `<section id="features">`

2. External links:
   - Replace `href="https://stripe.com/checkout"` with your payment or service URL
   - Always include `https://` for external links

### Contact Email Link
```html
<a href="mailto:perezdenmar@gmail.com">Contact Us</a>
```
To modify:
1. Replace `perezdenmar@gmail.com` with your business email
2. Keep the `mailto:` prefix

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy policy page (e.g., `privacy.html`)
2. Create your terms page (e.g., `terms.html`)
3. Update the links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section `id` attributes match link `href` values
   - Check for typos in both the link and section ID
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify `md:` prefixed classes are working
   - Common classes to check:
     - `hidden md:flex`: Shows element on desktop only
     - `md:w-1/2`: Sets width on medium screens

3. **Image Loading Problems**
   - Verify image URLs are correct
   - Check image paths are relative to your HTML file
   - Ensure images exist at the specified URLs

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12 key)
2. Verify all files are in the correct directory
3. Test links in multiple browsers
4. Ensure all Tailwind CSS classes are spelled correctly

Remember to always backup your files before making changes, and test your modifications in multiple browsers and screen sizes.