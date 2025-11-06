# ClassPass Hackathon Project

A mobile fitness/wellness app interface built from Figma design components.

## 🚀 Quick Start

1. **Open the project:**
   - Simply open `index.html` in your browser
   - No build process needed!

2. **View on mobile:**
   - Open browser dev tools (F12)
   - Toggle device toolbar (Ctrl/Cmd + Shift + M)
   - Select iPhone 12 or similar mobile device

## 📁 Project Structure

```
Hackathon/
├── index.html          # Main HTML file
├── styles.css          # Custom CSS styles
└── README.md          # This file
```

## 🎨 Design System

### Colors
- **Primary**: Black (#000000)
- **Background**: Light Gray (#F5F5F5)
- **Accent**: Light Blue (#E6F3FF)
- **Text Gray**: #676767

### Typography
- **Font**: Inter (Google Fonts)
- **Sizes**: 12px, 14px, 16px, 20px, 32px

### Spacing
- Small: 8px
- Medium: 16px
- Large: 20px
- Extra Large: 24px

## 🖼️ Adding Your Images

Currently using placeholder images. Replace them with your actual images:

### Venue/Class Images (164x110px):
- Sweat440
- The Fhitting Room
- Mile High Run Club
- [solidcore]
- Barry's
- Y7
- etc.

### Promo Card Images (127x116px):
- Referral card image
- Other promotional graphics

### Profile Images (36x36px, 80x80px):
- User avatars
- Venue logos

**How to add images:**
1. Create an `assets/images/` folder
2. Export your images from Figma
3. Save them in the assets folder
4. Update the `src` attributes in `index.html`

Example:
```html
<!-- Before -->
<img src="https://placehold.co/164x110" alt="Sweat440">

<!-- After -->
<img src="assets/images/sweat440.jpg" alt="Sweat440">
```

## 🛠️ Customization

### Changing Colors
Edit the CSS variables in `styles.css`:
```css
:root {
    --color-primary: #000000;
    --color-blue-light: #E6F3FF;
    /* Add more custom colors */
}
```

### Adding More Sections
The HTML follows a simple pattern:
```html
<section class="section">
    <div class="section-header">
        <h2>Section Title</h2>
    </div>
    <!-- Your content here -->
</section>
```

### Carousel Cards
To add more carousel items:
```html
<div class="carousel-card">
    <img src="your-image.jpg" alt="Venue Name" class="carousel-img">
    <div class="carousel-content">
        <h3>Venue Name</h3>
        <p class="location">Location · Distance</p>
        <p class="tags">Category Tags</p>
        <div class="rating">
            <!-- Rating content -->
        </div>
    </div>
</div>
```

## 📱 Features Included

- ✅ iPhone-style status bar
- ✅ Search functionality (UI ready)
- ✅ Horizontal scrolling carousels
- ✅ Promo/referral cards
- ✅ Bottom navigation tabs
- ✅ Responsive design
- ✅ Smooth scrolling
- ✅ Modern UI with shadows and rounded corners

## 🔄 Next Steps from Figma

1. **Export all assets** from your Figma file:
   - Images → PNG/JPG at 2x resolution
   - Icons → SVG format (already included)
   - Logo → SVG or PNG

2. **Copy additional components** you want:
   - Select component in Figma Dev Mode
   - Copy CSS from the Code panel
   - Paste into `styles.css`
   - Copy HTML structure into `index.html`

3. **Add interactivity**:
   - Search functionality
   - Carousel swipe gestures
   - Button click handlers
   - Navigation routing

## 💡 Tips

- Use the browser's device emulator for testing
- All SVG icons are embedded (no external files needed)
- Tailwind CSS is loaded via CDN for utility classes
- The design is mobile-first (375px width)

## 🎯 What's Working

- ✅ Layout and spacing
- ✅ Typography and fonts
- ✅ Colors and gradients
- ✅ Icons and graphics
- ✅ Navigation UI
- ✅ Scrolling carousels

## 📝 Notes

- The status bar mimics iPhone 12 design
- Bottom navigation has 5 tabs (Home, Search, Add Credits, Upcoming, Profile)
- Currently showing placeholder content
- Ready for you to add real data and functionality!

---

**Need help?** Just ask me to:
- Add more sections
- Implement specific features
- Adjust colors or spacing
- Add JavaScript functionality
- Make it responsive for desktop

Happy coding! 🚀
