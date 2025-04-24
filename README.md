# Alphington Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Alphington Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Hero Section
Located near the top of the page, find this section:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    We transform numbers into opportunities
</h1>
```
To modify:
1. Locate the text between the `<h1>` tags
2. Replace with your desired heading
3. Maintain the existing classes to preserve styling

#### Services Section
Find the service cards in the grid:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition duration-300">
    <h3 class="text-xl font-bold mb-4">Dedicated Manager</h3>
    <p class="text-gray-600">Your personal financial expert...</p>
</div>
```
To update:
1. Locate each service card within the `services` section
2. Modify the `<h3>` title and `<p>` description
3. Keep the class attributes unchanged

### Tailwind CSS Modifications

#### Understanding Key Classes
- `container mx-auto`: Centers content with automatic margins
- `px-6`: Adds horizontal padding (left and right)
- `py-4`: Adds vertical padding (top and bottom)
- `text-4xl`: Sets large text size
- `md:text-5xl`: Changes text size on medium screens
- `bg-white`: Sets white background
- `rounded-xl`: Adds rounded corners

#### Responsive Design Classes
Example of responsive navigation:
```html
<div class="hidden md:flex space-x-8">
```
- `hidden`: Hides element by default
- `md:flex`: Shows element as flex container on medium screens
- `space-x-8`: Adds horizontal spacing between items

## Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update internal links:
1. Locate the `href` attribute
2. Ensure it matches the `id` of the target section
3. For external links, replace with full URL:
```html
<a href="https://your-domain.com/services">Services</a>
```

### Call-to-Action Links
Find the "Get Started" buttons:
```html
<a href="https://theaccountants.com" class="inline-block px-8 py-4 bg-blue-600...">
```
Replace `https://theaccountants.com` with your actual URL.

## Linking Privacy and Terms Pages

### Footer Links Section
Locate the Legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Replace the `#` placeholder:
```html
<li><a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```
2. Ensure privacy.html and terms.html exist in your root directory
3. Maintain consistent styling by keeping the existing classes

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - Example: `href="#services"` must match `id="services"`

2. **Responsive Design Problems**
   - Verify Tailwind breakpoint classes are correct:
     - `md:` for medium screens (768px+)
     - `lg:` for large screens (1024px+)

3. **Missing Icons**
   - Ensure Font Awesome script is properly linked:
   ```html
   <script src="https://kit.fontawesome.com/your-code.js" crossorigin="anonymous"></script>
   ```
   - Replace `your-code.js` with your actual Font Awesome kit code

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify HTML validity using [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always backup your files before making changes and test on multiple devices and browsers after updates.