
### Day 32: Wednesday, September 1, 2021

**Project:** Todo List App

**Tech:** React, CSS

**Today's Progress:** (5 hrs) I fine tuned the styling, which included moving the overflow property from the entire TodoList component to only the actual list of todo items. This allowed the TodoList title and delete button in the header to remain on the screen even if the list of todo items was too long to fit on the screen and needed to be scrolled. Also, I added a CSS grid to the TodoList to help the new overflow element be more consistent across multiple screen sizes.

Additionally, I had an unusal eslint error with an equals sign in a class component: state = {}. It wasn't breaking anything, but I wanted to see if I could fix it and wound up going down a StackOverflow rabbit hole that directed me to add a babel parser, but I don't know that it fixed anything other than making the equals sign error message no longer show up - along with no other error messages showing up either, which did lead to other things breaking.

**Thoughts:** It was really tricky trying to get the overflow element to consistently reach to the bottom of its parent element. A new media query needed to be added for each screen size to re-adjust its height. I thought it might work better with a grid, but I was hesistant to try that because I wasn't sure how difficult that would be since I'm only semi-familiar with using grid, so I put off trying it with grid. However, once I got it as close as possible with media queries, I tried using grid, and it came together remarkably quickly and easily. I wish I hadn't hestitated earlier because if I tried grid sooner, I would have saved a lot of time. Lesson learned: don't avoid the hard thing, especially if it seems like it might work better. Because in this instance it worked better and was much faster to implement than struggling to find a solution with the method that I felt more comfortable with.

As for the eslint issue, I did notice that eslint errors were displaying in my functional components when they occured, but some of those same errors (indention, missing semi-colon) didn't show up in the class components, which is where the surprising equals sign error did show up. When I added the babel parser and its associated code to the eslint file, the equals sign error no longer came up, but the eslint errors that were coming up in the functional components now no longer came up either. However, they still broke the deployement on Netlify and needed to be fixed. And after all that, I tried removing all the babel code in the eslint file, which made error messages in the functional components be visible again as well as the equals sign error in the class component, but as long as the errors in the functional components were fixed, the equals sign error in the class component didn't seem to matter. The app still deployed fine with it.

**Link(s) to work**
1. [Repo](https://github.com/franco-ortega/demo-react-01-todos)
1. [Pull Request #1 - style updates](https://github.com/franco-ortega/demo-react-01-todos/commit/0b267390154a5246a7a928e516ff86ca0afa75e8)
1. [Pull Request #2 - eslint "fix"](https://github.com/franco-ortega/demo-react-01-todos/commit/b01feee8d266adac24cd86d02a75c244f9e42a1f)
1. [Website](https://a-list-of-todos.netlify.app)


### Day 33: Thursday, September 2, 2021

**Today's Progress:** (~6 hrs) I took the [Just JavaScript](https://justjavascript.com/) course.

**Thoughts:** I found this course very helpful for gaining a better understanding of:
1. primitive values (which are immutable, which makes sense, but I never thought of them that way before)
1. the relationship between variables and values
1. the fact that values are passed into functions (as opposed to the actual arguments)
1. object mutation

It also provided great visuals to help create a wonderful mental model of what happens when variables are re-assigned.

This course does not teach JavaScript, but it helps with understanding how some of the fundamentals work. I started learning JavaScript one year ago, and I would highly recommend this course to anyone who is a few months into their JavaScript journey or even a few years.


---

### Day 34: Friday, September 3, 2021

**Project:** Glowing Colors

**Tech:** React, CSS

**Today's Progress:** I added a landing page with instructions.

**Thoughts:** The landing page is a component that fades away when the user clicks to proceed, and then it is unrendered. Afterwards is when the orbs are rendered. It was somewhat tricky getting the timing right for the fade away to complete before the orbs begin rendering, but now it is working great.

Also, I tried adding a color gradient on the text, which looked really nice. However, it didn't work on mobile and left the text transparent, so I removed the gradient.

**Link(s) to work**
1. [Repo](https://github.com/franco-ortega/glowing-colors)
1. [Pull Request #1 - add Welcome component](https://github.com/franco-ortega/glowing-colors/commit/ab0ed96ff2594496c32ca51c3e6e659994aff163)
1. [Pull Request #2 - remove text gradient](https://github.com/franco-ortega/glowing-colors/commit/60aad948d21eebd23c61e310da5249636e24a84f)
1. [Website](https://glowing-colors.netlify.app)


---
### Day 35: Saturday, September 4, 2021

**Today's Progress:** A day of rest.


---
### Day 36: Sunday, September 5, 2021

**Today's Progress:** Another day of rest.


---
### Day 37: Monday, September 6, 2021

**Project:** Storybook

**Tech:** React, TypeScript, CSS

**Today's Progress:** (~6 hrs) I started building an app where the user will build a story by visiting different lands in any order they wish, and then selecting a sentence from each land. When they have visited all the lands, their completed story will be displayed.

**Thoughts:** I'm getting back into TypeScript, and this will be my first fully-fledged app that combines it with React. I spent almost an hour watching video tutorials followed by more than an hour sketching out a plan on Miro. Then, I spent several more hours using test-driven development (TDD) to start building the app. I set up the App component with a router and created the initial Prologue component with a form, and the initial Chapters component with test data. It's coming together nicely so far.

**Link(s) to work**
1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Pull Request #1 - Prologue component](https://github.com/franco-ortega/ts-02-storybook/commit/45d24ecb55953ea8fddc88204095b56c5cac672c)
1. [Pull Request #2 - Chapters component](https://github.com/franco-ortega/ts-02-storybook/commit/4dd5ebd4a2eb6fd0895bd2ab33d941a1e93cbfe4)
