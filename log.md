<!-- # 100 Days Of Code - Log

### Day 0: February 30, 2016 (Example 1)
##### (delete me or comment me out)

**Today's Progress**: Fixed CSS, worked on canvas functionality for the app.

**Thoughts:** I really struggled with CSS, but, overall, I feel like I am slowly getting better at it. Canvas is still new for me, but I managed to figure out some basic functionality.

**Link to work:** [Calculator App](http://www.example.com)

### Day 0: February 30, 2016 (Example 2)
##### (delete me or comment me out)

**Today's Progress**: Fixed CSS, worked on canvas functionality for the app.

**Thoughts**: I really struggled with CSS, but, overall, I feel like I am slowly getting better at it. Canvas is still new for me, but I managed to figure out some basic functionality.

**Link(s) to work**: [Calculator App](http://www.example.com)


### Day 1: June 27, Monday

**Today's Progress**: I've gone through many exercises on FreeCodeCamp.

**Thoughts** I've recently started coding, and it's a great feeling when I finally solve an algorithm challenge after a lot of attempts and hours spent.

**Link(s) to work**
1. [Find the Longest Word in a String](https://www.freecodecamp.com/challenges/find-the-longest-word-in-a-string)
2. [Title Case a Sentence](https://www.freecodecamp.com/challenges/title-case-a-sentence) -->


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
2. [Pull Request #2 - context update](https://github.com/franco-ortega/hide-and-seek/commit/ace4883d4cc1cf2265b02457eed27eb49801e1f8)
2. [Pull Request #3 - refactor useEffects](https://github.com/franco-ortega/hide-and-seek/commit/f8b9dd1d1faea56486a3ae7118c29aa3c450de84)
3. [Website](https://hide-and-seek-game.netlify.app/)


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


### Day 25: Wedsday, August 25, 2021

**Project:** Glowing Colors

**Tech:** React, CSS

**Today's Progress:** (1 hr) The height and width of the orbs are now created dynamically and randomly each time an orb is rendered, so every orb is a different size. Also, I added tests for some of the functions from yesterday's refactor.

**Thoughts:** The dynamic styling is being added each Orb component via inline styling as it is created. I wasn't sure how to input the height and width in this manner while also maintaining a responsive design. The orbs had a height/width of 75px on mobile and 100px on larger screens. The dynamic height/width has a range between 0px and 200px, but I didn't want the orbs to get that big on mobile screens. Luckily, I was able to utilize the the max-height and max-width properties, which I only recently got more familiar with, in the CSS module for the Orb component, and that successfully capped the height/width of the orbs on mobile.

**Link(s) to work**
1. [Repo](https://github.com/franco-ortega/glowing-colors)
2. [Pull Request](https://github.com/franco-ortega/glowing-colors/commit/0965f0484c0cd02ca7445da3a144a2714aaabaa3)
3. [Glowing Colors Website](https://glowing-colors.netlify.app/)
