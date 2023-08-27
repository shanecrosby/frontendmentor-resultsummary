# Frontend Mentor - Results summary component solution

This is a solution to the [Results summary component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/results-summary-component-CE_K6s0maV). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page
- **Bonus**: Use the local JSON data to dynamically populate the content

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- CSS gradient and transitions

### What I learned

CSS gradients can't be transitioned on and off, so one must cheat and have a second pseudo element containing the gradient, transitioning the opacity of that instead.

For example:

```css
.btn {
    position: relative;
    background-color: var(--blue);
    z-index: 1;
}

.btn::before {
    position: absolute;
    content: '';
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-image: linear-gradient(0deg, var(--gradient-top) 0%, var(--gradient-bottom) 100%);
    z-index: -1;
    transition: opacity 0.4s ease;
    opacity: 0;
}

.btn:hover::before {
    opacity: 1;   
}
```

### Continued development

Next step would be to populate the summary values from the data.json file instead of using the static HTML version.

### Useful resources

- Thanks to Keith J. Grant for the css gradient transition [tip](https://keithjgrant.com/posts/2017/07/transitioning-gradients/).
- [Understanding CSS flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Understanding CSS grid](https://css-tricks.com/snippets/css/complete-guide-grid/)

## Author

- Website - [Shane Crosby](https://www.shanecrosby.com)
- Frontend Mentor - [@shanecrosby](https://www.frontendmentor.io/profile/shanecrosby)
- Twitter - [@crosbyshane](https://www.twitter.com/crosbyshane)

## Acknowledgments
[Kevin Powell](https://www.youtube.com/watch?v=QqDH5sYzDS8)'s video on stepping up front-end web development skills was what got me started on this journey.
