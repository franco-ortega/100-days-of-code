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

### Day ??: ?day, October ??, 2021

**Project:**

**Tech:**

**Today's Progress:**

**Thoughts:**

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Pull Request](https://github.com/franco-ortega/ts-02-storybook/pull/8)
1. [Website](https://tell-your-tale.netlify.app/)
