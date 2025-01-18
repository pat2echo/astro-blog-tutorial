# Editing Pages
1. Go to src/pages and make edits and see this reflect on your browser
https://docs.astro.build/en/tutorial/1-setup/3/

## Add new pages
https://docs.astro.build/en/tutorial/2-pages/1/

## Creating Posts
https://docs.astro.build/en/tutorial/2-pages/2/

## Define and use variables
https://docs.astro.build/en/tutorial/2-pages/3/

## CSS variables
https://docs.astro.build/en/tutorial/2-pages/4/

## Reuable components - Menus etc
Create a new src/components/ folder
To hold .astro files that will generate HTML but that will not become new pages on your website, you will need a new folder in your project: src/components/.

https://docs.astro.build/en/tutorial/3-components/1/

## Using Props
define props in a component
```
---
const { platform, username } = Astro.props;
---
<a href={`https://www.${platform}.com/${username}`}>{platform}</a>
```

set props when calling the component
```
---
const platform = "github";
const username = "withastro";
import Social from './Social.astro';
---

<footer>
  <p>Learn more about my projects on <a href={`https://www.${platform}.com/${username}`}>{platform}</a>!</p>
  <Social platform="twitter" username="astrodotbuild" />
  <Social platform="github" username="withastro" />
  <Social platform="youtube" username="astrodotbuild" />
</footer>
```
https://docs.astro.build/en/tutorial/3-components/2/

## Importing JS
```
<body>
  <script>
    import "../scripts/menu.js";
  </script>
</body>
```
https://docs.astro.build/en/tutorial/3-components/4/

## Using Astro inbuilt <slot /> component
Use an Astro <slot /> element to place page contents within a layout.  
sending HTML content to be rendered inside another component using a <slot /> placeholder
https://docs.astro.build/en/tutorial/4-layouts/1/

## Dynamically display a list of posts
```
const allPosts = Object.values(import.meta.glob('./posts/*.md', { eager: true }));
```
https://docs.astro.build/en/tutorial/5-astro-api/1/

## Create pages dynamically
