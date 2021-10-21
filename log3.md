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

1. [Repo](https://github.com/franco-ortega/demo-sass-02-react)
1. [Pull Request #1 - refactor SaturationBox](https://github.com/franco-ortega/demo-sass-02-react/pull/2)
1. [Pull Request #2 - replace if else statment with bracket notation](https://github.com/franco-ortega/demo-sass-02-react/pull/3)
1. [Website](https://sass-react-demo.netlify.app/)

---

### Day 64: Sunday, October 3, 2021

**Project:** Sass Demo with React

**Tech:** Sass, React

**Today's Progress:** (1 hr) Added LightBox component to display colors with different levels of light in their HSL color codes.

**Thoughts:**

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/demo-sass-02-react)
1. [Pull Request](https://github.com/franco-ortega/demo-sass-02-react/pull/4)
1. [Website](https://sass-react-demo.netlify.app/)

---

### Day 65: Monday, October 4, 2021

**Project:** Sass Demo with React

**Tech:** Sass, React

**Today's Progress:** (1 hr) Added media queries for tablet and desktop views.

**Thoughts:**

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/demo-sass-02-react)
1. [Pull Request](https://github.com/franco-ortega/demo-sass-02-react/pull/5)
1. [Website](https://sass-react-demo.netlify.app/)

---

### Day 66: Tuesday, October 5, 2021

**Project:** Sass Demo with React

**Tech:** Sass, React

**Today's Progress:** (1 hr) Updated media queries to be handled by a mixin.

**Thoughts:** Came across some strange behavior where the background color would not fill the entire height of a component. The area below the final child element was transparent, so it showed up as a while gap between this component and the one below it. I did some searching and found the solution to be to add the **display: flex** property to the component, and then the background color went to the bottom edge. Alternatively, I was able to acheive the same effect by adding a border to the component, but that was a sub-par solution because I didn't want the component to have a border. I tried making the border transparent, but that still created a gap along any elements that sat along the edge of the component.

Also along strange styling lines, when I added **display: flex** to a component with images, the image size grew big enough to fill the width of the screen, which looked terrible. The solution I found here was to add **align-items: center** to the component, and then the images went back to their regular size.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/demo-sass-02-react)
1. [Pull Request #1](https://github.com/franco-ortega/demo-sass-02-react/pull/6)
1. [Pull Request #2](https://github.com/franco-ortega/demo-sass-02-react/pull/7)
1. [Website](https://sass-react-demo.netlify.app/)

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

### Day 71: Sunday, October 10, 2021

**Project:** Portfolio

**Tech:** React, Sass

**Today's Progress:** (3 hr) Lots of pull requests today:

1. Updated the image that displays on previews when the site is linked on search engines and social media.
1. Added meta tags to create the preview when posting this site on Twitter.
1. Adjusted position of Resume, Cartography, and island components on mobile.
1. Added media query to differentiate between tall vs short mobile devices (height above & below 700px).
1. Updated the module for Legend to scss and replaced class names with nested selectors.
1. Updated the module for BorderCorner to scss and replaced class names with nested selectors.
1. Updated the module for CartographyDetails to scss and replaced class names with nested selectors.

**Thoughts:** The project has a lot of CSS files. After changing the main components to to SCSS files last week, I didn't realize how many more files there were to change and update.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/portfolio)
1. [Pull Request #1 - portfolio preview](https://github.com/franco-ortega/portfolio/pull/231)
1. [Pull Request #2 - meta tags ](https://github.com/franco-ortega/portfolio/pull/232)
1. [Pull Request #3 - adjust position](https://github.com/franco-ortega/portfolio/pull/233)
1. [Pull Request #4 - media query ](https://github.com/franco-ortega/portfolio/pull/234)
1. [Pull Request #5 - Legend ](https://github.com/franco-ortega/portfolio/pull/235)
1. [Pull Request #5 - BorderCorner ](https://github.com/franco-ortega/portfolio/pull/237)
1. [Pull Request #5 - CartographyDetails ](https://github.com/franco-ortega/portfolio/pull/242)
1. [Website](https://francoortega.com/)

---

### Day 72: Monday, October 11, 2021

**Project:** Portfolio

**Tech:** React, Sass

**Today's Progress:** (3 hr) Updated the Ocean module to scss, moved the grid to the outermost element and removed the element that had the grid, restructed the order of the elements to be more reflective of their importance, and added a media query to differntiate between wide vs narrow landscape orientation on mobile. Also, I made adjustments to the Compass component that were required after the updates to Ocean.

**Thoughts:** The compass is a CSS wonder, which makes it a doozy to adjust. Also, moving the grid to the outermost element required lots of changes to everything inside that component, but being able to nest the selectors helped this go smoother.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/portfolio)
1. [Pull Request](https://github.com/franco-ortega/portfolio/pull/243)
1. [Website](https://francoortega.com/)

---

### Day 73: Tuesday, October 12, 2021

**Project:** Portfolio

**Tech:** React, Sass

**Today's Progress:** (1 hr) - Changed all the remaining css files to scss files. Adjusted the position of Profile on mobile.

**Thoughts:** I didn't realize how many components that my portfolio site had. It's over 30! So this task took some time.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/portfolio)
1. [Pull Request](https://github.com/franco-ortega/portfolio/pull/246)
1. [Website](https://francoortega.com/)

---

### Day 74: Wednesday, October 13, 2021

**Project:** Portfolio

**Tech:** React, Sass

**Today's Progress:** (3 hr) - Added and adjusted Legend media queries. Fine tuned placement of GitHub and LinkedIn islands on mobile.

**Thoughts:** The recent refactor of the main grid on the Ocean component resulted in the Legend component overlapping the header text on smaller screens. It took quite a bit of trial and error, but I was able to get it looking good on all screens again.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/portfolio)
1. [Pull Request](https://github.com/franco-ortega/portfolio/pull/243)
1. [Website](https://francoortega.com/)

---

### Day 75: Thursday, October 14, 2021

**Project:** Portfolio

**Tech:** React, Sass

**Today's Progress:** (1 hr) - Adjust the position of the Cartography on mobile landscape and Profile on mobile portrait. Reduced the z-index of continents and islands from 2 to 1.

**Thoughts:** The seemed to be behaving oddly on mobile for the Profile component. When I adjusted its left column, it moved as expected, but when I adjusted the right column, there was no change on the screen. It turned out that this component was set to position:absolute, and when I changed it to position:relative, it worked as expected. I don't yet understand why that made a difference. And the only reason I added position to components was because it was necessary to give them a z-index after I made changes to the grid earlier this week. They were no longer clickable until I gave them a z-index to put them above the grid layer. The grid layer now has a z-index of -1, so I gave everything a z-index of 2 justo to be safe incase anything had a z-index of 1, but today I reduced those 2's to 1's, and all is still well.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/portfolio)
1. [Pull Request](https://github.com/franco-ortega/portfolio/pull/251)
1. [Website](https://francoortega.com/)

---

### Day 76: Friday, October 15, 2021

**Project:** Portfolio

**Tech:** React, Sass

**Today's Progress:** (2.5 hr) - I added hover styles to the continents, which made them more consistent with the islands. Now they all clickable components transform on hover. Also, I added focus styles to the continents and islands for keyboard navigation; this makes it much more obvious with component has focus. The focus style is the same transform as the hover, and it adds a box shadow as well. Then, I updated the reduced-motion media queries to remove the focus and hover transforms, and to add the box shadow to the hover style.

**Thoughts:** I gave the focus style the additional box shadow because I figured that if a user who hovers over clickable component then looks away from the screen, when they look at the screen again, they can still see where the mouse is positioned to remind them which items is hovered. However, if a user using keyboard navigation looks away from the screen, there is no other indicator to show them which item is focused when they look back at the screen, and it might not be obvious which focused item is currently transformed, so the box shadow helps make the focus more obvious.

Then, when I removed all the transforms for the reduced-motion option, the hover no longer had any style, so that's why I added the box shadow to it at that point.

One quirk about applying transform to focus and hover styles is that if the user focuses and hovers on a component at the same time, it gets transformed twice. I don't know yet how to prevent that double transform from happening.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/portfolio)
1. [Pull Request](https://github.com/franco-ortega/portfolio/pull/253)
1. [Website](https://francoortega.com/)

---

### Day 77: Saturday, October 16, 2021

**Project:** Portfolio

**Tech:** React, Sass

**Today's Progress:** (1 hr) Replaced the mobile media queries in several components with the media-query mixin for mobile.

**Thoughts:** I had started this work a couple weeks ago but then got sidetracked - in a beneficial way - by creating proper styling for landscape orientation on mobile and updating the css modules of many components into scss modules with nested selectors (which helped reduce the amount of class names), so it was good to get back to this.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/portfolio)
1. [Pull Request](https://github.com/franco-ortega/portfolio/pull/255)
1. [Website](https://francoortega.com/)

---

### Day 78: Sunday, October 17, 2021

**Project:** Portfolio

**Tech:** React, Sass

**Today's Progress:** (3 hr) I added and fine tuned media queries in order to have the site display well when the browser is narrow on desktop screens (i.e. less than 900px wide while also having a height of less than 1000px, which is shorter than a tablet screen, but also a height of more than 500px, which is taller than landscape orientation on mobile). Adjusted the placement of Legend on mobile screens. Revamped the compass to be more evenly responsive.

**Thoughts:** It felt really good to fix how the site looked on narrow desktop screens. Between the changes I made to the main grid and the changes to make landscape orientation look good on mobile, it seemed to have screwed up how it looked on narrow desktop screens, and it was difficult at first to figure out how to fix it. But I used the Firefox dev tools (after hearing really good things about them this weekend on video tutorials) to see how the main grid and inner grids were working at different screen sizes, and that helped a lot with figuring out a solution. Then, I overhauled the compass in a way that made its parts stay fairly proportional across all screen sizes. The original code for the compass resulted in the points changing sizes notably across different screen sizes, and even with media queries to mitigate these affects, I still wasn't able to get the compass points to remain equally proportional at different screen sizes. However, being able to see its grid allowed me to see that the compass parts were distorting the grid, so I worked on changing the parts and grid to keep the grid a consistent shape, and that went a long way to keeping the compass proportional across different screen sizes. My recent deeper understanding of the position property helped too. Quite honestly, when I first created the compass, I didn't have a great understanding of how the CSS was working to create the points. The points were triangles created by manipulating the different border sides (top, left, etc), which I learned how to do through tutorials, and I was able to combine these triangle with circles to form the compass, but it was a hodgepodge effort more based on trial & error than understanding of the code. So it makes sense that the result was somewhat unwieldy and hard to control. This revamp, however, was based on my much deeper understanding of the CSS properties that were used and new ones that helped make it better (such as the position property).

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/portfolio)
1. [Pull Request #1 - narrow desktop view](https://github.com/franco-ortega/portfolio/pull/256)
1. [Pull Request #2 - compass updates](https://github.com/franco-ortega/portfolio/pull/261)
1. [Website](https://francoortega.com/)

---

### Day 79: Monday, October 18, 2021

**Project:** Storybook

**Tech:** React, TypeScript

**Today's Progress:** (0.5 hrs) Built a feature to display the user's most recent selection in the Chapters component. Updated the test data to make it more clear which chapter that each selection comes from. Added the current props (two of which were missing) to the ChapterDetails test.

**Thoughts:** It felt good to get back to this practice after a few weeks of diving deeper into Sass and applying a lot of it to my portfolio site. Part of the reason I spent that time on Sass was to determine if I wanted to style this project with it. It was either going to be Sass or Tailwind. Now that I have a much better feel for and understanding of Sass, I want to put that into practice, so I will be adding that soon. I do still want to get more experience with Tailwind, but it seems like combining Tailwind with TypeScript might be a tricky way to get a better grasp on Tailwind, so I'll use a straight up React app for that.

Anyway, one idea that came to me today by looking at this app with fresh eyes was that it could be helpful for the user to see their most recent selection. I am intentionally not showing them their whole story until the end because I want to be a bit of a surprise, but they might find it helpful to keep in mind their latest seletion while picking the next one. Especially now that they have the ability to look at a chapter but back out of it without making a selection. If they look at several chapters before making their next selection, it might be that enough time has passed that they don't quite remember their previous selection. But now they can see if every time that they return to the Chapters component. Maybe I'll add it to the ChapterDetails component, too, so they can see their latest selection while picking the next one.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Pull Request](https://github.com/franco-ortega/ts-02-storybook/pull/15)
1. [Website](https://tell-your-tale.netlify.app/)

---

### Day 80: Tuesday, October 19, 2021

**Project:** Storybook

**Tech:** React, TypeScript

**Today's Progress:** (2 hrs) Added props to the tests that were missing them. Tried to mock the useParams hook in the ChapterDetails test but was not able to do so. Removed userSelections state from ChapterDetails. Renamed the userSelections type to Selections in order to differentiate it from the userSelections state. Added an enum to hold the strings for endpoints.

**Thoughts:** Figuring out how to test the useParams hook is very challenging. Neither the documentation for the React Testing Library nor several articles or StackOverflow posts on the subject were able to get me there. The same "undefined" error for the params continues to come up. I spent way too much time trying to figure that out. At least I was able to update the ChapterDetails component in a way that allows the setUserSelections function to also redirect the user to the proper component. I'm not sure if the Endpoints enum would make sense for best practices, but it does help to avoid mistyping magic strings.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Commit #1 - update tests](https://github.com/franco-ortega/ts-02-storybook/commit/9eacfabf025429d087eaeb6cd0addf2c3e6b181c)
1. [Commit #2 - remove userSelections state](https://github.com/franco-ortega/ts-02-storybook/commit/66d0f4ad898813a9a022f254d8326afe9c4e765d)
1. [Commit #3 - rename userSelections type](https://github.com/franco-ortega/ts-02-storybook/commit/d0a702dcbdb01fd5d6e20e9fe9882bca6a9471e5)
1. [Commit #4 - add Endpoints enum](https://github.com/franco-ortega/ts-02-storybook/commit/7ae506fddccc291fa98a815c268b9710c3b6c193)
1. [Website](https://tell-your-tale.netlify.app/)

---

### Day 81: Wednesday, October 20, 2021

**Project:** Sundial

**Tech:** React, Node

**Today's Progress:** (1 hr) I implemented the feedback received for this take-home project from last month. It had to do with keeping data stored "in memory" without a database for a Node server. I actually had to make more changes to the code besides just what the interviewer shared, but I was able to get it working with this alternate approach, and it didn't take long either. Then, I spent some time refactoring my old code.

**Thoughts:** My first approach at storing data without a database was to use Redis. That worked great. However, the interviewer said that Redis was a database, so it didn't meet the "databaseless" requirement. My next approach was to create a file with the data that was updated accordingly as the data was updated. That worked well too. Unfortuntely, this approach was also rejected. That was the end of my interview process with that company. The feedback was only a high level look at their solution for this issue. I wish they would have provided feedback on the entire fullstack app because I was able to get it all working, and with multiple approaches too. I just didn't figure out the specific approach that they wanted. At least afterwards they gave me a rough idea of how to do it, and it felt good to be able to implement it so easily. And I did learn a bit more about how a Node server can hold onto changing data even if it isn't being stored anywhere persistent.

**Link(s) to work**
I am not allowed to share the code for this project, so no links this time.

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
