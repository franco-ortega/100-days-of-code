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