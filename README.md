# Coffee Shop Website

This repository contains the code for a responsive website with a clean and modern UI. The project includes an interactive Hamburger Menu, a Search Form, and a Shopping Cart component that can be toggled open or closed. It is designed with mobile-first responsiveness, meaning the site adapts to different screen sizes seamlessly.

## Live Demo

You can view a live demo of the project by visiting the following link:

 🔴[Live Demo](https://coffeeclassicscafe.netlify.app/)

## Table of Contents

- [Installation](#installation)

- [Features](#features)

- [HTML Structure](#html-structure)

- [CSS Styling](#css-styling)

- [JavaScript Functionality](#javascript-functionality)

## Features

- **Responsive Design**: The layout adjusts according to different screen sizes (Desktop, Tablet, Mobile).

- **Hamburger Menu**: A collapsible navigation menu that appears on smaller screens.

- **Search Form**: A functional search bar that can be toggled open and closed.

- **Shopping Cart**: A shopping cart container that displays selected items and can be toggled open and closed.

- **Smooth Transitions**: Transitions for opening and closing the menu, search form, and cart.

## Installation
To run this project locally, follow these steps:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   ```

2. **Navigate to the project folder:**

   ```bash
   cd repository-name
   ```

3. **Open the index.html file in your browser to view the project.**

4. **Optionally, you can also set up a local server if needed for additional functionality (e.g., live server in VSCode).**

## HTML Structure

The HTML structure is organized to ensure easy navigation and accessibility. Below is a summary of the main sections:

### Header Section:

- Contains a Logo and a Navbar with navigation links.

- Includes a Search Button and a Cart Button.

- The Hamburger Menu is triggered by a button and appears only on smaller screen sizes.

### Main Content Sections:

- **Home Section**: Hero image with introductory text.

- **About Section**: Information about the website or company.

- **Menu Section**: A grid layout displaying items available for purchase.

- **Products Section**: A grid of product cards, each with a title, price, and images.

- **Review Section**: Customer reviews with star ratings.

- **Contact Section**: Contact form and a map.

- **Blogs Section**: Display blog posts with images and brief descriptions.

### Footer Section:

- Links to social media.

- Site navigation links.

- Copyright information.

## CSS Styling

The website is styled using CSS with the following notable features:

- **Typography**: The project uses the Roboto font from Google Fonts for a modern and clean look.

- **Color Scheme**:

  - **Primary Color**: A warm, golden color (#d3ad7f).

  - **Secondary Color**: A dark shade of gray (#13131a) used for the background and text.

  - **Background Color**: The background of the page is set to a very dark black (#010103).

- **Layout**:

  - Flexbox is used for centering elements and creating responsive layouts.

  - The grid layout is applied to sections like the Menu, Products, and Blogs for a modern, adaptive design.

- **Media Queries**: Used to adapt the design to different screen sizes (Desktop, Tablet, Mobile).

### Media Queries Breakdown

- For screens wider than 768px: Basic layout.

- For screens 768px or smaller: The hamburger menu is activated, and the navbar turns into a vertical sidebar.

- For screens 450px or smaller: Further optimizations for mobile devices.

- For screens 380px or smaller: Additional tweaks for ultra-small devices like phones in portrait mode.

## JavaScript Functionality

The JavaScript file adds interactivity to the page. Here are the key features implemented in JavaScript:

### Elements:

- **Navbar**: Handles the visibility of the main navigation menu.

- **Search Form**: Controls the toggle behavior for the search bar.

- **Cart Container**: Manages the visibility of the shopping cart.

### Event Listeners:

- **Hamburger Menu Toggle**: Clicking on the hamburger icon (`#menu-btn`) will show or hide the navbar on small screens.

- **Search Form Toggle**: Clicking on the search button (`#search-btn`) will show or hide the search form.

- **Cart Toggle**: Clicking on the cart button (`#cart-btn`) will show or hide the cart container.

- **Scroll Behavior**: When the user scrolls down, the navbar, search form, and cart container are automatically closed, improving the user experience.

```bash
let navbar = document.querySelector(".navbar");
let searchForm = document.querySelector(".search-form");
let cartItem = document.querySelector(".cart-items-container");

// Hamburger menu toggle
document.querySelector("#menu-btn").onclick = () => {
  navbar.classList.toggle("active");
  searchForm.classList.remove("active");
  cartItem.classList.remove("active");
};

// Search form toggle
document.querySelector("#search-btn").onclick = () => {
  searchForm.classList.toggle("active");
  navbar.classList.remove("active");
  cartItem.classList.remove("active");
};

// Cart items toggle
document.querySelector("#cart-btn").onclick = () => {
  cartItem.classList.toggle("active");
  navbar.classList.remove("active");
  searchForm.classList.remove("active");
};

// Close all on scroll
window.onscroll = () => {
  navbar.classList.remove("active");
  searchForm.classList.remove("active");
  cartItem.classList.remove("active");
};
```

## JavaScript Functionality

The JavaScript file adds interactivity to the page. Here are the key features implemented in JavaScript:

### Behavior:

- **Hamburger Menu**: Clicking the hamburger menu toggles the visibility of the navigation bar.

- **Search Button**: Clicking the search button opens or closes the search form, hiding the navbar and cart.

- **Cart Button**: Clicking the cart button opens or closes the shopping cart, hiding the navbar and search form.

- **Scroll Behavior**: If the user scrolls, all pop-ups (navbar, search form, cart) close automatically.

## Customization

### Colors

- **Primary Color**: The primary color is used for buttons, highlights, and interactive elements. You can change the color by modifying the `--primary-color` variable in the `:root` section of `styles.css`.

#### Example:

```css
:root {
    --primary-color: #d3ad7f; /* Change this value to customize the primary color */
}
```

### Background Color

- **Background Color**: Modify the background color of the body and other sections by changing the `--bg` and `--secondary-color` variables.

#### Example:

```css
:root {
    --bg: #f0f0f0; /* Change this value to customize the background color */
    --secondary-color: #ffffff; /* Change this value for secondary backgrounds */
}
```
### Fonts

- The project uses the Roboto font from Google Fonts. If you'd like to change the font, replace the link in the <head> section of index.html with a new Google Fonts link, and update the font-family in the CSS.

### Example:

```html
<link href="https://fonts.googleapis.com/css2?family=YourNewFont&display=swap" rel="stylesheet">
```

```css
body {
    font-family: 'YourNewFont', sans-serif; /* Update to your new font */
}
```

## Layout

- **Layout**: To change the layout, adjust the values in the `grid-template-columns` and `flex` properties found in the CSS for different sections like `.menu .box-container`, `.product .box-container`, and `.blogs .box-container`.

## Navbar and Menu

- **Navbar and Menu**: To add or remove links in the navigation menu, simply modify the `<a>` tags in the `<nav>` section of `index.html`.

## JavaScript

- **JavaScript**: You can easily modify the JavaScript to add more functionality, such as a search feature, product filters, or even dynamic content loading. The current script handles toggling of the navbar, search form, and cart container, but you can extend it as needed.

## Contribution

Contributions are welcome! If you'd like to improve this project, you can fork the repository, make changes, and create a pull request. Below are a few ways you can contribute:

- **Fix Bugs**: If you find any bugs or issues with the website, feel free to open an issue and submit a pull request with your fix.

- **Enhance Features**: Add new features, such as additional sections or interactivity enhancements.

- **Improve Documentation**: If you have suggestions for improving this documentation, please submit a pull request with your improvements.

- **Improve UI/UX**: Propose changes to improve the design or user experience of the website.

### To Contribute:

1. Fork the repository.

2. Create a new branch.

3. Make your changes.

4. Test your changes locally.

5. Create a pull request.

Please make sure to follow best practices and maintain the code style of the project.
   
