# Dream Interpretation Landing Page - Maintenance Guide

This guide will help you maintain and customize the Dream Interpretation landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely.

## 1. Updating Text and Tailwind CSS Classes

### Header Section
```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    DreamGuide
</a>
```
To update the logo text:
1. Locate the above code in the header section
2. Replace "DreamGuide" with your desired text
3. Keep the existing classes to maintain the gradient effect

### Hero Section Text
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    What Does It Mean When You Dream About Someone, Something, or a Place?
</h1>
```
To modify the main headline:
1. Find this `<h1>` tag in the hero section
2. Replace the text between the tags
3. Important classes explained:
   - `text-4xl`: Base font size
   - `md:text-5xl`: Font size on medium screens
   - `lg:text-6xl`: Font size on large screens
   - `mb-8`: Bottom margin spacing

### Feature Cards
Each feature card follows this structure:
```html
<div class="bg-gray-900 rounded-xl p-8 transform hover:scale-105 transition-all duration-300">
    <h3 class="text-xl font-semibold mb-4">500+ Dream Symbols</h3>
    <p class="text-gray-400">Comprehensive database of common dream symbols and their meanings</p>
</div>
```
To update feature cards:
1. Locate the features section (id="features")
2. Modify the `<h3>` text for the title
3. Update the `<p>` text for the description
4. Keep the existing classes for consistent styling

## 2. Fixing Broken Links

### Navigation Menu Links
Current navigation links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
    <a href="mailto:hello@dreamingaboutguide.com" class="text-gray-300 hover:text-white transition-colors duration-300">Contact</a>
</div>
```
To update navigation links:
1. Locate the navigation menu in the header
2. For internal links (starting with #):
   - Ensure the href matches the id of the target section
   - Example: `href="#features"` links to `<section id="features">`
3. For external links:
   - Replace the href with the full URL
   - Example: `href="https://your-site.com/page"`

### Call-to-Action Buttons
```html
<a href="https://dreamingaboutguide.com/blog" class="inline-block bg-gradient-to-r from-purple-500 to-pink-500 text-white font-semibold px-8 py-4 rounded-lg">
    Decode Your Dreams Now
</a>
```
To update CTA buttons:
1. Find the button links in the hero and bottom sections
2. Replace the href attribute with your target URL
3. Update the button text between the tags
4. Maintain the existing classes for styling

## 3. Linking Privacy and Terms Pages

### Footer Link Section
Current placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To add privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the placeholder links in the footer:
```html
<li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting Tips

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Don't remove responsive classes (md:, lg:, etc.)
   - Test on different screen sizes after changes
   - Common responsive classes used:
     - `md:grid-cols-3`: Three columns on medium screens
     - `text-4xl md:text-5xl`: Different text sizes per screen size

3. **Gradient Text Not Showing**
   - Ensure these classes stay together:
     ```html
     bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
     ```

4. **Email Links**
   - Format: `mailto:your-email@domain.com`
   - Update all instances of the email address:
     - Header contact link
     - Footer email address

Remember to:
- Always backup before making changes
- Test all links after updating
- View changes on multiple devices
- Keep consistent styling across sections

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML Links Guide](https://www.w3schools.com/html/html_links.asp)