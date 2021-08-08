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

### Day 8: Saturday, August 8, 2021

**Project:** Server-03

**Tech:** Node, Express, PostgreSQL

**Today's Progress:** (1 hr) I added two GET routes (get all, get by id), one PUT route, and one DELETE route for the tiles table along with their correspondings methods and tests.

**Thoughts:** Everything went rather smoothly. I was able to write most of the code from memory, and debugging the mistakes went relatively quickly. Also, before I was re-creating the table before each test, but now the table is created only once before any tests are run, so the tests work off each other. That could get somewhat risky with a bigger batch of tests, but it seems very manageable with only five tests.

**Link(s) to work**
1. [Repo](https://github.com/franco-ortega/demo-server-03-joins)
2. [Pull Request #1](https://github.com/franco-ortega/demo-server-03-joins/commit/644d8d08d3a8b0f1db612da95bfc4cef52e76b45)
3. [Pull Request #1](https://github.com/franco-ortega/demo-server-03-joins/commit/ce90443a9bda11d119c23f88f6d7038db0ee444a)