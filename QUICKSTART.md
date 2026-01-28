# Quick Start Guide - Four Card Feature Section

## Get Started in 3 Steps

### 1. Open the Project
Simply open `index.html` in your web browser:
- Double-click `index.html`
- Or drag it into your browser
- Or use a local server (recommended)

### 2. View the Design
The page will display a responsive four-card feature section that adapts to your screen size:
- **Mobile**: Resize to < 768px
- **Tablet**: Resize to 768px - 1439px
- **Desktop**: Resize to ≥ 1440px

### 3. Make Changes (Optional)
If you want to customize the design:

#### Edit Sass Files
1. Navigate to `sass/` folder
2. Edit any `.scss` file:
   - `abstracts/_variables.scss` - Colors, fonts, spacing
   - `components/_card.scss` - Card styles
   - `components/_feature-section.scss` - Layout
3. Compile Sass to CSS:
   ```bash
   sass sass/main.scss style.css --no-source-map
   ```

#### Edit HTML
1. Open `index.html` in your text editor
2. Modify content as needed
3. Save and refresh browser

## File Structure

```
├── index.html              ← Open this file
├── style.css               ← Generated from Sass
├── images/                 ← Icons and images
└── sass/                   ← Edit these for styling
    ├── abstracts/          ← Variables & mixins
    ├── base/               ← Reset & typography
    ├── layout/             ← Page layout
    └── components/         ← Card & section styles
```

## Development Commands

### Compile Sass (One-time)
```bash
sass sass/main.scss style.css --no-source-map
```

### Watch Mode (Auto-compile on save)
```bash
sass --watch sass/main.scss:style.css
```

### Using npm
```bash
npm run build:css    # One-time compile
npm run watch:css    # Watch mode
```

## Customization Quick Reference

### Change Colors
Edit `sass/abstracts/_variables.scss`:
```scss
$color-primary-red: #EA5454;    // Your color
$color-primary-cyan: #44D3D2;   // Your color
// etc.
```

### Change Spacing
Edit `sass/abstracts/_variables.scss`:
```scss
$spacing-400: 2rem;  // Adjust spacing
```

### Change Card Size
Edit `sass/abstracts/_variables.scss`:
```scss
$card-width: 21.875rem;   // Adjust width
$card-height: 15.625rem;  // Adjust height
```

### Change Breakpoints
Edit `sass/abstracts/_variables.scss`:
```scss
$breakpoint-tablet: 48rem;    // 768px
$breakpoint-desktop: 90rem;   // 1440px
```

## Browser Testing

Test the responsive design:
1. Open browser DevTools (F12)
2. Click "Toggle Device Toolbar" (Ctrl+Shift+M)
3. Select different device sizes
4. Or manually resize browser window

## Common Issues

### Sass not compiling?
- Ensure Sass is installed: `sass --version`
- Install if needed: `npm install -g sass`

### Styles not updating?
- Clear browser cache (Ctrl+Shift+R)
- Check if `style.css` was updated
- Recompile Sass

### Images not showing?
- Check file paths in `index.html`
- Ensure images are in `images/` folder
- Check browser console for errors

## Need More Help?

- 📖 See `README.md` for full documentation
- 🎨 See `STYLEGUIDE.md` for design system details
- 💻 See `IMPLEMENTATION.md` for technical details

## Live Server (Optional)

For better development experience, use a local server:

### VS Code Live Server
1. Install "Live Server" extension
2. Right-click `index.html`
3. Select "Open with Live Server"

### Python Simple Server
```bash
python -m http.server 8000
# Open http://localhost:8000
```

### Node.js http-server
```bash
npx http-server -p 8000
# Open http://localhost:8000
```

---

**That's it!** You're ready to use and customize the Four Card Feature Section.