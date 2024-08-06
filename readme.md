# Landing Pages

## Overview

This project contains a collection of landing pages created by me to test various design theories and implement landing page designs from different Figma files. The primary focus is on using Tailwind CSS for styling and AOS (Animate On Scroll) for adding animations.

## Project Structure

```

project-folder/
│
├── landingpages/
│ ├── landing-0.html
│ ├── landing-1.html
│ ├── ...
│ └── landing-24.html
│
└── index.html

```

## Technologies Used

### Tailwind CSS

For styling, I chose to use Tailwind CSS instead of writing plain CSS. This decision was made to further my learning of Tailwind CSS, and I found the process enjoyable.

#### CDN Code for Tailwind CSS

To include Tailwind CSS in the project, add the following CDN links in the `<head>` section of your HTML files:

```html
<script src="https://cdn.tailwindcss.com"></script>
<script
  src="https://kit.fontawesome.com/143f4c7aad.js"
  crossorigin="anonymous"
></script>
```

#### Code for Dark Mode

To enable dark mode using Tailwind CSS, add the following script:

```html
<script>
  tailwind.config = {
    darkMode:
      "class" /* class/media, here we use class to enable manually dark mode */,
  };
</script>
```

### AOS (Animate On Scroll)

AOS library was used to animate most of the landing pages, enhancing the visual appeal and user experience.

#### CDN Code for AOS

To include AOS in the project, add the following CDN links in the `<head>` section of your HTML files:

```html
<!-- animate on scroll library -->
<link
  href="https://cdn.rawgit.com/michalsnik/aos/2.1.1/dist/aos.css"
  rel="stylesheet"
/>
<script src="https://cdn.rawgit.com/michalsnik/aos/2.1.1/dist/aos.js"></script>
```

## Index Page

The `index.html` file in the root directory lists all the landing pages. Users can click on any link to be directed to the respective landing page.

### Example of `index.html`

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Landing Pages</title>
    <style>
      body {
        font-family: Arial, sans-serif;
        padding: 20px;
      }
      ul {
        list-style-type: none;
        padding: 0;
      }
      li {
        margin: 10px 0;
      }
      a {
        text-decoration: none;
        color: #007bff;
      }
      a:hover {
        text-decoration: underline;
      }
    </style>
  </head>
  <body>
    <h1>Landing Pages</h1>
    <ul>
      <!-- Landing pages links will be inserted here by JavaScript -->
    </ul>
    <script>
      const landingPagesContainer = document.querySelector("ul");
      const totalLandingPages = 25; // Total number of landing pages

      for (let i = 0; i < totalLandingPages; i++) {
        const listItem = document.createElement("li");
        const link = document.createElement("a");
        link.href = `landingpages/landing-${i}.html`;
        link.textContent = `Landing Page ${i}`;
        listItem.appendChild(link);
        landingPagesContainer.appendChild(listItem);
      }
    </script>
  </body>
</html>
```

## How to Use

1. Clone the repository to your local machine.
2. Open the `index.html` file in your browser to view the list of landing pages.
3. Click on any landing page link to view the respective landing page.

## Notes

- The project heavily relies on CDN links to make it simple for anyone who reads or re-uses the code.
- Ensure you have an active internet connection to load the CDN resources properly.

## Conclusion

This project serves as a practical exercise in implementing and testing landing page designs using Tailwind CSS and AOS. Feel free to explore and modify the code to suit your needs. Happy coding!
