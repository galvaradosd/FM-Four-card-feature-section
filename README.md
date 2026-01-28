# Four Card Feature Section

A responsive four-card feature section built with semantic HTML5 and Sass, following BEM methodology.

## Overview

This project showcases a modern feature section with four cards highlighting different features. The layout adapts seamlessly across mobile, tablet, and desktop viewports.

### Features

- ✅ Semantic HTML5 markup
- ✅ BEM (Block Element Modifier) methodology
- ✅ Sass/SCSS with modular architecture
- ✅ Fully responsive design (Mobile: 375px, Tablet: 768px, Desktop: 1440px)
- ✅ Custom color-coded cards with top borders
- ✅ Smooth transitions and modern styling
- ✅ Accessible markup with proper heading hierarchy

## Design System

### Colors

#### Primary Colors
- **Red**: `#EA5454` - Team Builder card
- **Cyan**: `#44D3D2` - Supervisor card
- **Orange**: `#FCAE4A` - Karma card
- **Blue**: `#549EF2` - Calculator card

#### Neutral Colors
- **Grey 500**: `#4D4F62` - Headings and titles
- **Grey 400**: `#6A7178` - Body text
- **White**: `#FFFFFF` - Card background
- **Background**: `#FAFAFA` - Page background

### Typography

**Font Family**: Poppins (Google Fonts)

#### Font Weights
- Extra Light: 200
- Regular: 400
- Semibold: 600

#### Type Scale
- **Heading (Desktop)**: 36px / 2.25rem
- **Heading (Mobile)**: 24px / 1.5rem
- **Card Title**: 20px / 1.25rem
- **Body**: 15px / 0.9375rem
- **Small**: 13px / 0.8125rem

### Spacing

- **500**: 40px / 2.5rem
- **400**: 32px / 2rem
- **300**: 24px / 1.5rem
- **200**: 16px / 1rem
- **100**: 8px / 0.5rem

### Layout

#### Cards
- Width: 350px
- Height: 250px
- Padding: 32px
- Border Radius: 8px
- Top Border: 4px (colored)
- Shadow: `0 15px 30px -11px rgba(131, 166, 210, 0.5)`

## Project Structure

```
FM Four card feature section/
├── index.html
├── style.css (compiled from Sass)
├── README.md
├── STYLEGUIDE.md
├── package.json
├── images/
│   ├── icon-supervisor.svg
│   ├── icon-team-builder.svg
│   ├── icon-karma.svg
│   └── icon-calculator.svg
└── sass/
    ├── main.scss
    ├── abstracts/
    │   ├── _variables.scss
    │   └── _mixins.scss
    ├── base/
    │   ├── _reset.scss
    │   └── _typography.scss
    ├── layout/
    │   └── _page.scss
    └── components/
        ├── _feature-section.scss
        └── _card.scss
```

## BEM Methodology

### Blocks
- `.page` - Main page container
- `.feature-section` - Feature section component
- `.card` - Card component

### Elements
- `.feature-section__header` - Header container
- `.feature-section__title` - Main title
- `.feature-section__description` - Description text
- `.feature-section__cards` - Cards grid container
- `.card__content` - Card content wrapper
- `.card__title` - Card title
- `.card__description` - Card description
- `.card__icon` - Card icon image

### Modifiers
- `.feature-section__title-text--light` - Light weight title text
- `.feature-section__title-text--bold` - Bold weight title text
- `.card--cyan` - Cyan colored card
- `.card--red` - Red colored card
- `.card--orange` - Orange colored card
- `.card--blue` - Blue colored card

## Development

### Prerequisites
- Sass compiler installed

### Compile Sass

To compile the Sass files to CSS:

```bash
sass sass/main.scss style.css --no-source-map
```

For development with watch mode:

```bash
sass --watch sass/main.scss:style.css
```

Or using npm scripts:

```bash
npm run build:css
npm run watch:css
```

## Responsive Breakpoints

- **Mobile**: 375px and up
- **Tablet**: 768px and up
- **Desktop**: 1440px and up

### Layout Behavior

#### Mobile (< 768px)
- Single column layout
- Cards stack vertically
- Centered content

#### Tablet (768px - 1439px)
- Two column grid
- Cards arranged in 2x2 grid

#### Desktop (≥ 1440px)
- Three column grid
- Side cards (Supervisor & Calculator) aligned with center column
- Middle column contains Team Builder and Karma cards

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Accessibility

- Semantic HTML5 elements (`<main>`, `<section>`, `<article>`, `<header>`)
- Proper heading hierarchy
- Alt text for decorative images (empty alt)
- Sufficient color contrast ratios

## Credits

- Design: Frontend Mentor
- Icons: Provided by Frontend Mentor
- Font: Poppins by Google Fonts