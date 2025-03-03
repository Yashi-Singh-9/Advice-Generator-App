# Frontend Mentor - Advice Generator App Solution

This is a solution to the [Advice Generator App challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/advice-generator-app-QdUG-13db). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of Contents

- [Overview](#overview)
  - [The Challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My Process](#my-process)
  - [Built With](#built-with)
  - [What I Learned](#what-i-learned)
  - [Continued Development](#continued-development)
  - [Useful Resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The Challenge

Users should be able to:

- View the optimal layout for the app depending on their device's screen size
- See hover states for all interactive elements on the page
- Generate a new piece of advice by clicking the dice icon

### Screenshot

**Desktop Device**

![Advice Generator Screenshot](design/desktop-design.png)

**Mobile Design**

<img src="design/mobile-design.png" height="750">

### Links

- Solution URL: [Solution](https://www.frontendmentor.io/solutions/advice-generator-app-SU1t6L0Bqn)
- Live Site URL: [Live Demo](https://yashi-singh-9.github.io/Advice-Generator-App/)

## My Process

### Built With

- Semantic HTML5 markup
- Less (CSS preprocessor)
- JavaScript (fetch API for async data fetching)
- Bootstrap 5
- Mobile-first workflow

### What I Learned

During this project, I reinforced my understanding of asynchronous JavaScript using the `fetch()` API to retrieve data from an external source. Implementing dynamic content updates with JavaScript and styling elements responsively using Bootstrap and Less was a valuable experience.

Example of fetching and displaying advice:

```js
async function fetchAdvice() {
    try {
        const response = await fetch('https://api.adviceslip.com/advice');
        const data = await response.json();
        document.getElementById('advice-id').textContent = data.slip.id;
        document.getElementById('advice-text').textContent = `"${data.slip.advice}"`;
    } catch (error) {
        document.getElementById('advice-text').textContent = "Failed to load advice. Try again!";
    }
}

window.onload = fetchAdvice;
```

### Continued Development

Moving forward, I would like to:

- Improve UI animations for a smoother user experience
- Implement caching to reduce API calls
- Explore different ways to handle errors and user feedback

### Useful Resources

- [Bootstrap 5 Documentation](https://getbootstrap.com/docs/5.3/) - Helped with responsive design and UI components.
- [Advice Slip API](https://api.adviceslip.com/) - The external API used to fetch advice.

## Author

- Frontend Mentor - [Yashi-Singh-9](https://www.frontendmentor.io/profile/Yashi-Singh-9)
- LinkedIn - [Yashi Singh](https://www.linkedin.com/in/yashi-singh-b4143a246)

## Acknowledgments

A big thank you to the Frontend Mentor community for providing great challenges that help improve coding skills. Looking forward to building more projects!