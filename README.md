# ClassPass Hackathon Project

A mobile fitness/wellness app interface built from Figma design components.

## 🚀 Quick Start

1. **Open the project:**
   - Simply open `index.html` in your browser (shows device mockup on dark background)
   - Or open `screen.html` directly to see just the app
   - No build process needed!

2. **View on mobile:**
   - The `index.html` shows a device mockup (best for presentations)
   - Open browser dev tools (F12) with `screen.html` for mobile testing
   - Toggle device toolbar (Ctrl/Cmd + Shift + M)
   - Select iPhone 12 or similar mobile device

## 📁 Project Structure

```
Hackathon/
├── index.html          # Device mockup showcase (dark background + phone frame)
├── screen.html         # Your actual app (mobile interface)
├── styles.css          # Custom CSS styles for the app
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
4. Update the `src` attributes in `screen.html`

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
Edit `screen.html`. The HTML follows a simple pattern:
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
   - Copy HTML structure into `screen.html`

3. **Add interactivity**:
   - Search functionality
   - Carousel swipe gestures
   - Button click handlers
   - Navigation routing

## 💡 Tips

- Use the browser's device emulator for testing `screen.html`
- Use `index.html` for presentations and demos (dark background + device frame)
- All SVG icons are embedded (no external files needed)
- Tailwind CSS is loaded via CDN for utility classes
- The design is mobile-first (375px width)

## 🎯 What's Working

- ✅ Device mockup presentation (index.html)
- ✅ Mobile app interface (screen.html)
- ✅ Layout and spacing
- ✅ Typography and fonts
- ✅ Colors and gradients
- ✅ Icons and graphics
- ✅ Navigation UI
- ✅ Scrolling carousels
- ✅ Dark background showcase
- ✅ AI-powered schedule generation
- ✅ Real-time API integration
- ✅ Dynamic carousel updates
- ✅ Session tracking with ID
- ✅ Live clock in status bar

## 🤖 AI Schedule Generation

### How It Works:

1. **Click the AI icon** (✨ sparkle) in the "Recommended for you" section
2. **Title changes** to "Generate schedule" (static purple)
3. **Input field appears** with arrow button on the right
4. **Type your request**: e.g., "plan my workout week"
5. **Click the arrow button** (⬆️) or press Enter
6. **API call is made** to the workout generation endpoint
7. **"Thinking..."** shows in the input with animated dots
8. **Title shows** flowing gradient with "Generating schedule..."
9. **Carousel updates** with your personalized workout schedule!

### API Integration:

**Endpoint**: 
```
POST https://chatcoachhackathon.app.n8n.cloud/webhook/a889d2ae-2159-402f-b326-5f61e90f602e/chat
```

**Request Format**:
```json
{
  "action": "sendMessage",
  "chatInput": "user input text",
  "sessionId": "SID-xxxxxxxxxxxx"
}
```

**Response Format**:
```json
{
  "answer": "text response",
  "workout_schedule": [
    {
      "classTitle": "Strength Class",
      "slotLabel": "Mon, 7:00 AM",
      "credits": 5,
      "studio": {
        "name": "Virgin",
        "neighborhood": "Eixample",
        "distance": 1.2,
        "distanceUnit": "km"
      },
      "rating": {
        "average": 4.9,
        "count": 200,
        "badge": "Excellent"
      },
      "thumbnailUrl": "https://..."
    }
  ]
}
```

### Session Tracking:

- **Session ID**: Visible in bottom right corner (dark gray badge)
- **Format**: `SID-xxxxxxxxxxxx` (12 random chars)
- **Accessible**: `window.sessionId` in console
- **Persistent**: Same ID throughout page session
- **Click to copy**: Copy icon (📋) copies session ID to clipboard
- **Selectable**: Can highlight and copy manually

## 📝 Notes

- `index.html` = Main entry point with device mockup on dark background
- `screen.html` = The actual mobile app interface (375x831px)
- The status bar shows **real-time clock** (updates every minute)
- Bottom navigation has 5 tabs (Home, Search, Add Credits, Upcoming, Profile)
- **AI-powered**: Real workout schedule generation via API
- **Dynamic carousel**: Updates automatically with API response
- **Session tracking**: Unique ID for each session

---

**Need help?** Just ask me to:
- Add more sections
- Implement specific features
- Adjust colors or spacing
- Add JavaScript functionality
- Make it responsive for desktop
- Debug API issues

Happy coding! 🚀
