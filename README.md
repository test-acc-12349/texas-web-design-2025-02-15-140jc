# Texas Web Design Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Texas Web Design landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<div class="text-2xl font-bold text-blue-600">
    <a href="/" class="flex items-center space-x-2">
        <i class="fas fa-globe"></i>
        <span>Texas Web Design</span> <!-- Edit this text -->
    </a>
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a> <!-- Edit menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
To modify the main headline and subtext:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Best Websites In Texas <!-- Edit main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    Professional web design solutions... <!-- Edit subheading -->
</p>
```

### Tailwind CSS Tips
- Font sizes use classes like `text-xl`, `text-2xl`, etc.
- Colors use format `text-{color}-{shade}` (e.g., `text-blue-600`)
- Spacing uses format `m-{size}` for margin or `p-{size}` for padding
- Responsive classes start with screen sizes: `md:` or `lg:`

Example of modifying button styling:
```html
<!-- Original -->
<a href="https://twd.com" class="bg-blue-600 text-white px-8 py-4 rounded-full">

<!-- To change color to red -->
<a href="https://twd.com" class="bg-red-600 text-white px-8 py-4 rounded-full">
```

## Managing Links

### Navigation Links
Current navigation links are internal anchor links. To update:

1. **Internal Links:**
```html
<a href="#features">Features</a> <!-- Links to section on same page -->
```

2. **External Links:**
```html
<a href="https://twd.com" class="hidden md:block bg-blue-600">
    Get Started
</a>
```

### Updating Links Step-by-Step:
1. Locate the `<a>` tag you want to modify
2. Change the `href` attribute value
3. For internal sections, use `#section-id`
4. For external pages, use complete URLs starting with `https://`

Example:
```html
<!-- Before -->
<a href="https://twd.com">Get Started</a>

<!-- After -->
<a href="https://your-new-domain.com">Get Started</a>
```

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the legal section in the footer:

```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to new pages:
1. Create `privacy.html` and `terms.html` in your project directory
2. Update the href attributes:

```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match href values
   - Check for typos in IDs
   - Verify that sections have the correct ID attribute

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify media query classes (md:, lg:) are correct
   - Test different screen sizes

3. **Style Changes Not Applying**
   - Confirm Tailwind CSS is properly loaded
   - Check class name spelling
   - Verify class order (more specific classes should come later)

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify Font Awesome icons are loading properly
- Test all links in multiple browsers
- Use browser developer tools to inspect elements

Remember to always test your changes across different devices and browsers before deploying to production.