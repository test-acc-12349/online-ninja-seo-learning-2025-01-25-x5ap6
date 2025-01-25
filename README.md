# Ninja SEO Landing Page - Maintenance Guide

This guide will help you maintain and customize the Ninja SEO landing page. Whether you're new to HTML and CSS or just getting started, follow these instructions to make updates while preserving the design integrity.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this section near the top -->
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">
    Ninja SEO  <!-- Change this text to update the logo -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <!-- Edit these link texts as needed -->
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors">Características</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors">Beneficios</a>
```

### Hero Section
The main headline and call-to-action section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">
    Multiplica tu Tráfico SEO x10  <!-- Edit this headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Domina el arte del SEO con nuestro programa de aprendizaje online  <!-- Edit this subheading -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this page:

- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-[size]`: Margin bottom (e.g., `mb-8`, `mb-12`)
- `px-[size]`: Horizontal padding (e.g., `px-6`)
- `py-[size]`: Vertical padding (e.g., `py-4`)
- `md:`: Applies styles on medium screens and up

## Managing Links

### Navigation Menu Links
Current internal links that need attention:

```html
<!-- In the header navigation -->
<div class="hidden md:flex space-x-8">
    <a href="#features">Características</a>
    <a href="#benefits">Beneficios</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contacto</a>
</div>
```

To update these links:
1. For internal sections, keep the `#` prefix (e.g., `#features`)
2. For external pages, use the full URL (e.g., `https://example.com`)

### Call-to-Action Buttons
Update the main CTA buttons:

```html
<!-- Main CTA button -->
<a href="https://ninja200.online" class="inline-block px-8 py-4 text-lg font-semibold text-white bg-gradient-to-r from-purple-600 to-blue-500 rounded-full shadow-lg hover:shadow-xl transform hover:scale-105 transition-all duration-300">
    Comienza Ahora
</a>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <!-- Update these href attributes -->
        <li><a href="privacy.html" class="hover:text-white transition-colors">Privacidad</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors">Términos</a></li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check that all `href` attributes have correct paths
   - Verify that linked files exist in the correct directory
   - Test all links after updating

2. **Responsive Design Issues**
   - Keep the `md:` prefix for medium-screen styles
   - Don't remove responsive classes like `text-4xl md:text-5xl`
   - Test on multiple screen sizes after making changes

3. **Gradient Text Not Showing**
   - Ensure these classes remain together:
     ```html
     bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent
     ```

### Need Help?
If you encounter issues:
1. Check the HTML structure remains intact
2. Verify all opening tags have matching closing tags
3. Test the page in multiple browsers
4. Ensure Tailwind CSS CDN link remains in the header

Remember to always backup your files before making changes, and test thoroughly after each update.