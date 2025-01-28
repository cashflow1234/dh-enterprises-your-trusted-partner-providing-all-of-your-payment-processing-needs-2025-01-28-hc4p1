# DH Enterprises Landing Page - Maintenance Guide

This guide will help you maintain and customize the DH Enterprises landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu:
```html
<div class="text-2xl font-bold text-blue-600">DH Enterprises</div>
```
To change the company name:
1. Locate this div in the header section
2. Replace "DH Enterprises" with your desired text
3. Adjust size using `text-2xl` (options: text-sm, text-lg, text-3xl, etc.)
4. Modify color using `text-blue-600` (options: text-red-600, text-green-600, etc.)

### Hero Section
The main headline is located in:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">
    Your Trusted Partner Providing All of Your Payment Processing Needs
</h1>
```
To modify:
1. Change the text between the `<h1>` tags
2. Adjust responsive sizes:
   - `text-4xl`: Mobile size
   - `md:text-5xl`: Tablet size
   - `lg:text-6xl`: Desktop size

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold text-gray-900 mb-4">Feature Title</h3>
    <p class="text-gray-600">Feature description text.</p>
</div>
```
To update:
1. Find the feature card you want to modify
2. Change the title text in the `<h3>` tag
3. Update the description in the `<p>` tag
4. Modify colors using Tailwind classes:
   - Background: `bg-white`
   - Text: `text-gray-900`, `text-gray-600`
   - Icon background: `bg-blue-100`

## Fixing Broken Links

### Navigation Menu Links
Current navigation links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```
To update:
1. Locate the link you want to change
2. Modify the `href` attribute:
   - Internal sections: Use `#section-id`
   - External pages: Use full URL (e.g., `https://example.com`)

### Contact Links
Current contact links:
```html
<a href="mailto:cashflowinvest@pm.me">Email Us</a>
<a href="https://form.typeform.com/to/lGiUJKtP">Get Started</a>
```
To update:
1. Replace `cashflowinvest@pm.me` with your email address
2. Replace the Typeform URL with your form URL

## Linking Privacy and Terms Pages

### Footer Links
Current placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```
To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Layout**
   - Check for missing closing tags
   - Verify all div containers are properly nested
   - Ensure Tailwind CSS is loading (check the `<head>` section)

2. **Non-Working Links**
   - Verify file paths are correct
   - Check for typos in URLs
   - Ensure section IDs match href attributes

3. **Responsive Issues**
   - Check media query classes (md:, lg:)
   - Test on different devices
   - Verify container widths

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools (F12) to inspect elements
- Double-check HTML syntax and nesting

Remember to always test your changes across different devices and browsers before publishing updates.