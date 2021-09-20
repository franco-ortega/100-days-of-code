
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


---
### Day 38: Tueday, September 7, 2021

**Project:** Storybook

**Tech:** React, TypeScript, CSS

**Today's Progress:** (3 hrs) I begin working a dynamic route linked to a reusable component that will receive props from a data file in order to generate most of the pages for this app.

**Thoughts:** I vaguely remember creating a dynamic route for a school project over 6 months ago. It was part of an app that fetched fictional character data (LotR) from an API. The title of each character was displayed on the page as a link. Clicking on a character link took the user to a page that displayed details of that particular character. A reusuable component was used to generate all the character details pages. So, the work today was not totally knew to me. I had done this sort of work at least once in the past (and probably more like a few times), but my memory was really fuzzy on it, and I had never done this with TypeScript before, so that made it extra tricky, but I seemed to get things most of the way there today. Also, I did most of the work today with a test component using data inside that same file just to see if I could get it working more or less properly.

**Link(s) to work**
1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Pull Request](https://github.com/franco-ortega/ts-02-storybook/pull/2)
1. [Website](https://tell-your-tale.netlify.app/)


---
### Day 39: Wednesday, September 8, 2021

**Project:** Storybook

**Tech:** React, TypeScript, CSS

**Today's Progress:** (3 hrs) I completed work on getting the dynamic route linked up to the reusuable component, which in turn takes in information from a data file via props to dynamically generate most of the pages for this app. If I want to add more pages, I just need to add more information to the data file without needing to touch the dynamic route or reusuable component. Woohoo!

**Thoughts:** It felt good to get all this wired up and working properly. The toughest part was figuring out how to give TypeScript the proper types. Each dynamic page needed to pull a word from the URL in order to display the appropriate data, and TypeScript was getting super grumpy about properly typing params. Eventually, after much internet searching, I found out that I could use "keyof typeof dataName" where dataName was the variable that pointed to the imported data. Such as "import dataName from './data/dataFile.json'". Additionally, the main page (that had links to all the dymanic pages) also needed to import the data to generate the links by accessing the keys of objects inside the data file. I was able to get the keys easily with Object.keys(), but properly typing these values was super tricky too. The values were strings, but TypeScript would not accept the string type. Eventually, I realized, it would only accept the strings listed in the data. I was able to get it working by creating a type that included all the strings with or statments ( || ) between each string. However, that was not at all dynamic and would get very clunky as the data scaled up. The solution was to create a type with the same shape as the objects in the data file, and then, another type that was an array of the previous object type. It looks like this:

type ChapterInfo = {
  title: string,
  choices: string[]
}

type AllChapterInfo = ChapterInfo[]

AllChapterInfo was set as the type for the variable that held the array of object values created by Object.value(). That was a doozy, but now I know how to handle that kind of issue.

**Link(s) to work**
1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Pull Request](https://github.com/franco-ortega/ts-02-storybook/pull/3)
1. [Website](https://tell-your-tale.netlify.app/)

---
### Day 40: Thursday, September 9, 2021

I attended TechCrawl 2021. I did attend the virtual version last year, but this time it was my first in-person tech event. There were about 10 booths, and I spoke to employers or recruiters at most of them. Also, I saw a bunch of people from the code school that I attended (Alchemy Code Lab). This include fellow students from my cohort, but I also saw people from past cohorts and the newer cohorts - all of whom I hadn't seen in person before, so that was rad.

1. [TechCrawl](https://www.techcrawl.org/2021-techcrawl)
1. [Alchemy Code Lab](https://www.alchemycodelab.com/)


---
### Day 41: Friday, September 10, 2021

**Project:** Job Searching / Networking

**Tech:** n/a

**Today's Progress:** I attended the third day of LTX Quest - a virtual conference for Latinx professionals, and this included listening to speakers, connecting with other attendees on LinkedIn, and having virtual chats with employers.

**Thoughts:** It was really nice hearing speakers talk about a variety of topics, and the entertainment was super fun. I watched a drag king performance for the first time.

**Link(s)**
[LTX Quest](https://ltxconnect.org/quest/)


---

Need to write up the logs for Days 42 - 49.

---

### Day 50: Sunday, September 19, 2021

**Project:** Glowing Colors

**Tech:** React, CSS

**Today's Progress:** I made some adjustments to the text color, font size, and media queries.

**Thoughts:** The text color gradient that I added previously to the Welcome component did not work on mobile, but I still wanted to have some color with the text. I tried adding a background with a colorful gradient, but it felt like too much color. In the end, I kept the original dark backgound and chose a soft, light blue-purple shade that suited it. Also, since the Welcome component took up nearly the entire screen on mobile, I removed the background entirely from the mobile version. I still like how the dark background looks on larger screens. It gives the text an island to sit on. Whereas on mobile view, it felt too cluttered to have that island try to squeeze into a space barely bigger than it.

There was only one media queries before. This is a mobile first design, and the one media query was for screens that have a min-width of 500px. This was not sufficient to make the site look proper responsive of tablet and desktop screens, so I added another media query for screens with a min-width of 900px. Also, I increased the middle setting of the clamp for font size while decreasing the max value. Now the text is bigger and more readable on tablet size, but not too big on desktop.

And this was all CSS work, so it took multiple pull requests to make sure everything was looking as expected on mobile. You know how it goes.

**Link(s) to work**
1. [Repo](https://github.com/franco-ortega/glowing-colors)
1. [Pull Request #1 - change text color](https://github.com/franco-ortega/glowing-colors/pull/9)
1. [Pull Request #2 - add media query](https://github.com/franco-ortega/glowing-colors/pull/10)
1. [Pull Request #3 - adjust font size](https://github.com/franco-ortega/glowing-colors/pull/11)
1. [Website](https://glowing-colors.netlify.app)

---

### Day 51: Monday, September 20, 2021

**Project:** Glowing Colors

**Tech:** React, CSS

**Today's Progress:** I added a button that allows the user to "go back" to the "home page" by removing the orbs and rendering the Welcome component.

**Thoughts:** Previously, once the orbs began rendering, there was no way to stop the process from continuing without end or to return to the Welcome component that serves as a landing page to greet the user. So, I added a button in the upper righthand corner that does both of these things, and I added instructions to click in that area to return to the "home page". This **Go Back** button has an opacity of 0% to keep it invisible to the user under most conditions. However, when the user hovers over the button, or when the button receives focus, the opacity becomes 100% to make it visible. I recently took a course about web accessibility on Udemy, and I learned that it is helpful to have the same styling for focus and hover. This allows users who navigate with a mouse and users who navigate with a keyboard to have the same experience and same acesss to functionality.

**Link(s) to work**
1. [Repo](https://github.com/franco-ortega/glowing-colors)
1. [Pull Request](https://github.com/franco-ortega/glowing-colors/pull/13)
1. [Glowing Colors Website](https://glowing-colors.netlify.app)
1. [Introduction to Web Accessibility WCAG 2.1](https://www.udemy.com/course/introduction-to-web-accessibility-wcag21/)

