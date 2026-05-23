# Petvet Web - Project Documentation

## Project Overview

**Petvet** is a static single-page website for a pet veterinary and grooming service. It is built using vanilla HTML5 and CSS3, leveraging **Bootstrap 5.3.8** for responsive layout components and **Font Awesome 7.0.1** for icons.

This project was built as the **Final Exam** for HTML, CSS, Bootstrap, and styling libraries for the **Saylani Mass IT Training's Techno Kids Course (Batch 7)**.

The design and layout of this project are inspired by and cloned from the [Colorlib Petvet Theme](https://preview.colorlib.com/theme/petvet/).

### Deployment

- [GitHub Repository](https://github.com/sheikh-mohammad/petvet-web)
- [Live URL](https://final-petvet.netlify.app/)

### Key Features/Sections

| Section | Description |
|---------|-------------|
| Hero | Landing area with background image, headline, and CTA buttons |
| Services | Cards displaying veterinary, grooming, and pet-sitting services |
| About | Company introduction with qualifications checklist |
| Appointment | Form for booking veterinary appointments |
| Groomers | Team member profiles with social links |
| Testimonials | Customer reviews in a carousel slider |
| Pricing Plans | Service pricing cards |
| Blog | Latest blog posts section |
| Footer | Contact info, quick links, and newsletter signup |

### Technology Stack

- **HTML5** - Semantic markup
- **CSS3** - Custom styles with CSS variables
- **Bootstrap 5.3.8** (CDN) - Grid system, navbar, carousel, cards, forms
- **Font Awesome 7.0.1** (CDN) - Icon library
- **Custom Font** - Roboto (loaded from `assets/fonts/Roboto-Regular.ttf`)

### Design System

```css
:root {
    --font: "Roboto";
    --primary: #FD4C82;    /* Pink accent color */
    --secondary: #91c235;  /* Green accent color */
}
```

## Project Structure

```
petvet-web/
├── index.html              # Main HTML file (all sections in single page)
├── style.css               # Custom stylesheet
├── README.md                 # Project documentation
└── assets/
    ├── fonts/
    │   └── Roboto-Regular.ttf
    └── images/
        ├── about/          # About section images
        ├── blogs/          # Blog post thumbnails (blog-1.png, blog-2.png, blog-3.png)
        ├── groomers/       # Team member photos (g-1.png through g-4.png)
        ├── hero/           # Hero background image
        ├── logo/           # Brand logo
        ├── plans/          # Pricing plan images
        └── testinomial/    # Testimonial images (person_*.png, background.png)
```

## Building and Running

This is a **static website** with no build process required.

### To Run Locally

1. **Simple file open**: Double-click `index.html` in a file explorer
2. **Using a local server** (recommended for proper asset loading):
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js (npx)
   npx serve .
   
   # Using PHP
   php -S localhost:8000
   ```
3. Open `http://localhost:8000` in a browser

### Dependencies

All dependencies are loaded via CDN:
- Bootstrap 5.3.8 CSS
- Font Awesome 7.0.1 CSS

No `npm install` or package management required.

## Development Conventions

### CSS Organization

- **CSS Variables** used for theme colors (`--primary`, `--secondary`) and font
- **Section-based styling**: Each major section has its own class prefix:
  - `.hero-section`, `.service-card`, `.about-section`, `.as-img`
  - `.appoinment-section`, `.groomers-section`, `.gc` (groomer card)
  - `.testinomials-section`, `.plans-section`, `.blog-section`
- **Responsive design**: Mobile-first with `@media` queries for smaller screens

### Naming Conventions

- **Kebab-case** for CSS classes (e.g., `.service-card`, `.groomers-section`)
- **Descriptive class names** reflecting section/function
- **Bootstrap utility classes** heavily used for spacing, flexbox, typography

### Image Assets

- All images are PNG format
- Expected missing images that should be added for complete functionality:
  - `assets/images/hero/hero.png`
  - `assets/images/logo/logo.png`
  - `assets/images/testinomial/background.png`
  - `assets/images/testinomial/person_1.png`, `person_2.png`, `person_3.png`
  - `assets/images/plans/` (plan images)
  - `assets/images/blogs/` (blog thumbnails)

## Known Notes

- The appointment form is **front-end only** (no backend integration)
- Some placeholder text uses "Lorem Ipsum"-style dummy text ("Far far away, behind the word mountains...")
- Groomer cards have duplicate placeholder names ("Lloyd Wilson")
- The site uses `sticky-top` and `fixed-top` Bootstrap classes for navigation
- Overflow-x is hidden on `html, body` to prevent horizontal scrolling

## Future Enhancements

Potential areas for development:
1. Add JavaScript for form validation/submission
2. Implement smooth scrolling for navigation links
3. Add missing image assets
4. Create separate pages for detailed views (blog posts, services)
5. Add meta tags for SEO optimization
6. Implement lazy loading for images
