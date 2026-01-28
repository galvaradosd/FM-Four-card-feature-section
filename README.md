# Frontend Mentor - Four card feature section solution

This is a solution to the [Four card feature section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/four-card-feature-section-weK1eFYK). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![Desktop View](./screenshot-desktop.png)

### Links

- Solution URL: [GitHub Repository](https://galvaradosd.github.io/FM-Four-card-feature-section/)
- Live Site URL: [Live Demo](https://yourusername.github.io/four-card-feature-section)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties (via Sass variables)
- Flexbox
- CSS Grid
- Mobile-first workflow
- Sass/SCSS - CSS preprocessor
- BEM methodology - CSS naming convention

### What I learned

This project was an excellent opportunity to practice several key web development concepts:

#### 1. BEM Methodology
I implemented a strict BEM naming convention throughout the project, which made the CSS more maintainable and self-documenting:

```html
<article class="card card--cyan">
  <div class="card__content">
    <h2 class="card__title">Supervisor</h2>
    <p class="card__description">Monitors activity to identify project roadblocks</p>
  </div>
  <img src="images/icon-supervisor.svg" alt="" class="card__icon" />
</article>
```

#### 2. Sass Architecture
I organized my Sass files using a modular structure inspired by the 7-1 pattern:

```scss
// Abstracts
@import "abstracts/variables";
@import "abstracts/mixins";

// Base
@import "base/reset";
@import "base/typography";

// Layout
@import "layout/page";

// Components
@import "components/feature-section";
@import "components/card";
@import "components/footer";
```

#### 3. Custom Grid Layout
The desktop layout required a unique three-column grid where the center column contains two cards while the side columns contain one card each, vertically centered. I achieved this using CSS Grid:

```css
.feature-section__cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  align-items: center;
}

.feature-section__cards-center {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}
```

#### 4. Pseudo-element for Card Borders
Instead of using a traditional border-top, I used a pseudo-element to create the colored top border on each card, giving more control over styling:

```scss
@mixin card-border-top($color) {
  position: relative;

  &::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 0.25rem;
    background-color: $color;
    border-radius: 0.5rem 0.5rem 0 0;
  }
}
```

### Continued development

Areas I want to continue focusing on in future projects:

1. **Advanced Sass features** - Explore more complex mixins, functions, and the newer `@use` and `@forward` rules
2. **CSS Grid mastery** - Continue practicing complex grid layouts and responsive patterns
3. **Accessibility** - Implement more comprehensive ARIA labels and keyboard navigation patterns
4. **Animation** - Add subtle micro-interactions and entrance animations
5. **Performance optimization** - Implement lazy loading and optimize asset delivery

### Useful resources

- [Sass Documentation](https://sass-lang.com/documentation) - Essential for understanding Sass features and best practices
- [BEM Methodology](http://getbem.com/) - Great resource for learning and implementing BEM naming conventions
- [CSS Grid Guide](https://css-tricks.com/snippets/css/complete-guide-grid/) - Comprehensive guide that helped me understand CSS Grid layouts
- [MDN Web Docs](https://developer.mozilla.org/) - Invaluable reference for HTML, CSS, and accessibility best practices

## Author

- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/galvaradosd)
- GitHub - [@yourusername](https://github.com/galvaradosd)

---

## Project Structure

```
FM Four card feature section/
├── index.html
├── style.css (compiled from Sass)
├── README.md
├── IMPLEMENTATION.md
├── QUICKSTART.md
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
        ├── _card.scss
        └── _footer.scss
```

## Development

To work with this project:

1. Clone the repository
2. Ensure Sass is installed: `npm install -g sass`
3. Compile Sass: `sass sass/main.scss style.css --no-source-map`
4. Or use watch mode: `sass --watch sass/main.scss:style.css`
5. Open `index.html` in your browser

## Design System

### Colors
- **Primary**: Red (#EA5454), Cyan (#44D3D2), Orange (#FCAE4A), Blue (#549EF2)
- **Neutral**: Grey 500 (#4D4F62), Grey 400 (#6A7178), White (#FFFFFF), Background (#FAFAFA)

### Typography
- **Font Family**: Poppins
- **Weights**: 200 (Extra Light), 400 (Regular), 600 (Semibold)
- **Sizes**: 36px/24px (heading), 20px (card title), 15px (body), 13px (small)

### Spacing Scale
- 100: 8px | 200: 16px | 300: 24px | 400: 32px | 500: 40px
