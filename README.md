# EagleiO Landing Page Maintenance Guide

This guide will help you maintain and customize the EagleiO landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent">EagleiO</a>
```
- Replace "EagleiO" with your desired text
- Keep the classes to maintain the gradient effect

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <!-- Add or modify menu items here -->
</div>
```
- `hidden md:flex` means the menu is hidden on mobile and visible on medium screens
- `space-x-8` adds horizontal spacing between items

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent">Soar Above Service Hassles with EagleiO</h1>
```
- `text-4xl` sets base font size
- `md:text-5xl` and `lg:text-6xl` increase size on larger screens
- Maintain the gradient classes for consistent styling

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-800 rounded-2xl p-8 hover:bg-gray-750 transition-all duration-300 transform hover:scale-105 hover:shadow-xl hover:shadow-blue-500/10">
    <!-- Icon container -->
    <div class="w-16 h-16 bg-gradient-to-br from-blue-500 to-teal-400 rounded-xl mb-6">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-400">Feature description</p>
</div>
```

## Fixing Broken Links

### Current Link Structure
1. **Navigation Links:**
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://eagle360.app">Get Started</a>
```
- Internal links use "#" followed by section ID
- External links use full URLs

### Updating Links
1. **Internal Links:**
```html
<!-- Find section IDs in the HTML -->
<section id="features">
<section id="benefits">
<section id="faq">
```
- Ensure section IDs match navigation href attributes
- Example: `<a href="#features">` links to `<section id="features">`

2. **External Links:**
```html
<!-- Replace placeholder URL -->
<a href="https://eagle360.app" class="...">Get Started</a>
```
- Update all instances of "https://eagle360.app" with your actual URL
- Search for this URL throughout the document

## Linking Privacy and Terms Pages

### Footer Links
Located in the footer section:
```html
<!-- Find these lines -->
<ul class="space-y-4">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To update:
1. Replace the "#" with proper paths:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Gradients:**
- Ensure all gradient classes remain intact:
  ```html
  bg-gradient-to-r from-blue-500 to-teal-400
  ```
- Don't remove `bg-clip-text` or `text-transparent` when updating text

2. **Responsive Issues:**
- Keep responsive classes:
  - `md:` prefix for medium screens
  - `lg:` prefix for large screens
- Example: `text-4xl md:text-5xl lg:text-6xl`

3. **Missing Hover Effects:**
- Maintain hover classes:
  ```html
  hover:text-white
  hover:scale-105
  hover:shadow-xl
  ```

### Best Practices
- Always test changes across different screen sizes
- Keep the existing class structure when adding new elements
- Maintain consistent spacing using Tailwind's spacing classes
- Back up the file before making changes

Remember to validate all links and test the page thoroughly after making any modifications.