# Landing Page Maintenance Guide

This guide will help you maintain and customize the Hoogwerker Veendam landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the main navigation and logo. To update:

1. **Company Name/Logo**
```html
<!-- Find this line in the header -->
<a href="#" class="text-2xl font-bold text-blue-600">Hoogwerker Veendam</a>
```
- Replace "Hoogwerker Veendam" with your company name
- Adjust text size using `text-2xl` (can be `text-xl` for smaller or `text-3xl` for larger)

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Kenmerken</a>
    <!-- More menu items -->
</div>
```
- Replace "Kenmerken" with your desired menu text
- Keep the `hover:text-blue-600` class for consistent hover effects

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Hoogwerker Huren Veendam</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">Tijdelijk 10% Korting op alle hoogwerkers!</p>
```
- Update heading and promotional text as needed
- Maintain responsive text sizes (`text-4xl`, `md:text-5xl`, `lg:text-6xl`)

### Tailwind CSS Class Guide
Common classes used throughout:
- Text sizes: `text-xl`, `text-2xl`, `text-3xl`, etc.
- Colors: `text-blue-600`, `bg-white`, `text-gray-900`
- Spacing: `px-4`, `py-2`, `mb-6`, `mt-8`
- Responsive prefixes: `md:`, `lg:`, `sm:`

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Kenmerken</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
- These are internal links (marked with #)
- Ensure section IDs match these links exactly

2. Call-to-Action Links:
```html
<a href="https://hansschuiling.nl" class="bg-blue-600 text-white px-6 py-2">Direct Huren</a>
```
- Replace `https://hansschuiling.nl` with your booking URL
- Test all CTA buttons to ensure they point to the correct destination

### Updating Links Step-by-Step
1. Locate the link in the HTML
2. Update the `href` attribute
3. Test the link
4. For internal links, ensure matching section IDs exist

## Linking Privacy and Terms Pages

### Adding Footer Links
Add these links to the footer section:
```html
<div class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-400">
    <p>&copy; 2024 Hoogwerker Huren Veendam. Alle rechten voorbehouden.</p>
    <!-- Add these lines below the copyright notice -->
    <div class="mt-4">
        <a href="/privacy.html" class="text-gray-400 hover:text-white mr-4">Privacy Policy</a>
        <a href="/terms.html" class="text-gray-400 hover:text-white">Terms & Conditions</a>
    </div>
</div>
```

### Creating Policy Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Use the same header and footer as `index.html`
3. Maintain consistent styling using Tailwind classes

## Troubleshooting

Common Issues and Solutions:

1. **Broken Internal Links**
- Check that section IDs match exactly (case-sensitive)
- Ensure # prefix is present for internal links
- Example: `href="#contact"` must match `id="contact"`

2. **Responsive Design Issues**
- Check mobile view using browser dev tools
- Verify responsive classes are correct:
  ```html
  text-base md:text-lg lg:text-xl
  ```
- Test at different screen sizes

3. **Missing Styles**
- Confirm Tailwind CDN is loading
- Check browser console for errors
- Verify class names are spelled correctly

Remember to:
- Always test changes in multiple browsers
- Back up files before making changes
- Keep the original HTML as reference
- Test all links after updates

Need more help? Feel free to refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs) or contact technical support.