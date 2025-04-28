# 101Headshots Landing Page - Maintenance Guide

This guide will help you maintain and customize the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
```html
<header class="fixed w-full z-50 bg-gray-900/95 backdrop-blur-sm border-b border-gray-800">
    <nav class="container mx-auto px-6 py-4">
        <a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
            101Headshots
        </a>
```
To update:
- Change company name: Replace "101Headshots" with your brand name
- Modify colors: Update gradient colors by changing `from-purple-500` and `to-pink-500`
- Adjust spacing: Modify `px-6 py-4` for different padding

### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Raytown, Missouri Corporate Headshot Photography Services
</h1>
```
To update:
- Change heading: Replace text between `<h1>` tags
- Adjust text size: Modify `text-4xl md:text-5xl lg:text-6xl`
  - `text-4xl`: Mobile size
  - `md:text-5xl`: Tablet size
  - `lg:text-6xl`: Desktop size

### Features Cards
Each feature card follows this structure:
```html
<div class="bg-gray-900 rounded-2xl p-8 hover:scale-105 transform transition duration-300">
    <h3 class="text-xl font-semibold mb-4">Trust Poses</h3>
    <p class="text-gray-400">Professional poses that convey confidence</p>
</div>
```
To update:
- Change feature title: Modify text in `<h3>` tags
- Update description: Change text in `<p>` tags
- Adjust card styling:
  - Background color: Change `bg-gray-900`
  - Padding: Modify `p-8`
  - Hover effect: Adjust `hover:scale-105`

## Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white">Benefits</a>
    <a href="#contact" class="px-6 py-2 bg-gradient-to-r from-purple-600 to-pink-600">Book Now</a>
</div>
```
To update:
1. Internal links (sections on same page):
   - Keep the `#` prefix
   - Ensure ID matches section: `href="#sectionId"`
2. External links:
   - Replace `#contact` with full URL: `href="https://example.com/contact"`
   - Update "Book Now" button URL in multiple locations

### Email Links
```html
<a href="mailto:bryan@101headshots.com">bryan@101headshots.com</a>
```
To update:
1. Replace email address in both:
   - `href="mailto:your-email@domain.com"`
   - Link text between `<a>` tags

## Linking Privacy and Terms Pages

### Footer Legal Links
Current structure:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```
To add proper links:
1. Create privacy.html and terms.html in same directory
2. Update href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. Broken Internal Links
- Check that section IDs match exactly (case-sensitive)
- Verify `href` attributes include `#` prefix
- Example: `<section id="features">` matches `href="#features"`

2. Responsive Design Issues
- Always include mobile-first classes without prefix
- Add tablet (`md:`) and desktop (`lg:`) variants
- Example: `class="text-sm md:text-base lg:text-lg"`

3. Gradient Text Not Showing
```html
<!-- Required classes for gradient text -->
class="bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent"
```

4. Hover Effects Not Working
- Ensure all classes are spelled correctly
- Check that `hover:` prefix is included
- Verify parent elements aren't blocking interactions

Remember to:
- Test all changes across different screen sizes
- Validate links before deploying
- Keep consistent styling throughout the page
- Back up files before making major changes

Need more help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).