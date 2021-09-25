
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

### Day 42: Saturday, September 11, 2021

**Project:** Take-Home Project (Fullstack app)

**Tech:** React, Node, Redis, webhooks

**Today's Progress:** I spent time today researching webhooks and Redis to help me to build a take-home project (fullstack app) from a company I interviewed with earlier this week.

**Thoughts:** Webhooks seem to be a way to help facilitate receiving multiple incoming requests in response to an inital outgoing request. For example, my server had to make a POST request to an external API with a piece of data and a URL. The URL was an endpoint on my server. The external API would send requests to this URL with updates on the data. The response to my inital request was an id number that would represent to piece of data that I just sent out. Then, at a later time, the external API would make several POST requests to the provided URL; those requests would have the id number and an update on the data. POST requests would continue to be sent for each piece of data until work on that particular piece of data was complete.

I guess what makes this different than other standard requests is that the external API doesn't know where to send the data. Because I think usually when you create code to make requests, you include the URL to send the request. But in this instance, the URL is unknown, and it is provided from another source (my server in this instance). Does this mean that my endpoint is the webhook? Or is the external API using a webhook to do this kind of dymanic work?

Also, I wasn't allowed to use a database but had to store the updated data "in memory". I wasn't quite sure what this meant or how to accomplish it, but a friend suggested that I look into Redis, and after doing some research, it seemed like a good solution. I watched a very helpful video tutorial on the YouTube channel of Web Dev Simplified to get me started with Redis (link below).

**Link(s)**
Because this is a take-home project for an interview, I am not allowed to post the code online, but here are links to resources that I used to build it:
1. [Redis](https://redis.io/)
1. [Web Dev Simplified](https://www.youtube.com/watch?v=jgpVdJB2sKQ)


---

### Day 43: Sunday, September 12, 2021

**Project:** Take-Home Project (Fullstack app)

**Tech:** React, Node, Express, Redis, webhooks

**Today's Progress:** I began this project on the server side. I used Node, which was required, and paired it with Express to build the API. I provided a GET route for my client (website) to access the initial version of the data held by my server; the reponse was a formatted version of the raw data.

Then, I built my client using React. It needed to display the data received from the first GET route. It would later need to update the display with data from the second endpoint.

The second endpoint was a GET route that prompted my server to begin processing the data; the processing was done by making a POST request to a 3rd-party API for each piece of data. Each response from the 3rd-party API responded was an id number for that particular piece of data, and my server responded to my client with an updated version of the formatted data that now included the id numbers.

The third endpoint was a POST route for the 3rd-party API to send me the status of each piece: process began, process continues, process completed. Each status was sent separately and at a different time. Each time a new status was received, I had to update the status in the formatted data on my server. However, I was not able to use a database, so this was where Redis would help. It could store the data locally.

**Thoughts:** I was able to get the first endpoint and the client working properly together to display the initial data. I had a tougher time with the second and third endpoints because it wasn't as straightforward as it may sound, but I'll discuss that tomorrow.

**Link(s)**
Because this is a take-home project for an interview, I am not allowed to post the code online, but here are links to resources that I used to build it:
1. [Redis](https://redis.io/)
1. [Web Dev Simplified](https://www.youtube.com/watch?v=jgpVdJB2sKQ)


---

### Day 44: Monday, September 13, 2021

**Project:** Take-Home Project (Fullstack app)

**Tech:** React, Node, Express, Redis, webhooks

**Today's Progress:** I created the logic that allowed the server to process data in a very specific way outlined in the requirement. There were 9 pieces of data that had to be sent to an external API for processing, and the processing of each piece of data resulted in  multiple incoming requests to my server. However, I could not send all 9 pieces of data together or immediately consecutively. I could only send 3 pieces of data to start, and when 1 piece was completed, then I could send out the next one.

**Thoughts:** I tried building the logic to handle all this complexity right from the start. However, the combination of multiple loops and conditional statments wound up being too much to track all at once off the bat. I scrapped this effort and restarted with a simpler approach. First, I desgined the server to process only the first piece of data. Then, when that was working, I added loops so it would process every piece of data right away. After that was completed, I finally added the conditional statments to check if a piece of data had been completed, and if so, to send out the next piece of data.

Everything appeared to be working properly except for one piece of data that never completed processing. I would later find out that there was a bug for this piece of data in the external API. It must have been intentionally placed there as a test. I hadn't considered that a take-home project would provide me with broken code, but I can understand why that was done, and now I know to look for such things in the future.

**Link(s)**
Because this is a take-home project for an interview, I am not allowed to post the code online.


---

### Day 45: Tuesday, September 14, 2021

**Project:** Cover letters and Promises

**Tech:** GoogleDocs and VSCode

**Today's Progress:** I spent the morning working on cover letter templates for applying to fullstack positions, frontend positions, fullstack positions that use React, and frontend React positions. Then in the evening, I watched a video tutorial on Promises.

**Thoughts:** The cover letter work took several hours and used up a day of job searching, but it will help me be more efficient going forward when applying to jobs. I will be able to use the template as a framework and then weave in details that pertain to the particular job and company. I already had a one cover letter template with different options for different positions, and sometimes even different options for the same kind of position. All this grew cumbersome over time and required me to sort through the many options each time I needed a new cover letter. Now all the options have been trimmed down and sorted, so I don't have to piece together all the parts anymore. I just need to add the details for each particular job and company.

As for Promises, I had used Promise.all and Promise.resolve before, but that was over 6 months ago. Also, I had never created a Promise using the "new" keyword before. I came across a video tutorial by Web Dev Simplified that helped refresh my memory and teach me new aspects of Promises too.

**Link(s)**
1. [Web Dev Simplied - Promises](https://www.youtube.com/watch?v=DHvZLI7Db8E)


---

### Day 46: Wednesday, September 15, 2021

**Project:** Accessibility

**Tech:** HTML

**Today's Progress:** I finished the web accessibility course that I stared a few weeks ago. The final portion covered user interfaces like buttons, input, and forms. I coded along with it to practice the techniques.

**Thoughts:** I'd say this was a pretty good beginner course on web accessibility. I was already familiar with some of this material, but I learned new things too - like that it is helpful to provide the same styling to focus and hover effects, so that the same experience is provided to users who use a mouse/touchpad and users who use keyboard navigation. Also, even though I coded along to this portion of the course, I didn't do that with the prior portions, which included the importtance of semantic HTML and skip links. All portions of the course had coding exercises to do afterwards, which involved making changes to sample websites in order to make them more accessible, and I did all of these exercises, but I'd still like to go back and practice those early portions on my own outside of the sample websites.

**Link(s)**
1. [Introduction to Web Accessibility WCAG 2.1](https://www.udemy.com/course/introduction-to-web-accessibility-wcag21/)


---

Need to write up the logs for Days 47 - 49.

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

---

### Day 52: Tuesday, September 21, 2021

**Project:** Storybook

**Tech:** React, TypeScript

**Today's Progress:** I started building a custom hook to help deactivate chapters that have already been read/written by the user.

**Thoughts:** When the Chapters component first loads, it displays each chapter as a link. When the user clicks on a chapter, goes to the page (ChapterDetails dynamic/reusuable component - direct child of Chapters component) that displays the info for that chapter, and then makes their choice, they are re-directed to the Chapters component. At that point, the chapter which was completed (and all other completed chapters) should be disabled. Today's work was the start of that effort.

I created a custom hook that returns a piece of state called "completed" (boolean) and a function that changes the value of "completed". The idea is that the boolean begins as false, and when the user completes a chapter, the boolean is changed to true, and this disables access to that chapter. This seemed like an easy thing to implement in my head, but once I started working on it, I realized that it was more complicated than I expected.

I started out by calling the custom hook boolean and function in the ChapterDetails component, but then, I realized that the Chapter parent component needed access to the boolean for every chapter in order to disable the completed chapters.

I took some time to draw out what this may look like as a diagram. Tomorrow I may create a new piece of state (perhaps an array or object) that keeps track of which chapters are completed. Originally, I thought that I could add the boolean to the piece of state (userData) that keeps track of the user's choices from each chapter (one per chapter), but this piece of state is an array, and the items in it will oftentimes have a different order than the chapter order. For example, if the chapters are:

Forest, Mountain, Swamp, Desert

The player may visit them in this order:

Mountain, Desert, Forest, Swamp

In that instance, the items would be placed in the userData array in that order, which would allow the final component to displace the user choices in the proper order (the order that they were selected): Mountain choice, Desert choice, Forest choice, Swamp choice.

However, the chapters array would remain in the original order, and the booleans linked to each chapter would have to be in that order too. As the user visited the chapters in the above order, it could look like this:

Forest: false, Mountain: false, Swamp: false, Desert: false
Forest: false, Mountain: true, Swamp: false, Desert: false
Forest: false, Mountain: true, Swamp: false, Desert: true
Forest: true, Mountain: true, Swamp: false, Desert: true
Forest: true, Mountain: true, Swamp: true, Desert: true

Anyway, long story short (too late), the userData array would oftentimes be in a different order than the chapters array, and the completed array would have to be in the same order as the chapters in order for them to line up properly.

So I guess the real long story short is that I still need to do more planning for this next step of disabling chapters as they are completed. Looking forward to the challenge!

**Link(s) to work**
1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Commit #1 - create custom hook](https://github.com/franco-ortega/ts-02-storybook/commit/5f4e8445b5cea8140fa357640eeb96348fb2c655)
1. [Commit #2 - implement custom hook](https://github.com/franco-ortega/ts-02-storybook/commit/c7dd9e6e96f32192bce7b5de84c6bedcab7a3d0c)
1. [Storybook Website](https://tell-your-tale.netlify.app/)


---

### Day 53: Wednesday, September 22, 2021

**Project:** Storybook

**Tech:** React, TypeScript

**Today's Progress:** (2 hrs) I created the Story component. The user will be redirected here when they have selected enough choices to complete their story, and the completed story will be displayed on this page.

**Thoughts:** Much of this session was actually spent trying to disable individual chapters after the user makes their selection from the respective chapter. I know how to do this with JavaScript and React, but I kept getting errors from TypeScipt. I tried a few different options, and I seemed to have the most success with using the useState hook to create an object (completed) that could take in any amount of properties that were added dynamically, but I couldn't get the setter function (setCompleted) to work without TypeScript errors. The error said something like that it wasn't allowed to return the type "void" for something that had the property [key: boolean], and when I tried returning that propety, it said something like Object<validtor> wasn't valid.

Anyway, after close to 90 min of trying and failing to make TypeScript happy, I decided to put this on the backburner and move on to the next step. Which was creating the Story component to display the completed story. I was able to do this relatively quickly, and in doing so, I successfully used the reduce method for the first time. Each piece of the story was an string in an array, and at first, I used the map method to place each piece into an p-tag and then display those elements on the screen. But then, with the reduce method, I was able to concatenate all the pieces into a single string and display it in a single p-tag. Instead of having a p-tag for each piece.

**Link(s) to work**
1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Pull request](https://github.com/franco-ortega/ts-02-storybook/pull/5)
1. [Storybook Website](https://tell-your-tale.netlify.app/)


---

### Day 54: Thursday, September 23, 2021

**Project:** MEAN Todo App

**Tech:** MongoDB, Express, Angular, Node

**Today's Progress:** (1 hr) I started making a Todo app with the MEAN stack. Today I built the API and database for the server and then started to create the client.

**Thoughts:** My stack is the PERN stack (PostgreSQL, Express, React, Node). I am currently taking a Udemy course to learn more about Node (see link below), and the final part of this course is to build a Todo app using the MEAN stack. I have seen a tiny bit of Angular and Mongo but have never worked with them, so it was neat to finally try them out. Also, this course is at least a few years old, so some of it is outdated. The course used MLab for the Mongo database, but Mlab no longer accepts new users, so I had to sign up straight with MongoDB. The process was different than what was outlined in the course. Also, some of the Angular code used in the course is now deprecated. However, in both instances, I was able to figure out how to do all this in the current way, so that felt good. Sure helps me feel more like a professional. :)


**Link(s) to work**
1. [Learn and Understand NodeJS](https://www.udemy.com/course/understand-nodejs/)
