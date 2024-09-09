# Exercise: Build a Recipe in React

## Learning Goals

By completing this exercise, you will be able to:

- Create and structure a React Application
- Break down a UI into React Components
- Render static content using React Components
- Apply basic styling to React Components

## Introduction

Welcome to the world of React!

You’ve taken your first steps into a large world of web development using React. In this exercise, you’ll be creating a recipe page for your favourite dish. This isn’t just any recipe page - it’s your first React-powered web application!

Imagine you’re a developer for a popular cooking website. Your task is to create a visually appealing and well-structured recipe page that will make users’ mouths water and their coding senses tingle. You’ll be using your newly acquired skills to break down a page into components, creating a modular and maintainable structure.

Are you ready to cook up some delicous React components? Let’s dive in and start building!

## Getting Started

Follow the instructions below:

1. Fork this Repository
2. Clone the Repository to your computer
3. Create a new React application using Vite templates:

```bash
npm create vite . -- --template codeverge-react-starter
```

4. Run `npm install`
5. Open the project in VS Code
6. Start the development server:

```bash
npm run dev
```

7. Follow instructions

## Instructions

Complete the following exercises to practice working with React components:

### Part 1: Planning your Components

Before you start coding, plan out the structure of your recipe page.

Consider breaking your page into the following components:

1. Header (Title of the recipe)
2. RecipeImage (image of the finished dish)
3. Ingredients (list of ingedients)
4. Instructions (steps to prepare the dish)
5. NutritionInfo (nutritional information)
6. Footer (copyright information)

### Part 2: Creating Components

Create a new file for each component in the `src` folder.

### Part 3: Assembling Your Recipe Page

In your `App.js` file, import and use all the components you’ve created.

### Part 4: Adding Content

Fill in each component with appropriate content for your chosen recipe. Remember to use proper HTML tags within your JSX.

### Part 5: Styling Your Components

Add some basic styling to your components. You can do this by creating a CSS file for each component or using inline styles.

For example:

```jsx
// src/Header.js
import React from "react";
import "./Header.css";

function Header() {
  return (
    <header className="recipe-header">
      <h1>Delicious Chocolate Chip Cookies</h1>
    </header>
  );
}

export default Header;
```

## Submission

When you've completed the exercise:

1. Commit your changes:

```bash
git add .
git commit -m "Completed Recipe in React exercise"
git push origin main
```

2. Create a Pull Request

3. Submit the URL of your Pull Request below

<submission>

Please submit the URL of your Pull Request below:

## Bonus Challenges

If you finish early or want to push yourself further:

### Part 6: Responsiveness

Create a responsive layout using CSS Media Queries.

### Part 7: Print-friendly Stylesheet

This one is new, but a challenging and rewarding task.

Create a print-friendly stylesheet for your recipe page. This will allow users to easily print out the recipe with a clean, easy-to-read layout. Consider removing unnecessary elements, adjusting font sizes, and optimizing the layout for paper.

To implement this, you'll need to create a separate CSS file with print-specific styles and link it to your HTML using the media attribute in the link tag.

For example:

```html
<!-- In your HTML file -->
<link rel="stylesheet" href="styles.css" />
<link rel="stylesheet" href="print-styles.css" media="print" />
```

This will apply your regular styles for screen viewing, and the print-specific styles when the page is being printed. In your print stylesheet, you can then define styles that are optimized for printing, such as removing background colors, adjusting font sizes, and hiding non-essential elements.

## You Got Questions? We Got Answers!

<details>
<summary>How can I add an image to my React component?</summary>

To add an image in React:

1. Place your image in the `public` folder
2. Reference it in your component using the following syntax:

```jsx
<img src="/image-name.jpg" alt="Descripton of the Image" />
```

Alternatively, you can import the image in your component file:

1. Place your image in the `src` folder
2. Import it at the top of your component file:

```jsx
import recipeImage from "./recipe-image.jpg";
```

3. Use it in your JSX:

```jsx
<img src={recipeImage} alt="Description of the Image" />
```

</details>
<details>
<summary>How do I style my React Components?</summary>
There are several ways to style React components:

1. External CSS File

   1. Create a CSS file (e.g., `ComponentName.css`)
   2. Import it in your component file:

   ```jsx
   import "./ComponentName.css";
   ```

   1. Use class names in your JSX:

   ```jsx
   <div className="my-class">
   ```

2. Inline styles:

```jsx
<div style={{ color: 'blue', fontSize: '14px' }}>
```

</details>

<details>
<summary>Why can’t I use `class` instead of `className` in React?</summary>
In React, we use className instead of class for CSS classes because class is a reserved keyword in JavaScript. React uses JSX, which is closer to JavaScript than to HTML, so it uses className to avoid conflicts with the JavaScript class keyword.

```jsx
// Correct
<div className="recipe-title">

// Incorrect
<div class="recipe-title">
```

</details>

<details>
<summary>How do I create a list in React?</summary>
To create a list in React, you can use the `map` function to transform an array of data into an array of JSX elements:

```jsx
function IngredientList() {
  const ingredients = ["Flour", "Sugar", "Eggs", "Butter"];

  return (
    <ul>
      {ingredients.map((ingredient, index) => (
        <li key={index}>{ingredient}</li>
      ))}
    </ul>
  );
}
```

Remember to add a unique `key` prop to each list item to help React identify which items have changed.

</details>

<details>
<summary>How can I add comments in JSX?</summary>
To add comments in JSX, you need to use JavaScript comment syntax inside curly braces:

```jsx
function RecipeComponent() {
  return (
    <div>
      {/* This is a JSX comment */}
      <h1>Recipe Title</h1>
      {/* 
          Multi-line
          JSX comment 
        */}
    </div>
  );
}
```

</details>
