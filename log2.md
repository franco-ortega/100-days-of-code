
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
