# 1. August

1. [August](#1-august)
1. [September](#2-september)
1. [October](#3-october)
1. [Bottom](#4-bottom)

---

### Day 1: Sunday, August 1, 2021

**Project:** Hide & Seek game where the computer and user alternate between hiding an item and finding the hidden item. The game logic is complete for this current version. Now I'm working on the styling, which is an area that I want to improve in general. My current tasks are to add colors and to fine tune the responsive layout. I used the [Coolors](https://coolors.co/) website to help pick my color palette.

**Tech:** React, Sass

**Today's Progress:** (~90 min) I moved a dropdown menu from the Home page to the Welcome page. Then, I adjusted the styling on the Welcome page for four screen sizes (mobile, tablet, desktop small, desktop large).

**Thoughts:** Yesterday, I spent over an hour adding the colors to the Welcome page and fine tuning its layout. However, in addition to wanting to move the dropdown menu to the Welcome page today, I also wanted the Welcome page styling to be more consistent with the styling on the Home page. This was tricky to achieve because the two pages have very different amounts of content, and even now, not all the styling is the exact same (especially not on smaller screen sizes), but they are a lot more consistent. The work yesterday and today took much longer than I expected, but I am happy with the results. Tomorrow I will update the styling on the Game page.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/hide-and-seek)
2. [Pull Request](https://github.com/franco-ortega/hide-and-seek/commit/6f9262b1c17cd24118c48f606b812ce70141dec7)
3. [Website](https://hide-and-seek-game.netlify.app/)

### Day 2: Monday, August 2, 2021

**Project:** Hide & Seek game where the computer and user alternate between hiding an item and finding the hidden item. The game logic is complete for this version. Currently working on the styling.

**Tech:** React, Sass

**Today's Progress:** (~2 hr) Started working on adding colors and updating the styling to the Game page, which also included the Scoreboard and GameBoard components. Only got to the layout for the mobile view, and that still needs work.

**Thoughts:** I was able to apply the colors fairly quickly. However, it turned out that there needed to be a lot of restructuring of the Game and Scoreboard components while working on the layout of the components and elements. The trickiest part was that the amount of content in one p-tag changed throughout the game, but it needed to remain a consistent size the whole time; otherwise, the items below it would shift around. Although, I didn't want all the p-tags to have that same size. I had been using Display Flex but switched to Grid, which worked, but it also caused other problems. In the end, I switched back to Flex and used a CSS selector combinator to target the proper p-tag without affecting any of the other p-tags.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/hide-and-seek)
2. [Pull Request](https://github.com/franco-ortega/hide-and-seek/commit/38b185b77fcab01794b39f55c639229778daf100)
3. [Website](https://hide-and-seek-game.netlify.app/)

### Day 3: Tuesday, August 3, 2021

**Project:** Hide & Seek game where the computer and user alternate between hiding an item and finding the hidden item. The game logic is complete for this version. Currently working on adding styling and fine tuning the layout.

**Tech:** React, Sass

**Today's Progress:** (~4 hr) Made a lot of progress on the third (out of 4) page - the Game component, which also included the Scoreboard, GameBoard, and HidingSpot components. Got a lot of the layout and styling fine tuned. I learned how to style disabled buttons, too, by using the **:disabled** pseudo-class. Additionally, I did a lot of refactoring to clean up the custom hook that handles the many messages (and different types of messages: instructions, results, round change) that are dynamically rendered to the screen during gameplay. This last effort included the replacing of multiple **if statements** with **switch statements**.

**Thoughts:** I worked twice as long as I expected, but it felt good to feel like I was making progress most of that time. This week I'm gaining a much better understanding of custom hooks - what they can and cannot do. Also, it was really nice to clean up the code because things got somewhat clunky as I added more features. I made a plan when I started this project, and that plan was a great guide. However, I didn't update the plan as the project grew and evolved. New features were plugged in here and there, but I didn't take enough time to step back and look at the big picture, so this was a good lesson in the importance of updating plans with every new version of a project. It would've been nice to have kept documentation on the changes too. Next time. Additionally, I had thought that pseudo-classes didn't work on mobile, so I had been avoiding them. But apparently, maybe it's only **:hover** that doesn't work properly on mobile. Anyway, this was great to realize, so now I'll start digging more into pseudo-classes. Finally, switch statments were something that I pretty much never used during code school cos they seemed hard for my newbie brain to understand, or at least remember. However, today it was relatively easy to implement them. It sure feels great when something that was super hard is now pretty easy.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/hide-and-seek)
2. [Commit](https://github.com/franco-ortega/hide-and-seek/commit/5325c16bf0b3df3875719ac76016934219417872)
3. [Website](https://hide-and-seek-game.netlify.app/)

### Day 4: Wednesday, August 4, 2021

**Project:** Hide & Seek game where the computer and user alternate between hiding an item and finding the hidden item. The game logic is complete for this version. Currently working on adding styling and fine tuning the layout.

**Tech:** React, Sass

**Today's Progress:** (~2 hr) Added styling to the fourth and final page of the app: the Results page where the user is directed when the game ends.

**Thoughts:** It's been fairly tricky trying to apply consistent styling to each page since they all have different amounts of content and somewhat different elements. However, it feels good for everything to finally have the same color scheme and a pretty similar layout. I think and hope that fine tuning it all will go relatively quickly. Also, adding opacity to the styled buttons when they are disabled has been quirkier than I anticipated. The original issue was that the buttons were taking on the color of their backgrounds on mobile devices (why??), so I applied colors to their backgrounds to help differentiate them from the actual background. However, when I did this, the default styling (that faded look) for buttons was no longer being applied. So, I manually turned down the opacity a little, which looked as expected when viewed locally. However, on the live site, the small degree of opacity appears to make the buttons totally invisible when disabled, which is not the desired effect. So, I'll look into that tomorrow.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/hide-and-seek)
2. [Commit](https://github.com/franco-ortega/hide-and-seek/commit/20acbb7d4d3b25687c0d5f5c9494b573a4ad30d5)
3. [Website](https://hide-and-seek-game.netlify.app/)

### Day 5: Thursday, August 5, 2021

**Project:** Hide & Seek game where the computer and user alternate between hiding an item and finding the hidden item. The game logic is complete for this version. Currently working on adding styling and fine tuning the layout.

**Tech:** React, Sass

**Today's Progress:** (~4 hr) Worked on making the styling more consistent across all 4 pages and the header on mobile and tablet views.

**Thoughts:** My initial styling efforts focused on one page at a time with media queries for a total of 4 different screen sizes. However, this resutled in some consistency variations between each pages. The degree of inconsistency seemed to increase from page to page from first to last Also, the main Game page, which houses the most components, differed most from all the otehr pages. I almost tried to make the Game page styling line up more with the rest of the pages, but then, I opted not to go down that rabbit hole. It looks good as it is, and a more unique look may be apprpriate for the main page since it is where users will spend their most time. Next time, though, instead of doing one page at a time for all screen sizes, I may focus on doing all the pages for one screen size before moving onto the next screen size. That way I can see how the entire app design changes on the next screen size, instead of just one page at a time. Also, using more CSS variables would be helpful for keeping things (like font sizes) consistent across all the pages, and if/when I do change a font-size, it will change on all pages at once simply by changing the value of the variable. Lessons learned. Also, I used the nth-child CSS property today for the first time to give a unique styling to the third (out of four) section on the Game page. I was having a lot of trouble targetting just that one until I used the nth-child property. I could have used a class to target it specifically, but I'm trying to keep my class names to a miminum of one per page.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/hide-and-seek)
2. [Commit](https://github.com/franco-ortega/hide-and-seek/commit/52db72a7b5e66537d08e0933ddaf94a9319f615f)
3. [Website](https://hide-and-seek-game.netlify.app/)

### Day 6: Friday, August 6, 2021

**Project:** Tailwind demo.

**Tech:** React, Tailwind

**Today's Progress:** (~2 hr) This morning I tuned into a great Tailwind presentation by [Tis Lais](https://github.com/tislais/) that was clear and thorough. It focused on using Tailwind with React, and she even shared how to maneuver some of the trickier aspects of installation at the beginning and deployment on Netlify at the end. Then, this afternoon, I spent a couple hours spinning up a quick, simple project to start to get a feel for Tailwind.

**Thoughts:** I'd been meaning to checkout out Tailwind since March but kept putting it off because other practicing and learnings took priority. However, also, I wasn't sure how complicated it would be to figure out. But the presentation today was very well done and made me feel like I could give it a go. And indeed, I was able to install and configure everything relatively quickly and very smoothly. Also, I learned enough during the presentation to have a good feel for how to implement the Tailwind code in a React app. The tricky part about the Netlify build did trip me up and took a few times to sort out, but again, the issue was solved super quick thanks to the guidance by the presenter this morning. If you feel fairly comfortable with CSS, I definitely recommend giving Tailwind a whirl. The documentation is very helpful, and the built-in styling can be implenented pretty quickly. Also, there are option for customization as well.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/demo-tailwind-01)
2. [Website](https://amazing-fantasy.netlify.app/)
3. [Presenation repo by Tis Lais](https://github.com/tislais/project-owlfeather)
4. [Presentation site by Tis Lais](https://owlfeather.netlify.app/)

### Day 7: Saturday, August 7, 2021

**Project:** Server-03

**Tech:** Node, Express, PostgreSQL

**Today's Progress:** (~90 min) I started building a server with a RESTful API and relational database. I implemented test-driven development while creating one table (tiles) with a corresponding model (Tile) and a POST endpoint.

**Thoughts:** I did as much as I could from memory without using references. I did very well with this for the app.js and server.js files. I did pretty well with the table and model. The test and endpoint were somewhat trickier, but I was able to get close to completing them from memory. The only file that I needed to pretty much completely reference from past projects was the pool.js file. All in all, I feel good about my effort and progress this evening.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/demo-server-03-joins)
2. [Commit](https://github.com/franco-ortega/demo-server-03-joins/commit/447f33c52e78e9b397f17866a8c73564711072f8)

### Day 8: Sunday, August 8, 2021

**Project:** Server-03

**Tech:** Node, Express, PostgreSQL

**Today's Progress:** (1 hr) I added two GET routes (get all, get by id), one PUT route, and one DELETE route for the tiles table along with their correspondings methods and tests.

**Thoughts:** Everything went rather smoothly. I was able to write most of the code from memory, and debugging the mistakes went relatively quickly. Also, before I was re-creating the table before each test, but now the table is created only once before any tests are run, so the tests work off each other. That could get somewhat risky with a bigger batch of tests, but it seems very manageable with only five tests.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/demo-server-03-joins)
2. [Pull Request #1](https://github.com/franco-ortega/demo-server-03-joins/commit/644d8d08d3a8b0f1db612da95bfc4cef52e76b45)
3. [Pull Request #1](https://github.com/franco-ortega/demo-server-03-joins/commit/ce90443a9bda11d119c23f88f6d7038db0ee444a)

### Day 9: Monday, August 9, 2021

**Project:** Server-03

**Tech:** Node, Express, PostgreSQL

**Today's Progress:** (1 hr) I added a second table (floors) to create joins with the first table. ALso, I added created a Floor model with a POST endpoint and two GET endpoints (get all, get by id) as well as their correspondings methods and tests.

**Thoughts:** Things went pretty smoothly. The hiccups were: 1) I forgot to add the CASCADES keyword to drop the main table; 2) I created a floor in the "get by id" test with a post request, which gave me an issue because I was dynamically creating up its endpoint with its id, but floor.id was resulting in a failed request because it turned out that I needed to use floor.body.id to get the floor id out of the response via the response body; 3) I had to decouple the tiles tests to run independently of each other because now the tiles were tied to the floors table, and that was causing issues with the tiles tests.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/demo-server-03-joins)
2. [Pull Request](https://github.com/franco-ortega/demo-server-03-joins/commit/07081371878ba40b7c1c7a86a929cbdf345639e6)

### Day 10: Tuesday, August 10, 2021

**Project:** Python Games

**Tech:** Python

**Today's Progress:** (1 hr) I built a four games with Python today: Mad Libs, Guess A Number (two versions: one where the player guesses and one where the computer guesses), and Rock Paper Scissors. You can check out the tutorial here: [12 Beginner Python Projects](https://www.youtube.com/watch?v=8ext9G7xspg).

**Thoughts:** I played with Python a tiny bit earlier this year, but today I started to really learn it. The main reason is because a company I'm interviewing with - which seems mostly JavaScript-based (React, Node) - seems to have a bit of Python in their tech stack. I actually started by learning about NumPy, which was mentioned in the job post, and then I watched a couple hours of a video tutorial for beginners: [Learn Python - Full Course for Beginners](https://www.youtube.com/watch?v=rfscVS0vtbw). After that, I started building the games. Python seems similar enough to JavaScript that I've been able to follow along pretty easily. The main difference that I've noticed so far is that Python lists appear to be more powerful than JavaScript arrays. Especially when used with NumPy to create multi-dimensional arrays. This was the NumPy tutorial: [Python NumPy Tutorial for Beginners](https://www.youtube.com/watch?v=QUT1VHiLmmI)

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/python-01-games)
2. [Pull Request](https://github.com/franco-ortega/python-01-games/commit/37a2fc44a24716a8db817b729dd4cd16781e6ef9)

### Day 11: Wednesday, August 11, 2021

**Project:** Portfolio

**Tech:** React

**Today's Progress:** (3 hr) I did some reading to get a better understanding of the "children" prop in React. Then, I made use of the children prop to create a reusable component for some of the popups on my portfolio site. Each popup has different kinds and amounts of elements, and the children prop was perfect for handling these kinds of differences among child components who using the same reusable parent component.

**Thoughts:** My portfolio site is map-themed. I was hoping to use a lot of reusuable components for the landmasses. Especially since the landmasses were composed of nested elements that were practically identical in amount and kind. However, one issue for the large continents was that they were all-shaped differently, and this shape was determined by the outermost element, so it didn't seem convenient (or even possible?) to create a reusable component that had different styling on the outermost level. It seemed more feasible to have the outer layer be the same and then pass in more varied components as the children. But that did not work for what I was creating. On the flip side, I was able to create a reusable component for the small islands because they had identical styling as well as the amount and kind of content was the same for each one (a pair of strings passed as regular props). Additionally, each continent could be clicked to open a popup with more details. Originally, the popups all had different shapes, too, but I streamlined their shape last month. Yet their contents remained very varied, so they didn't seem suitable to use with a reusable component. However, getting a better understanding of the children prop today made me realize that I could use that to create a reusable parent component for the continent popups. This allowed me to remove CSS that was repeated in multiple continent files and place it in the new reusable component. Then, I called the reusable component into each of the continent files and wrapped it around their content. Also, apparently, the children prop wraps the child component in a div, and that extra element caused some problems with CSS because that div was now a new layer between the original layers of the popup, so I did have to add back a tiny bit of CSS back into the continent popups, but overall, the reusable component still notably reduced the total amount of CSS.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/portfolio)
2. [Pull Request](https://github.com/franco-ortega/portfolio/commit/26a3b457f4d6208f7d1cb80c35a37e04c20e0573)
3. [Website](https://francoortega.com/)
4. [Children in JSX](https://reactjs.org/docs/jsx-in-depth.html#children-in-jsx)

### Day 12: Thursday, August 12, 2021

**Project:** Hide & Seek

**Tech:** React, Sass

**Today's Progress:** (2 hr) I finalized the styling to make it consistent on all pages and make it responsive across four screen sizes. Also, I removed a piece of state that turned out to be repetitive, and I was able to consolidate two variables - that served different purposes but were actually created the same way - into one.

**Thoughts:** Styling is an aspect of web development that I want to get better at, but I tend to put it off or not really get to it with personal projects, so it felt great to devote time to figuring out colors and a layout that I really liked. It took much longer than I expected to apply the styling to every page for every screen size, and then, to make sure it was consistent, but I did it, and I learned some good lessons along the way. Lessons about CSS and the process of applying and fine tuning styling.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/hide-and-seek)
2. [Pull Request](https://github.com/franco-ortega/hide-and-seek/commit/c6f3c4f50c060970d2e755967eab0f84bf64dcc2)
3. [Website](https://hide-and-seek-game.netlify.app/)

### Day 13: Friday, August 13, 2021

**Project:** Phaser.io Game

**Tech:** Phaser.io, Node, Express

**Today's Progress:** (~3 hr) I attended a great presentation on [Phaser.io](https://phaser.io/) by [Cameron Zimmerman](https://github.com/CameronZimmerman) who provided everyone with a repo to clone down and code along. The project was a game where a character scored points by flying in between stationary obstacles. It was a very fun 2-hr demo, and I spent about another hour finishing it up and debugging.

**Thoughts:** I'm a big fan of games, so getting an introduction to a gaming framework was a big treat. There is certainly much more learn, but this introduction provided a very helpful gateway into Phaser.io. I don't have my code for this on GitHub, but you can check out Cameron's repo for his version: [Flappy Duck repo](https://github.com/CameronZimmerman/phaser-flappy-duck-finished)

### Day 14: Saturday, August 14, 2021

**Project:** Hide & Seek

**Tech:** React, Sass

**Today's Progress:** (1 hr) I added Context (as in React Context) to handle the player state that is used in most of the components.

**Thoughts:** I had only used Context a couple times before, and this was back in the spring. I was somewhat fuzzy on how to write the code for it back then, but this time it was pretty quick and easy to add it to this app. I wouldn't say that I understand it well yet, but it's starting to click much better than it did 6 months ago.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/hide-and-seek)
2. [Pull Request](https://github.com/franco-ortega/hide-and-seek/commit/8eec4fbc33683737cb0c7e21b9e3c75fde92db47)
3. [Website](https://hide-and-seek-game.netlify.app/)

### Day 15: Sunday, August 15, 2021

**Project:** Hide & Seek

**Tech:** React, Sass

**Today's Progress:** (2 hrs) I did a lot of refactoring today. I removed the gameOver state, which was mostly created to determine when the Scoreboard was rendered in the Header (which was only during gameplay). However, now the Scoreboard is rendered in the Game component, which itself is only rendered during gameplay, so the Scoreboard no longer needed conditional rendering. Then, I used to gameActive state to take over the remaining purpose of the gameOver state, which was to display a "Game Over" message when the game ends.

Additionally, I added the gameActive state to the Context.

Finally, I refactored the two useEffects in the Game component to reduce repetitive code in the first one, and to more accurately define the conditional statements in the second one. Also, I added a gameOver variable to the first useEffect to make it more obvious what the conditional statements were checking.

**Thoughts:** It felt really great to clean up the code and make it more readable.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/hide-and-seek)
2. [Pull Request #1 - refactor](https://github.com/franco-ortega/hide-and-seek/commit/f6aa334f750a2210c69a165333a5653a849f02ea)
3. [Pull Request #2 - context update](https://github.com/franco-ortega/hide-and-seek/commit/ace4883d4cc1cf2265b02457eed27eb49801e1f8)
4. [Pull Request #3 - refactor useEffects](https://github.com/franco-ortega/hide-and-seek/commit/f8b9dd1d1faea56486a3ae7118c29aa3c450de84)
5. [Website](https://hide-and-seek-game.netlify.app/)

### Day 16: Monday, August 16, 2021

**Project:** Hide & Seek

**Tech:** React, Sass

**Today's Progress:** (1 hr) I implemented suggestions that were kindly provided by [Matan B.](https://github.com/MatanBobi). This included the refactor of a function to remove an unnecessary variable, as well as creating a couple enum-like objects for passing around strings as object property values instead of directly passing the strings themselves. The refactor helped the function looked cleaner, and the enums are meant to help avoid typos.

**Thoughts:** I've been on a big refactoring kick, so it was fun to get advice from someone else on how to do more of it.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/hide-and-seek)
2. [Pull Request #1](https://github.com/franco-ortega/hide-and-seek/commit/f0b2f7d620cf5f22f0cf22183be080b479c8df8e)
3. [Website](https://hide-and-seek-game.netlify.app/)

### Day 17: Tuesday, August 17, 2021

**Project:** Rest

**Tech:** Couch, bed.

**Today's Progress:** Going to bed on time.

**Thoughts:** I did a lot of work today, which included a few hours of job searching, two pet sitting gigs, studying, physical therapy, and cooking. I could have squeezed in an hour of coding, but taking breaks is super important in this line of work, so I opted to get proper rest instead of needlessly pushing myself.

### Day 18: Wednesday, August 18, 2021

**Project:** Code Challenge

**Tech:** Leet Code

**Today's Progress:** I worked on two code challenges today. The first took in an array of sorted numbers and a target number. The task was to find the target number's location in the array and return the index, or if it wasn't in the array, to return the location where it would go in numerical order. The second code challege provided an array of sorted numbers and function that determined which numbers broke another piece of code. The task was to determine what was the first number to break the code.

**Thoughts:** The first code challenge was relatively easy to solve with a for loop. Although, initially, I didn't account for numbers that were lower than the first number in the array or higher than the last number, but that was a pretty quick fix. The second code challenge required a binary search algorithm. I've been diving deeper into algorithms lately, so it was good to come across a code challenge that required one that I recently got a better understanding of.

### Day 19: Thursday, August 19, 2021

**Project:** Glowing Colors

**Tech:** React, CSS

**Today's Progress:** I started work on a site that will display colorful orbs which fade in and out of existence.

**Thoughts:** I made good progress on creating the orbs and rendering the colors dynamically, so every orb has different colors, and the colors change on every page load. Then, I used an animation to make the orbs fade in and out of view. Toward the end of this session, I used a setInterval to make the orbs change colors every time they went out of view. This worked well for the first few fades in and out, but soon, the color change and fade fell out of sync, and a little while later, the colors started changing very rapidly. I'm not entirely sure what is causing this issue, but I blame the event loop.

### Day 20: Friday, August 20, 2021

**Project:** Job Searching

**Tech:** Job Sites, Networking

**Today's Progress:** Lots of job searching today, which included an online career fair. I applied to a bunch of places for a total of 25 this week, which is notably higher than my previous record last week of 15 applications.

**Thoughts:** Out of the 25 applications, only 7 were full-on application with lengthy questions and/or cover letters that took an hour or two to write. The rest received cover letters that were quicker to write, or they didn't accept cover letters at all. My aim is to send out one application per weekday that inspires my to put a lot of effort into the cover letter, plus another 2+ applications that I can complete quickly. Usually, this takes 3 hrs per the morning, but next week I'm going to try and get it done in 2 hrs.

### Day 21: Saturday, August 21, 2021

**Project:** Rest

**Tech:** Couch, bed.

**Today's Progress:** A day of rest after a very long week of job searching and attending networking events.

**Thoughts:** Rest is super important.

### Day 22: Sunday, August 22, 2021

**Project:** Glowing Colors

**Tech:** React, CSS

**Today's Progress:** Today I restared this project pretty much from scratch in order to implement test-drive development.

**Thoughts:** I flew through making this site last Thursday, but now I want to take a somewhat slower approach. Also, I need to brush up on my testing skills, so I spent time watching a tutorial on the React Testing Library. It was super helpful. The link is below.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/glowing-colors)
2. [Pull Request](https://github.com/franco-ortega/glowing-colors/commit/76ebc13654210f92828617997af4d817d9268698)
3. [React Testing Library Tutorial](https://www.youtube.com/playlist?list=PL4cUxeGkcC9gm4_-5UsNmLqMosM-dzuvQ)

### Day 23: Monday, August 23, 2021

**Project:** Glowing Colors

**Tech:** React, CSS

**Today's Progress:** (5 hrs) Today I brought the project up to speed to where the rough draft version was last week. I still struggled with the timer and animation being out of sync, but after much wrangling and thinking deeper about the issue, I was able to create a solution, and now it's working great!

**Thoughts:**

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/glowing-colors)
2. [Pull Request](https://github.com/franco-ortega/glowing-colors/commit/acd84ce52d84d289c637793483db2882f958e157)
3. [Glowing Colors Website](https://glowing-colors.netlify.app/)

### Day 24: Tuesday, August 24, 2021

**Project:** Glowing Colors

**Tech:** React, CSS

**Today's Progress:** (2 hrs) I spent an hour adding functionality to have to orbs appear in random locations on the screen. Then, I spent another hour refactoring the "random location" code into a single function that was moved into the utils file, and I refactored the other utils functions too.

**Thoughts:** It felt great to get the site working even more how I envisioned. It was really nice being able to clean up the code and trim it down while making it more readable too.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/glowing-colors)
2. [Pull Request #1](https://github.com/franco-ortega/glowing-colors/commit/38ead2abca07164843bd6d37ba6aa5d2d0d43190)
3. [Pull Request #2](https://github.com/franco-ortega/glowing-colors/commit/565737c07295ddddd9b5b8b6946e8386e102dfe3)
4. [Glowing Colors Website](https://glowing-colors.netlify.app/)

### Day 25: Wednesday, August 25, 2021

**Project:** Glowing Colors

**Tech:** React, CSS

**Today's Progress:** (1 hr) The height and width of the orbs are now created dynamically and randomly each time an orb is rendered, so every orb is a different size. Also, I added tests for some of the functions from yesterday's refactor.

**Thoughts:** The dynamic styling is being added each Orb component via inline styling as it is created. I wasn't sure how to input the height and width in this manner while also maintaining a responsive design. The orbs had a height/width of 75px on mobile and 100px on larger screens. The dynamic height/width has a range between 0px and 200px, but I didn't want the orbs to get that big on mobile screens. Luckily, I was able to utilize the the max-height and max-width properties, which I only recently got more familiar with, in the CSS module for the Orb component, and that successfully capped the height/width of the orbs on mobile.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/glowing-colors)
2. [Pull Request](https://github.com/franco-ortega/glowing-colors/commit/0965f0484c0cd02ca7445da3a144a2714aaabaa3)
3. [Glowing Colors Website](https://glowing-colors.netlify.app/)

### Day 26: Thursday, August 26, 2021

**Project:** CSS Sandbox

**Tech:** React, CSS

**Today's Progress:** (1 hr) I watched a video tutorial that did a great job of explaining hsl color codes. Also, it demonstrated the benefit of using CSS variables for the different parts of the color code. I highly recommend checking it out: [hsl tutorial](https://www.youtube.com/watch?v=EJtmfkKulNA&list=PLZlA0Gpn_vH8mpXIUHjWoMAAgoCEinL0R&index=7&ab_channel=WebDevSimplified). Also, before doing this, I cleaned up one of the older files, and then added a Nav component

**Thoughts:** I have mostly used the named color codes (i.e. green, red, etc) for my styling, and more recently, I've been utilizing rgb values to be able to adjust the opacity of the color as well. I didn't have much of an understanding of hsl, but now it makes much more sense to me. Also, I really like the flexibility that incorporating CSS variables adds to the use of hsl. Though, I don't have any particular use cases in mind for this yet. Also, I made this site several months as a way to experiment and play with new CSS properties. I had previously mostly just used it to learn grid, and I also dabbled a bit with making shapes like triangles.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/css-sandbox)
2. [Pull Request #1](https://github.com/franco-ortega/css-sandbox/commit/e0317294b698617b542d361369f855278526989c)
3. [Pull Request #2 - Nav](https://github.com/franco-ortega/css-sandbox/commit/4c3d51f8c7c3cdb05d2d221ee58789152533a2d7)
4. [Pull Request #3 - hsl](https://github.com/franco-ortega/css-sandbox/commit/19494766b37302608de7299fc0b4ce55128043b1)
5. [Website - CSS Sandbox](https://css-sandbox-playground.netlify.app/hsl)

### Day 27: Friday, August 27, 2021

**Project:** Glowing Colors

**Tech:** React, CSS

**Today's Progress:** (1 hr) The orbs are now clickable. Their styles change and transition with every click.

**Thoughts:** This feature was easier to implement than I expected, but it was also tricky to get it working properly. First, I created a new class with the transition. Next, I added the class as a second inline style to the orb, which was dependent on a new piece of state - a boolean that began as false. When the orb was clicked, the boolean was set to true, and that did a couple things:

1. It applied the new class name to the orb.
2. the change of state caused the orb to be re-rendered, or at least it causes the function that generates the dynamic stlying to re-run, and either way, this generated a new set of styling with the creation of new orb.

This worked well, and the newly generated styles were applied smoothly thanks to the transition. This allowed the styles on an orb to be changed once with a click. Then, I updated the function that changed the boolean to set it to the opposite of its previous value. This allowed a new style to be generated for an orb every time it was clicked. However, this also caused a couple issues:

1. Whenever the boolean was clicked back to false, this removed the class with the transition, so the orb changed suddenly and sharply instead of smoothly; I was able to rectify this by adding a transition to the original (and constant) class name for the orb, but this led to another issue.
2. Everyonce in a while, the orbs would transition as soon as they were rendered. I don't understand why this happened, or why it only happened occasionally, or why only some of the orbs of a single collection would behave this way (as opposed to all of them).

It took a bunch of troubleshooting and experimenting, but I discovered a solution. I created a second piece of state, which was also a boolean. This allowed me to split up the actions. One boolean was used to apply the new class name with the transition, so it began as false and was changed to true on click. The other boolean was set to change to the opposite value (i.e. setState(!boolean) ), so every time it was clicked, the orb re-rendered, but it still had the new class name with the transition. Success!

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/glowing-colors)
2. [Pull Request](https://github.com/franco-ortega/glowing-colors/commit/51f2ec5bc2c4466b9d07b01b411ab7ede5b375bf)
3. [Glowing Colors Website](https://glowing-colors.netlify.app/)

### Day 28: Saturday, August 28, 2021

**Project:** Rest

**Tech:** n/a

**Today's Progress:** A day of rest.

**Thoughts:** n/a

### Day 29: Sunday, August 29, 2021

**Project:** Glowing Colors

**Tech:** React, CSS

**Today's Progress:** Did some planning for adding a Welcome component that will provide instructions to the user.

**Thoughts:** At first I was thinking of creating a landing page that would link to the page with the glowing color orbs. However, I then decided to make it a component that would be visible on load - like a landing page - but when the user clicks on the button to proceed, the Welcome component fades out of view and is un-rendered.

### Day 30: Monday, August 30, 2021

**Project:** Glowing Colors

**Tech:** React, CSS

**Today's Progress:** (1+ hr) I built the first phase of the Welcome component.

**Thoughts:** This first phase includes the bulk of the content and styling. I placed the component in the center of the screen by using _position: relative_ with a _top_ and _left_ values of 50% combined with _transform: translate(-50%, -50%)_. Also, I am making this component responsive without the use of media queries by using the _clamp_ function with relative lengths for the font-sizes and providing the component a width of fit-content to stretch to fit the text, plus a max-width of 80% to prevent it from touching the sides of the screen on smaller screens.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/glowing-colors)
1. [Commit #1 - test for Welcome component](https://github.com/franco-ortega/glowing-colors/commit/0ce17cd9be8f08ab255c52883f59cf4acd9a1d3f)
1. [Commit #2 - initial Welcome component](https://github.com/franco-ortega/glowing-colors/commit/51b16750d3c8061cc38ea30ec9ed08d288964f30)
1. [Commit #3 - initial styling for Welcome component](https://github.com/franco-ortega/glowing-colors/commit/3b34f6ad3f21025700051c473e5f132a139c09d6)
1. [Commit #4 - added content and styling for Welcom Component](https://github.com/franco-ortega/glowing-colors/commit/fabbddb15d8ed54b0f110af3b9a9469521aac4e9)
1. [Glowing Colors Website](https://glowing-colors.netlify.app/)
1. [Clamp function](<https://developer.mozilla.org/en-US/docs/Web/CSS/clamp()>)

### Day 31: Tuesday, August 31, 2021

**Project:** Todo List App

**Tech:** React, CSS

**Today's Progress:** (5 hr) I spent today refreshing myself on class components in React, which I haven't used in about 6 months. When the user submits a todo, it is immediately displayed on the screen along with a button that will delete all the todos. Additionally, every time a todo is added, the entire list of todos is placed in local storage. When the page is reloaded, the todo list is retrieved from local storage. Finally, when the Delete button is clicked, the todo list is removed from the page and local storage.

Also, I spent some time trying out the CSS functions clamp, min, and max.

**Thoughts:**

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/demo-react-01-todos)
1. [Pull Request](https://github.com/franco-ortega/demo-react-01-todos/commit/c683fdf320c96350bc66e38d9762c2d3bf88892d)
1. [Website](https://a-list-of-todos.netlify.app)

---

---

## 2. September

1. [August](#1-august)
1. [September](#2-september)
1. [October](#3-october)
1. [Bottom](#4-bottom)

---

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

**Tech:** React, TypeScript

**Today's Progress:** (~6 hrs) I started building an app where the user will build a story by visiting different lands in any order they wish, and then selecting a sentence from each land. When they have visited all the lands, their completed story will be displayed.

**Thoughts:** I'm getting back into TypeScript, and this will be my first fully-fledged app that combines it with React. I spent almost an hour watching video tutorials followed by more than an hour sketching out a plan on Miro. Then, I spent several more hours using test-driven development (TDD) to start building the app. I set up the App component with a router and created the initial Prologue component with a form, and the initial Chapters component with test data. It's coming together nicely so far.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Pull Request #1 - Prologue component](https://github.com/franco-ortega/ts-02-storybook/commit/45d24ecb55953ea8fddc88204095b56c5cac672c)
1. [Pull Request #2 - Chapters component](https://github.com/franco-ortega/ts-02-storybook/commit/4dd5ebd4a2eb6fd0895bd2ab33d941a1e93cbfe4)

---

### Day 38: Tueday, September 7, 2021

**Project:** Storybook

**Tech:** React, TypeScript

**Today's Progress:** (3 hrs) I begin working a dynamic route linked to a reusable component that will receive props from a data file in order to generate most of the pages for this app.

**Thoughts:** I vaguely remember creating a dynamic route for a school project over 6 months ago. It was part of an app that fetched fictional character data (LotR) from an API. The title of each character was displayed on the page as a link. Clicking on a character link took the user to a page that displayed details of that particular character. A reusuable component was used to generate all the character details pages. So, the work today was not totally knew to me. I had done this sort of work at least once in the past (and probably more like a few times), but my memory was really fuzzy on it, and I had never done this with TypeScript before, so that made it extra tricky, but I seemed to get things most of the way there today. Also, I did most of the work today with a test component using data inside that same file just to see if I could get it working more or less properly.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Pull Request](https://github.com/franco-ortega/ts-02-storybook/pull/2)
1. [Website](https://tell-your-tale.netlify.app/)

---

### Day 39: Wednesday, September 8, 2021

**Project:** Storybook

**Tech:** React, TypeScript

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

**Today's Progress:** I created the logic that allowed the server to process data in a very specific way outlined in the requirement. There were 9 pieces of data that had to be sent to an external API for processing, and the processing of each piece of data resulted in multiple incoming requests to my server. However, I could not send all 9 pieces of data together or immediately consecutively. I could only send 3 pieces of data to start, and when 1 piece was completed, then I could send out the next one.

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

### Day 47: Thursday, September 16, 2021

**Project:** Take-Home Project (Fullstack app)

**Tech:** React, Node, Redis, webhooks

**Today's Progress:** My take-home project was rejected, but I was given the opportunity to make changes. I removed the Redis code that was storing the data (and its updates) in local memory. My new approach to storing the updated data was to use Node to write a file, and it would write to the file again with updates. This worked. Also, I created a work-around to avoid a bug that I discovered in the external API provided by the interviewer. This fix got the project working exactly as expected, so that was exciting!

**Thoughts:** The problem was that the project had to keep the state of the data (and updates to the data) in memory. I couldn't use a database, so I used Redis because that stored data in local memory. This seemed like an appropriate solution, but apparently, in the eyes of the interviewer, Redis counted as a database.

As for the bug, I realized that the reason one piece of data seemed to be processed strangely (by the external API provided by the interviewer) was because there was a bug in it. I handled this by checking for the behavior caused by the bug and responding in a way that processed the data as expected.

(This will be my last post about this project. I re-submitted, but it was rejected again. They didn't like my new approach to saving the data updates. And apparently, there is some other way to save updated data in Node that I don't know about yet because it turns out that was what they wanted. It would have helped if they made that clear because then I could have researched this approach to implement it. Also, they didn't provide any feedback about the rest of the project. That was disappointing. It would have been nice to know what they thought about the rest of it. Especially since it did work properly. They just didn't like one of my approaches. At least they did make the effort to give me code that was their guesstimate of how they wanted my code to look like, so I'll try updating mye project with their code to see if it still works that way.)

---

### Day 48: Friday, September 17, 2021

**Project:** Munge Data

**Tech:** JavaScript

**Today's Progress:** I helped a friend with a project. Their code did work on data received from a fetch request that resulted in an array of objects, and now they were trying to write a test for their code. I was able to help write a test for this code, but it wound up being a long, winding journey to get there.

**Thoughts:** I helped them start by putting the code in a function that could be called in a test file. This refactor went smoothly. However, we had a lot of trouble with setting up a test. It kept timing out, which seemed strange because it didn't seem to be doing a lot of work. However, in addition to returning the update data, their code was also return something that said <45546564 empty objects>, and there were a few of these items with different numbers in them. Eventually, I realized that <45546564 empty objects> was saying that the array had 45,546,564 empty objects in addition to the objects that contained data. No wonder the test kept timing out! It was doing a ton of work!! But why. It must have been something wrong with the code, so I looked closer at it. I hadn't looked too closely at the code before because it sounded like it was working like they expected. However, they hadn't understood what the "empty objects" message meant. Anyway, it look me a little to understand how their code was working, and I was able to spot the problem: they had mixed up the way to add items to an object with the way to change items in an array. They were using bracket notation to add items, which would work as intended for an object, but they were placing these items in an array, and they were doing so by the ID number, which was several numbers long - such as 45546564. The code looked something like this:

<pre>
const itemArray = []

let id = 0;

id = 45546564

itemArray[id] = { object with munged data }

</pre>

This code would add a single item to an object (if the property didn't exist already), but they were using it on an array, so it placed the item in the 45546564th index of the array and created 45546563 empty items in front of it, so that the new item could be placed in the 45546564th position.

Once I figured this out, it was easy enough to change the itemArray to an object, and then it worked as expected. No more empty items. And the test passed too.

---

### Day 49: Saturday, September 18, 2021

**Project:** Assessment

**Tech:** n/a

**Today's Progress:** I took an online assessment from company that I applied to earlier in the week.

**Thoughts:** It went smoothly.

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

---

### Day 55: Friday, September 24, 2021

**Project:** Storybook

**Tech:** React, TypeScript

**Today's Progress:** (1 hr) Between yesterday (1 hr) and today, I was able dynamically keep track of the chapters completed by the user in the ChapterDetails component. Then, I adjusted the Story component to work dynamically as well when concatenating each user selection to the final story.

**Thoughts:** I needed a way to keep track of which chapters were completed in order to know which chapters to disable (this work hasn't been done yet. My original efforts to do this with an object earlier this week went down in flames. However, I was able to accomplish it today by changing the userData array. Before, it held a string for the selection made by the user at each chapter. It was an array of strings. Now it is an array of sub-arrays. Each sub-array has the user selection as the first item, and the chapter title as the second item. I will be able to use these chapter titles to disable chapters (as they are completed) in the Chapters component. Progress. Not ideal, but still moving forward.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Pull Request #1](https://github.com/franco-ortega/ts-02-storybook/pull/6)
1. [Pull Request #2](https://github.com/franco-ortega/ts-02-storybook/pull/7)
1. [Website](https://tell-your-tale.netlify.app/)

---

### Day 56: Saturday, September 25, 2021

**Project:** Storybook

**Tech:** React, TypeScript

**Today's Progress:** (1.5 hrs) I finally updated the userData state to be an object!

**Thoughts:** I tried doing this several days ago but couldn't figure out the types to use to make TypeScript happy. I wound up having to scrap at least a couple hours worth of work/debugging that day and revert to a simpler, clunkier approach with an array. My initial plan today was to use the data in that array (in the sub-arrays of the array, to be exact) to disable each chapter after the user visited/completed a chapter. However, I decided to try to changing userData to an object one more time, and this time it worked! It went surprisingly smoothly. I guess getting some time away from it did help. StackOverflow helped a bit too. My biggest challenge today came with making the PropTypes happy with userData as an object instead of array. This is where StackOverflow helped most. The solution wound up being this:

<pre>userData: PropTypes.shape({}).isRequired</pre>

I don't like that the shape is just an object because each key in this object has another object as its value, and those objects have two properties with strings as values. Unfortunately, trying to be more specific with the shape was causing errors, so I'm just going to leave it like this for now.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Pull Request](https://github.com/franco-ortega/ts-02-storybook/pull/8)
1. [Website](https://tell-your-tale.netlify.app/)

---

### Day 57: Sunday, September 26, 2021

**Project:** Storybook

**Tech:** React, TypeScript

**Today's Progress:** (2 hrs) I was going to work on disabling the completed chapters. However, I realized that by moving all the user selections from an array to an object (that also kept track of which chapters had been completed), this meant that the user selections were no longer displayed in the order that they were selected. Because objects don't keep their properties in any particular order. Therefore, I decided to break up the user selections vs chapters completed into separate data structures. First, I made a new array to hold the user selections. Once that was created and captured the selections correctly, then I worked on redirecting the user to the Story component under the correct condition and properly displayed the user selections, Finally, I updated the "user seletion/chapter completed" object to only hold the "chapter completed" data.

Also, I placed all of the interfaces and types that were used in multiple files into their own utils files, and then exported them where needed.

**Thoughts:** This took longer than I would have expected, but it went relatively smoothly. I had to spend some time thinking how to rewire things, but I didn't get stuck on anything, so that felt great.

Also, I watched a few video tutorials that explained the differences between interfaces vs types, and they helped me understand their differences (capabilities and limitations) much better than the TypeScript docs or StackOverflow threads on the subject. Thank you, YouTubers! See their links below.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Pull Request #1 - change userData from array to object](https://github.com/franco-ortega/ts-02-storybook/pull/8)
1. [Pull Request #2 - separate user selections from chapters completed](https://github.com/franco-ortega/ts-02-storybook/pull/9)
1. [Website](https://tell-your-tale.netlify.app/)
1. [TypeScript Types Vs. Interfaces](https://www.youtube.com/watch?v=bEuXRAr0BVo)
1. [TypeScript: Interfaces vs Types - Learn in 5 minutes](https://www.youtube.com/watch?v=esWDwiFVqhw)
1. [TypeScript Interfaces vs Types](https://www.youtube.com/watch?v=crjIq7LEAYw)

---

### Day 58: Monday, September 27 2021

**Project:** Storybook

**Tech:** React, TypeScript

**Today's Progress:** I finally got around to disabling the completed chapters. Then, I did some refactoring to reduce the redundancy in the data file and make the naming of variables more consistent.

**Thoughts:** The redundacy is the data file was that each chapter title was the key for a chapter object (that held the selections to be displayed on each respective page), but each chapter title was also a value of a title property inside each chapter object. The key was lowercase, and the value was uppercase. I used the key (lowercase) to create the URLs for the links to each chapter page, and once inside a chapter page, the key was used with bracket notation to access the data of the respective object. Whereas, I used the value of the title property (uppercase first letter) to display the title on the Chapters page and ChapterDetails page. It took a while of experimenting to be able to remove the title property (uppercase) because I wanted the URL to remain lowercase. If the title had an uppercase first letter, I could use the toLowerCase method to make it all lowercase for the URL. However, once it was pulled out of the params in the ChapterDetails page, I was not able to make the first letter uppercase again in way that made TypeScript happy. I almost gave up on my effort, but eventually, I figured out a solution. I kept the title lowercase and created a function that would make the first letter uppercase for the places where the title would be displayed on the page.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Pull Request - disable completed chapters](https://github.com/franco-ortega/ts-02-storybook/pull/10)
1. [Pull Request - fine tune styling of disabled chapters](https://github.com/franco-ortega/ts-02-storybook/pull/11)
1. [Website](https://tell-your-tale.netlify.app/)

---

### Day 59 Tuesday, September 28 2021

**Project:** Storybook

**Tech:** React, TypeScript

**Today's Progress:** The logic was pretty much completed yesterday. Today I did some fine tuning and error handling.

1. I added a Go Back button to the reusable ChapterDetails component. This will allow the user to go back to the Chapters page.
1. I made added the required attribute to the input of the Prologue page (so the user has to enter a name to proceed) and the radio buttons of the ChapterDetails component (so the user has to make a selection to hit the Submit button).
1. I changed the New Story button to redirect the user to the Chapters page instead of the Prologue page. This allows the user with the same name to create a new story without having to re-enter their name on the Prologue page. This button still resets the userSelections state and completed state. Then, I added a New User button to the Story page, which resets all the state (userName, userSelections, completed) and redirects to the Prologue page to start from the beginning, so a new user can enter a new userName.

**Thoughts:** It felt good to be able to spot the errors that could happen without having the required attribute on the inputs. It was also nice to provide the user a way to exit the ChapterDetails page without having to submit a selection. Because maybe they want to look at all the chapters before making any selections. Adding the New User button felt like a helpful option, too, so that the current user could make a new story without having to re-enter their name, but they could also pass the device to someone new to make a story without having to manually go back through all the pages and reload the site.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/ts-02-storybook)
1. [Pull Request #1 - add Go Back button ](https://github.com/franco-ortega/ts-02-storybook/pull/12)
1. [Pull Request #2 - make inputs required](https://github.com/franco-ortega/ts-02-storybook/pull/13)
1. [Pull Request #3 - add New User button](https://github.com/franco-ortega/ts-02-storybook/pull/14)
1. [Website](https://tell-your-tale.netlify.app/)

---

### Day 60 Wednesday, September 29, 2021

**Project:** Sass Demo with React

**Tech:** Sass, React

**Today's Progress:** (2 hr) I started a new app to play with Sass and to implement with React in particular. I created variables for colors and fonts and used the @extend, @forward, and @use features.

**Thoughts:** This is my second time using Sass, and the first time was also with React. However, I used node-sass last time, and I know that version is being retired, so I wanted to see if I could figure out how to use to new Dart Sass with React because I couldn't figure out how to do that before. The documentation said to install it globally, but I didn't want to do that because I wasn't sure what kind of unexpected effects that might have. I searched through articles and video tutorials, and so many of them (even those from this year) were still using node-sass. However, eventually, I found an article that showed how to use Dart Sass with React. All that was required was this line for installation:
_npm install sass --save-dev_

There was also this scipt to add:
_"sass" : "sass src/scss:src/css --watch --no-source-map"_

Although, it seems like this isn't needed when Sass is used with React because React automatically takes care of the transpiling of Sass into CSS. However, before starting on this app, I made an regular HTML app with Sass, and for that one, I did need to run this line to create the CSS files:
_./node_modules/.bin/sass --watch src/scss:dist/css_

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/demo-sass-02-react)
1. [Website](https://sass-react-demo.netlify.app/)
1. [Sass video tutorial - Auto-refresh made easy with Parcel](https://www.youtube.com/watch?v=wYWf2m_yzBQ)
1. [Sass video tutorial - how to use @use & @forward](https://www.youtube.com/watch?v=CR-a8upNjJ0)

---

### Day 61: Thursday, September 30, 2021

**Project:** Sass Demo with React

**Tech:** Sass, React

**Today's Progress:** (1 hr) - I added a mixin, created an Image component, and adjusted the styling for a mobile first design.

**Thoughts:** The Sass features are starting to make more sense now. @extend is used to group together any number properties that can be added to any selector with a single line of code. @mixin is similar to @extend in grouping together multiple properties, but it can also accept arguments (like a function) to be used as values, which, make it more versatile than @extend; if the same @mixin is given different arguments (such as different colors) in different selectors, each selector would have a slightly different style (such as a different color). In this example. this box-shadow color could be different for every selector that uses this mixin:

<pre>
@mixin shadow($color: yellow) {
  box-shadow: 0 0 2vw 1vw $color;
  margin: 1rem;
}
</pre>

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/demo-sass-02-react)
1. [Commit #1 - add mixin](https://github.com/franco-ortega/demo-sass-02-react/commit/add32c5636959c43e5b2551a747cf91f3dae7189)
1. [Commit #1 - add Image component](https://github.com/franco-ortega/demo-sass-02-react/commit/c5e68fcb6345a8562ff4ae25076c61fcf6cb6ea9)
1. [Commit #1 - adjust styling for mobile first design](https://github.com/franco-ortega/demo-sass-02-react/commit/790cc43725bbe45b55cb82e1ff4b829fbd064392)
1. [Website](https://sass-react-demo.netlify.app/)

---

---

## 3. October

1. [August](#1-august)
1. [September](#2-september)
1. [October](#3-October)
1. [Bottom](#4-bottom)

---

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

### Day 82: Thursday, October 21 2021

**Project:** Glowing Colors

**Tech:** React, CSS

**Today's Progress:** Added open graph meta tags and meta tags for a Twitter card.

**Thoughts:** I am going to add this app to my portfolio site, so I wanted to add the meta tags to display information when I link it on Twitter and other platforms.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/glowing-colors)
1. [Pull Request](https://github.com/franco-ortega/glowing-colors/pull/16)
1. [Website](https://glowing-colors.netlify.app/)

---

### Day 83: Friday, October 22, 2021

**Project:** Student Search

**Tech:** React

**Tools:** Miro

**Today's Progress:** (2 hr) Started making a plan for a new take-home project from a a place that I applied. I used Miro to sketch out a low level wireframe of all the components. Also figured out how to munge the data that will be fetched from an API.

**Thoughts:** Looks like ten components, including one reusuable "search" component to be used in two separate parent components for different serach categories. Plus two components ("student" and "tag") that will be used to create elements for data that gets mapped.

**Link(s) to work**

No links for this project because I am not allowed to share it with the public.

---

### Day 84: Saturday, October 23, 2021

**Project:** Rest

**Tech:** Yoga, bike, boardgames.

**Today's Progress:** A day of rest. I did some food prep and yoga this morning. Then, I biked across the city in the rain to play a couple boardgames with friends (Eclipse and Mechs vs Minions).

**Thoughts:** This was my first since Day 36, so it was much deserved and felt great.

**Link(s) to work**

1. [Eclipse](https://boardgamegeek.com/boardgame/72125/eclipse)
1. [Mechs vs Minions](https://www.boardgamegeek.com/boardgame/209010/mechs-vs-minions)

---

### Day 85: Sunday, October 24, 2021

**Project:** Hide & Seek app

**Tech:** React, Sass

**Today's Progress:** I had to update a dependency (browserslist) and change the eslint file from js to json in order to make the build work on Netlify.

**Thoughts:** I noticed that the meta tags (for link previews) from a couple days prior didn't seem to be working. After checking the code and making some changes, which still didn't make the previews work, I checked the build log on Netlify and saw that it had been failing since the prior changes. Luckily, the logs told me the issue and how to fix it. First, I updated the browserslist dependency (something in the node modules). The build failed again, but there was a new message about the eslist file, and it offered a few suggestions, but changing the eslint file from a JavaScript file to a JSON file seemed like the easiest fix. The build succeeded after I made that change, and then, the link preview worked.

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/hide-and-seek)
1. [Pull Request #1 - update dependency](https://github.com/franco-ortega/hide-and-seek/pull/40)
1. [Pull Request #2 - change eslint file](https://github.com/franco-ortega/hide-and-seek/pull/41)
1. [Website](https://hide-and-seek-game.netlify.app/)

---

### Day 86: Monday, October 25, 2021

**Project:** Student Search (take-home project)

**Tech:** React

**Today's Progress:** (4 hrs) I spent an hour finishing my plan and completed the first 3 (out of 5) steps of this new take-home project. Step 1 was making a fetch request to an API, munging the data, and displaying the data on a website (that I built with React). Step 2 was to style the website to match images and videos of the website that were provided. Step 3 was to add a search bar to filter the data displayed on the site.

**Thoughts:** This was my first time using a class object for a frontend project. Usually, I use regular objects when working with React. However, in addition to needing to store properties from each piece of API data, I also needed to run logic on one of the properties of each object, so that felt like a great use case for a class method. It wound up working perfectly!

---

### Day 87: Tuesday, October 26, 2021

**Project:** Student Search (take-home project)

**Tech:** React

**Today's Progress:**

**Thoughts:**

---

### Day 88: Wednesday, October 27, 2021

**Project:** Student Search (take-home project)

**Tech:** React

**Today's Progress:**

**Thoughts:**

---

### Day 89: Thursday, October 28, 2021

**Project:** Student Search (take-home project)

**Tech:** React

**Today's Progress:**

**Thoughts:**

---

### Day ??: ?day, October ??, 2021

**Project:**

**Tech:**

**Today's Progress:**

**Thoughts:**

**Link(s) to work**

1. [Repo](https://github.com/franco-ortega/glowing-colors)
1. [Pull Request](https://github.com/franco-ortega/glowing-colors/pull/16)
1. [Website](https://glowing-colors.netlify.app/)

---

---

# 4. Bottom

1. [August](#1-august)
1. [September](#2-september)
1. [October](#3-october)
1. [Bottom](#4-bottom)
