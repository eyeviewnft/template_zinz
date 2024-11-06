# Zinz viewer template
Zinz stands for Zora in Zora.
A template to create stories like post on zora as a responsive, touch-enabled slideshow viewer for displaying a series of images with progress bars, navigation controls, and optional clickable links. It includes smooth transitions, automatic progression, and a clean, modern design.

Made to allow multi content posts, rewinds, curation and anything you want.

## Features
- Displays a sequence of images with progress bars
- Automatic progression through the slides
- Navigation buttons for manual slide navigation
- Responsive design adaptable to various screen sizes
- Clean, modern UI with customizable styles
- Optional clickable link at the bottom of each slide

## Usage

### 1. Basic Setup
1. Copy the template code into an HTML file.
2. Replace placeholder values marked with `{{PLACEHOLDER}}` syntax.
3. Duplicate content sections for each slide to display.

### 2. Placeholder Values
Replace the following placeholders in the template:
- `{{TITLE}}`: Title shown in the top-left corner
- `{{IMAGE_URL}}`: URL of the image to display
- `{{IMAGE_ALT}}`: Alt text for the image
- `{{LINK_URL}}`: URL that the bottom button links to (optional)
- `{{BUTTON_TEXT}}`: Text shown on the bottom button (optional)

### 3. Adding Multiple Slides
To add more slides, duplicate the respective sections as shown below.

#### Progress Bar
Duplicate the progress bar `div` within the `zinz-progress` section for each slide:
```html
<div class="zinz-progress">
    <div class="progress-bar">
        <div class="progress-bar-fill"></div>
    </div>
    <!-- Duplicate for each slide -->
</div>
```

## Slide Content
To add multiple slides, duplicate the `zinz-content` div within the `zinz-track` section for each slide:

```html
<div class="zinz-track" id="zinzTrack">
    <div class="zinz-content" data-link="{{LINK_URL}}" data-text="{{BUTTON_TEXT}}">
        <img src="{{IMAGE_URL}}" alt="{{IMAGE_ALT}}" class="zinz-image">
    </div>
    <!-- Duplicate for each slide -->
</div>
```

## Navigation Dots
To add navigation dots, duplicate the zinz-dot div within the zinz-overlay section for each slide:

```html
Copier le code
<div class="zinz-overlay">
    <div class="zinz-dot"></div>
    <!-- Duplicate for each slide -->
</div>
```

## Customization Options
# Images
- Web images: Use any image from the web by providing its link
- Zora posts images: Use any zora post image by providing its link (right-click on it and "Open image in a new tab")
- IPFS images: Use a IPFS storing tool to store image on it and provide gateway link to it

# Timing
- Slide duration: Modify the 5000 value (in milliseconds) in the JavaScript setTimeout call.
- Progress bar duration: Adjust the 5s value in the progressAnimation CSS animation.

# Styling
- Container width: Change max-width in .zinz-container.
# Colors:
- Progress bar: Change background in .progress-bar-fill.
- Navigation buttons: Change background in .nav-button.
- Bottom link: Change background-color in .bottom-link (if used).
- Transitions: Modify transition properties in .zinz-track and .zinz-content.

# Feature Options
- Disable auto-progression: Remove the setTimeout call in the showZinz function.
- Disable navigation buttons: Remove the .navigation-buttons section.
- Disable progress bars: Remove the .zinz-progress section.
- Remove the bottom link button: Use the template without the link button.

## Example Usage
# With Bottom Link Button
```html
Copier le code
<div class="zinz-content" data-link="https://example.com/item1" data-text="View Item 1">
    <img src="https://example.com/image1.jpg" alt="Item 1" class="zinz-image">
</div>
<div class="zinz-content" data-link="https://example.com/item2" data-text="View Item 2">
    <img src="https://example.com/image2.jpg" alt="Item 2" class="zinz-image">
</div>
```
# Without Bottom Link Button
```html
Copier le code
<div class="zinz-content">
    <img src="https://example.com/image1.jpg" alt="Item 1" class="zinz-image">
</div>
<div class="zinz-content">
    <img src="https://example.com/image2.jpg" alt="Item 2" class="zinz-image">
</div>
```

## Browser Support
The Zinz Viewer leverages modern CSS features, such as backdrop-filter. It supports all modern browsers (Chrome, Firefox, Safari, Edge). For older browsers, consider adding relevant vendor prefixes or fallbacks to ensure compatibility.
