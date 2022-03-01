# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![Screenshot](https://github.com/PiperRc/NFT-PREVIEW-CARD/blob/main/screenshot/screenshot.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- Flexbox
- Mobile-first workflow

### What I learned

My process to achieve the hover effect of the eye.

I placed the two images of the eye and the cube in the save div, with the eye image going second.

```html
<div class="header-img-container">
  <img
    src="images/image-equilibrium.jpg"
    alt="equilbrium-image"
    class="main-img"
  />
  <img src="images/icon-view.svg" alt="eye" class="eye-img" />
</div>
```

Set the div to have a position of relative and the eye image to have a position of absolute and set the opacity to zero. Also, set the background of the div to have the hovered effect background color.Used flex to center the eye image and opacity:0 to make the eye invisible.



```css
.header-img-container {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 10px;
    background-color: var(--cyan);
}

.main-img {
    width: 100%;
    border-radius: 10px;
}

.eye-img {
    position: absolute;
    opacity: 0;
}
}
```

Used hover to set the opacity of the eye to 1 and the opacity of the cube to .5 allowing the eye background color to be displayed.

I learnt that the hover of one element can affect other elements as long as they are the child elements of the parent elemenet.

```css
.header-img-container:hover .main-img {
    opacity: .5;
}

.header-img-container:hover .eye-img {
    opacity: 1;
}

```


### Continued development

Do more research on semantic HTML and when to use <section>,<article>,<main>,etc.

### Useful resources

- [Stackoverflow](https://stackoverflow.com/questions/4502633/how-to-affect-other-elements-when-one-element-is-hovered#:~:text=If%20you%20have%20two%20elements,within%20the%20same%20larger%20element.) - Helped realize the child elements can be effected by the hover of parent elements


## Author


- Frontend Mentor - [@PiperRc](https://www.frontendmentor.io/profile/PiperRc)


## Acknowledgments

-Frontend Mentor for such an amazing resource

