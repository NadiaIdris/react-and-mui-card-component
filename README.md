<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Result](#result)
- [Workflow lessons for the next project](#workflow-lessons-for-the-next-project)
- [Goal](#goal)
- [Diagram](#diagram)
- [Wireframe](#wireframe)
- [Modify Theme in MUI](#modify-theme-in-mui)
- [How to style MUI components](#how-to-style-mui-components)
- [Other useful links on MUI documentation](#other-useful-links-on-mui-documentation)
  - [TouchRipple](#touchripple)
  - [Style Library Interoperability](#style-library-interoperability)
- [index.js](#indexjs)
- [App.js](#appjs)
- [Leave HTML `<select>` option blank](#leave-html-select-option-blank)
- [Is JSON a string?](#is-json-a-string)
- [DOM API](#dom-api)
- [Git](#git)
  - [Amend to previous commit](#amend-to-previous-commit)
  - [Commit and push on the terminal](#commit-and-push-on-the-terminal)
- [Add hover effect on JSX](#add-hover-effect-on-jsx)
- [CSS Specificity](#css-specificity)
- [Owners of the images](#owners-of-the-images)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Result

![](./public/result.gif)

# Workflow lessons for the next project

1. Make React components
2. Convert React components to MUI components.
   - Note to self: Do not add any styling for layouts or anything else before
     adding MUI Components. Otherwise, it's confusing to figure out what style
     changes should be done at the theme level vs in the component level.
3. Start styling. Figure out what changes need to be made in the theme level,
   what changes need to be made in the reusable component level.

# Goal

- Learn how to create React and [MUI](https://material-ui.com/) components, pass
  data around with ease.

# Diagram

1. Choose a location.
2. View a weather data for the chosen location.

- Option to type a location in the omnibox and correct weather data displays.

# Wireframe

- ![](public/images/wireframes2.jpg)

# Modify Theme in MUI

- [MUI documentation on Theming](https://material-ui.com/customization/theming/)
- [Default Theme all the options](https://material-ui.com/customization/default-theme/?expand-path=$.typography)
  - A caption is text that appears below an image. One of the smallest font
    sizes, may be used sparingly to annotate other visual elements.
  - Overline is one of the smallest font sizes, might be used to introduce a
    headline.
    - [Learn about Material Design type system](https://material.io/design/typography/the-type-system.html#type-scale)
- [How to override a style globally with CSS](https://v4-3-3.material-ui.com/customization/globals/#css):
  When the configuration variables aren't powerful enough, you can take
  advantage of the overrides key of the theme to potentially change every single
  style injected by Material-UI into the DOM. That's a really powerful feature.

# How to style MUI components

1. Add all the MUI components (e.g. `<CardActionArea>`, `<CardMedia>`) to the
   React components.
2. Do **theme** level overrides (typography, spacing, globals, palette,
   breakpoints, z-index)
3. Add local styling to each component where needed.

# Other useful links on MUI documentation

## TouchRipple

- [TouchRipple API](https://v4-3-3.material-ui.com/api/touch-ripple/)

## Style Library Interoperability

- [Style Library Interoperability](https://material-ui.com/guides/interoperability/#style-library-interoperability)

# index.js

- `index.js` file inserts the React app, `App.js` file, to html. React's Shadow
  DOM selects the root element from the DOM API and inserts the React app in it.

```jsx
ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById("root")
);
```

# App.js

- `App.js` is the first component. All components start with a capital letter .
  This is how the nested components come together with HTML.
  ![](public/images/app-nesting.jpg)

# Leave HTML `<select>` option blank

- [StackOverflow article: default select option as blank](https://stackoverflow.com/questions/8605516/default-select-option-as-blank)

# Is JSON a string?

- JSON is a **text-based data format** following JavaScript object syntax. JSON
  exists as a string — **useful when you want to transmit data across a
  network**.
- It needs to be converted to a native JavaScript object when you want to access
  the data.
- [MDN article on JSON](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/JSON)
- You can include the same basic data types inside JSON as you can in a standard
  JavaScript object — strings, numbers, arrays, booleans, and other object
  literals.

# DOM API

- Browser and HTML and JS
- Whomever made the browser is providing the DOM API. Chrome browser makers make
  DOM for Chrome, Safari browser makers make the DOM API in Safari browser.
- DOM API is for me, the web developer, to interact with the browser from my JS
  files, which I link to my HTML. Browser will take my index.html file.
- I write HTML and I embed my JS link to my HTML. I then can get information
  about browser history, can access and manipulate the DOM elements and form
  data etc.
  [Read more here](https://developer.mozilla.org/en-US/docs/Web/API/HTML_DOM_API)

# Git

## Amend to previous commit

```
git add -A ; git commit --amend --no-edit ; git push -f

```

## Commit and push on the terminal

```
git add -A ; git commit -m  "Change Select component font" ; git push
```

# Add hover effect on JSX

- `onMouseOver={this.openDropdown}`

# CSS Specificity

- The more specific the styling, the higher priority it gets in CSS.
- Only use `!important` on page-specific CSS that overrides foreign CSS (from
  external libraries, like Bootstrap or normalize.css).
- [More on CSS Specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity#How_is_specificity_calculated)

# Owners of the images

- [Mountain View image](https://unsplash.com/photos/WL5kcYYvFOU) by
  [Cameron Venti](https://unsplash.com/@ventiviews)
- [Sunnyvale image](https://unsplash.com/photos/-dUjtzo9h7Q) by
  [Roxann C](https://unsplash.com/@partyroxy)
- [Palo Alto image](https://unsplash.com/photos/QGbcc4Ckg6U) by
  [Emily Karakis](https://unsplash.com/@iemyoung)
