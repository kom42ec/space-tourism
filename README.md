# Frontend Mentor - Space tourism challenge

This is a solution to the ....

The challenge is to build out this multi-page space tourism website and get it looking as close to the design as possible.

Users should be able to:

- View the optimal layout for each of the website's pages depending on their device's screen size
- See hover states for all interactive elements on the page
- View each page and be able to toggle between the tabs to see new information

## Links

- Solution URL:
- Live site URL:

## Screenshots

## Built with

- Semantic HTML5 Markup
- CSS custom properties
- Flexbox
- CSS Grid
- Vanilla JavaScript

## What I learned

### 1. Creating general reset

Every project starts with CSS reset. The most important ones are box-sizing, margin reset, media reset, form controls font reset, and percentage-based height. But we can also remove the animations for people who have turned them off, like this:

```
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
```

### 2. Using utility classes

Generic utility classes we often use are flex, grid, and container. We can use `padding-inline` and `margin-inline` properties with a container class as a modern CSS solution. The one generic utility class that I haven't used before is the "screen reader only" class which is useful when there is a button without text, for example. It is used for accessibility and it looks like this:

```
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap; /* added line */
  border: 0;
}
```

### 3. Adding custom properties

The main point here is that we define custom properties first and then use them to create number of utility classes which are added to elements later. Something like a mini-Tailwind approach.

- Color custom properties

Here I learned how to use a little trick to tweak the alpha value when needed. First we add hsl values to custom properties like this:

```
:root {
--clr-dark: 230 35% 7%;
--clr-light: 231 77% 90%;
--clr-white: 0 0% 100%;
}
```

...and then we create a class like this: `.example { background-color: hsl( var(--clr-light) / 0.2)}` where we can tweak alpha value easily.

We also created utility classes for background and text colors, like this:

```
.bg-dark {
  background-color: hsl(var(--clr-dark));
}
.text-white {
  color: hsl(var(--clr-white));
}
```

- Creating the design system

## Author

- Frontend Mentor
- Twitter

```

```

```

```
