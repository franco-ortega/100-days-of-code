### Day 62: Friday, October 1, 2021

**Project:** Sass Demo with React

**Tech:** Sass, React

**Today's Progress:** (90 min) I created variables for each part of the HSL code in order to easier adjust the color level, saturation, and light.

<pre>
$red-hsl: 0;
$orange-hsl: 39;
$yellow-hsl: 60;
$green-hsl: 120;
$blue-hsl: 240;
$purple-hsl: 300;

$sat-full: 100%;
$sat-high: 75%;
$sat-mid: 50%;
$sat-low: 25%;
$sat-none: 0%;

$light-full: 100%;
$light-high: 75%;
$light-mid: 50%;
$light-low: 25%;
$light-none: 0%;
</pre>

Example:

<pre>
background: hsl($purple-hsl, $sat-full, $light-mid);
</pre>

I used these to create a series of color sets with each set having varying saturations levels of its specific color (see image below). Then, I created component to hold all the elements of a single color. Finally, I made a Sass mixin that handled all the styings of a single color (all 5 different saturation levels to the boxes of one color).

**Thoughts:** Today I really saw the power of mixins to reduce repetitive CSS. I knew that properties could be placed in mixins, but I didn't realize that selectors could be placed inside mixins too. That really opened up things. Each color set has 5 boxes, and each box is styled differently, and that entire series of CSS code had to be repeated for every other. However, then I was able to put all that code into a single mixin that took in a parameter for the color. That saved me almost 100 lines of code!

There was also repetitive HTML for each color set, but I created a reusable component with props to clean that up, and it felt good to see how quickly and easily I was able to implement that.

![Set of colors with different saturation levels](./assets/saturations.png 'Color Boxes')

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/demo-sass-02-react)
1. [Pull Request](https://github.com/franco-ortega/demo-sass-02-react/pull/1)
1. [Website](https://sass-react-demo.netlify.app/)

---

### Day 63: Saturday, October 2, 2021

**Project:** Sass Demo with React

**Tech:** Sass, React

**Today's Progress:** (1 hr) I moved the mixin and appropriate styling properties from the Colors component into the SaturationBox component and refactored the latter component handling the styling more dynamically.

**Thoughts:** My changes yesterday worked how I wanted, but I realized that it made more sense to place the styling of the boxes in the actual SaturationBox component instead of its parent Colors component. Moving the mixin was easy, but getting to work dynamically was tricky. I was passing the color into the SaturationBox component as a prop, and I thought that I would be able to use that prop as a className that would connect to the corresponding class in the scss file. However, I had to concatenate the color prop to styles (styles.Color), but this kept resulting in an object Object issue ([object Object].Color). After experimenting with multiple ways to combine the styles and Color in a dynamic way, I restored to using an if else statment to create the style name:

<pre>
if(color === 'Red') hsl = styles.Red;
  else if(color === 'Yellow') hsl = styles.Yellow;
  else if(color === 'Orange') hsl = styles.Orange;
  else if(color === 'Green') hsl = styles.Green;
  else if(color === 'Blue') hsl = styles.Blue;
  else if(color === 'Purple') hsl = styles.Purple;
</pre>

I don't understand why this approach worked when my initial approach didn't work:

<pre>
const hsl = styles.Color

or

const hsl = `${styles}.${Color}`
</pre>

Oh! Eureka!!! I just figured out how to make it dynamic:

<pre>
const hsl = styles[color];
</pre>

I needed to use bracket notation because the key of the styles object was not known and could be different every time. Thank goodness that I understand objects much better than I did before the summer.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Pull Request #1 - refactor SaturationBox](https://github.com/franco-ortega/demo-sass-02-react/pull/2)
1. [Pull Request #2 - replace if else statment with bracket notation](https://github.com/franco-ortega/demo-sass-02-react/pull/3)
1. [Website](https://tell-your-tale.netlify.app/)

---

### Day 64: Sunday, October 3, 2021

**Project:** Sass Demo with React

**Tech:** Sass, React

**Today's Progress:** (1 hr) Added LightBox component to display colors with different levels of light in their HSL color codes.

**Thoughts:**

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Pull Request](https://github.com/franco-ortega/demo-sass-02-react/pull/4)
1. [Website](https://tell-your-tale.netlify.app/)

---

### Day 65: Monday, October 4, 2021

**Project:** Sass Demo with React

**Tech:** Sass, React

**Today's Progress:** (1 hr) Added media queries for tablet and desktop views.

**Thoughts:**

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Pull Request](https://github.com/franco-ortega/demo-sass-02-react/pull/5)
1. [Website](https://tell-your-tale.netlify.app/)

---

### Day 66: Tuesday, October 5, 2021

**Project:** Sass Demo with React

**Tech:** Sass, React

**Today's Progress:** (1 hr) Updated media queries to be handled by a mixin.

**Thoughts:** Came across some strange behavior where the background color would not fill the entire height of a component. The area below the final child element was transparent, so it showed up as a while gap between this component and the one below it. I did some searching and found the solution to be to add the **display: flex** property to the component, and then the background color went to the bottom edge. Alternatively, I was able to acheive the same effect by adding a border to the component, but that was a sub-par solution because I didn't want the component to have a border. I tried making the border transparent, but that still created a gap along any elements that sat along the edge of the component.

Also along strange styling lines, when I added **display: flex** to a component with images, the image size grew big enough to fill the width of the screen, which looked terrible. The solution I found here was to add **align-items: center** to the component, and then the images went back to their regular size.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Pull Request #1](https://github.com/franco-ortega/demo-sass-02-react/pull/6)
1. [Pull Request #2](https://github.com/franco-ortega/demo-sass-02-react/pull/7)
1. [Website](https://tell-your-tale.netlify.app/)

---

### Day 67: Wednesday, October 6, 2021

**Project:** Portfolio

**Tech:** React, Sass

**Today's Progress:** (1.5 hr) I added the **prefers-reduced-motion** media query to my portfolio site and set it to turn off the animations and transitions for users who have the **Reduce motion** option selected in the **Accessibility** section of their operating system settings.

Also, I added Sass to this project and created a few extends, which replaced almost 300 lines of repetitive CSS across 4 files. Amazing!

**Thoughts:** I tuned into a couple videos about web accessibility, and the first one (linked below) had a lot of high level helpful info and links to resources. One resource was an article that introduced me to the **prefers-reduced-motion** media query. It's a great, quick read that I recommend for everyone who builds websites, and I linked it below.

Also, it was really great to put the power of Sass to use on my portfolio site. I was able to remove a fair amount of repetitive code (including CSS) in the main "details" pages/popups a couple months ago by creating a reusuable component that received the children prop. However, the same strategy didn't seem practical for the structure parent components of the details pages. Luckily, Sass was able to do the trick, and I am going to implement its features in other areas of my portfolio too.

**Link(s) to work**

1. [Getting started with web accessibility with Ashlee Boyer - video](https://www.youtube.com/watch?v=qr0ujkLLgmE&t=3s&ab_channel=KevinPowell)
1. [Reduced Motion article](https://www.tatianamac.com/posts/prefers-reduced-motion)
1. [Repo](https://github.com/franco-ortega/portfolio)
1. [Pull Request #1](https://github.com/franco-ortega/portfolio/pull/223)
1. [Pull Request #2](https://github.com/franco-ortega/portfolio/pull/224)
1. [Pull Request #3](https://github.com/franco-ortega/portfolio/pull/225)
1. [Website](https://francoortega.com/)

---

### Day 68: Thursday, October 7, 2021

**Project:** Portfolio

**Tech:** React, Sass

**Today's Progress:** (1.5 hr) I added media queries to the continents and islands for landscape orientation on mobile view.

**Thoughts:** I usually create a mobile-first design, but I made a desktop-first approach for my portfolio site because originally, I thought the layout for the mobile and desktop views would be essentially the same. However, long story short, that was not a feasible approach. The mobile view wound up needing to be very different from the desktop view, and I was able to create a very nice looking mobile view. However, it looked very distorted if the phone was turned sideways to landscape view. Now it looks so nice!! :)

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/portfolio)
1. [Pull Request](https://github.com/franco-ortega/portfolio/pull/226)
1. [Website](https://francoortega.com/)

---

### Day 69: Friday, October 8, 2021

**Project:** Portfolio

**Tech:** React, Sass

**Today's Progress:** (1 hr) I added an extend to handle the flex alignment of the island components and applied it to each of them. Also, I fine tuned the position of the Compass and Scale elements. And I added Sass to the Legend as one of my front end skills.

**Thoughts:** It felt good to reduce more repetitive code and make adjustments to a couple of the map elements in order to make them more pleasing to the eye. Also, it feels great to understand Sass well enough at this point to add it to my list of skills.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/portfolio)
1. [Pull Request](https://github.com/franco-ortega/portfolio/pull/228)
1. [Website](https://francoortega.com/)

---

### Day 70: Saturday, October 9, 2021

**Project:** Portfolio

**Tech:** React, Sass

**Today's Progress:** (1 hr) Created a mixin with the Sass map function to handle media queries. Added a new media query to ProjectDetails and to CartographyDetails and its reusuable child components for landscape orientation on mobile.

**Thoughts:** My plan was to apply the media query mixin to several components, but after making adjustments for landscape orientation on the main components earlier this week, I realized that the popups needed to be adjusted for landscape orientation too.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/portfolio)
1. [Pull Request](https://github.com/franco-ortega/portfolio/pull/229)
1. [Website](https://francoortega.com/)

---

### Day ??: ?day, October ??, 2021

**Project:**

**Tech:**

**Today's Progress:**

**Thoughts:**

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Pull Request](https://github.com/franco-ortega/ts-02-storybook/pull/8)
1. [Website](https://tell-your-tale.netlify.app/)
