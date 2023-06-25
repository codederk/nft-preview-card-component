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
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./screenshot/Screen%20Shot%202023-06-25%20at%2013.10.21.png)

![](./screenshot/Screen%20Shot%202023-06-25%20at%2013.11.18.png)

![](./screenshot/Screenshot%202023-06-25%20131309.png)

### Links

- Solution URL: [https://github.com/codederk/nft-preview-card-component](https://github.com/codederk/nft-preview-card-component)
- Live Site URL: [https://codederk.github.io/nft-preview-card-component/](https://codederk.github.io/nft-preview-card-component/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow
- Scss

### What I learned

I have learned ho to bring up overlay color and icon on mouse hovered image.

```html
<div class="container">
  <img
    class="card-img"
    src="./images/image-equilibrium.jpg"
    alt="nft equillibrium"
  />
  <div class="overlay">
    <a href="#"><div class="icon"></div></a>
  </div>
</div>
```

```scss
.container {
  position: relative;
  width: 100%;
  margin-bottom: -6px;

  &:hover {
    & .overlay {
      opacity: 1;
      cursor: pointer;
    }
  }

  .card-img {
    border-radius: 0.5rem;
    overflow: hidden;
    max-width: 100%;
  }

  .overlay {
    position: absolute;

    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    height: calc(100% - 6px);
    width: 100%;
    background-color: $color-secondary-alpha;
    opacity: 0;
    border-radius: 0.5rem;
    transition: opacity 0.3s ease;
  }

  .icon {
    background-image: url("data:image/svg+xml,%3Csvg width='48' height='48' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cpath d='M0 0h48v48H0z'/%3E%3Cpath d='M24 9C14 9 5.46 15.22 2 24c3.46 8.78 12 15 22 15 10.01 0 18.54-6.22 22-15-3.46-8.78-11.99-15-22-15Zm0 25c-5.52 0-10-4.48-10-10s4.48-10 10-10 10 4.48 10 10-4.48 10-10 10Zm0-16c-3.31 0-6 2.69-6 6s2.69 6 6 6 6-2.69 6-6-2.69-6-6-6Z' fill='%23FFF' fill-rule='nonzero'/%3E%3C/g%3E%3C/svg%3E");
    height: 48px;
    width: 48px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
}
```

### Useful resources

- [w3school.com](w3school.com/howto/howto_css_image_overlay_icon.asp) - How to create Image Overlay Icon.
- [github.io](https://yoksel.github.io/url-encoder/) - URL-encoder for SVG

## Author

- Frontend Mentor - [@codederk](https://www.frontendmentor.io/profile/yourusername)
