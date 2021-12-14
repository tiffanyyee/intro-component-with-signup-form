# Frontend Mentor - Intro component with sign up form solution

This is a solution to the [Intro component with sign up form challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/intro-component-with-signup-form-5cf91bd49edda32581d28fd1). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page
- Receive an error message when the `form` is submitted if:
  - Any `input` field does not validate.

### Screenshot

![solution screenshot](img/solution-screenshot.jpg)

### Links

- Solution URL: [https://github.com/tiffanyyee/intro-component-with-signup-form]
- Live Site URL: [https://tiffanyyee.github.io/intro-component-with-signup-form]

## My process

### Built with

- Semantic HTML5 markup
- CSS3 custom properties
- Bootstrap framework
- Mobile-first workflow / Responsive design

### What I learned

Some of my major learnings while working through this project included creating the matching curved edge shadow effect on the bottom of the signup form and buttons with CSS and creating the signup form and implementing the form validation using Bootstrap.

Some snippets of my code learnings:

```html
      <form class="row g-3 signup-form needs-validation" novalidate>
        <div class="form-floating mb-3">
          <input type="text" class="form-control" id="fName" required placeholder="First Name">
          <label for="fName">First Name</label>
          <div class="invalid-feedback">
            Please provide a valid first name.
          </div>
        </div>
      </form>
```
```css
.signup-form {
  border-radius: 8px;
  box-shadow: inset 0px -8px 0px 0px #da6867;
}
```
```js
// JavaScript for disabling form submissions if there are invalid fields
(function () {
    'use strict'
  
    // Fetch all the forms to apply custom Bootstrap validation styles to
    var forms = document.querySelectorAll('.needs-validation')
  
    // Loop over them and prevent submission
    Array.prototype.slice.call(forms)
      .forEach(function (form) {
        form.addEventListener('submit', function (event) {
          if (!form.checkValidity()) {
            event.preventDefault()
            event.stopPropagation()
          }
  
          form.classList.add('was-validated')
        }, false)
      })
  })()
```

### Useful resources

- [Bootstrap Docs](https://getbootstrap.com/docs/5.1/getting-started/introduction/)

## Author

- Tiffany Yee - [Portfolio](https://tiffanyyee.github.io), [GitHub](https://github.com/tiffanyyee)
- Frontend Mentor - [https://www.frontendmentor.io]
