# [SDF05] CSS Magic Buttons

## Project Brief

Get ready to create animated buttons using CSS! This project focuses on creating three unique animated buttons using CSS. With this challenge, you'll dive into the world of CSS animations, transitions, and interactivity.


## Design Choices

1. **Button 1 - Ripple and Pulse**
    - Discovered the _radial-gradient_ function and chose to simulate a water drop ripple.
    - On hover, the user "disturbs" the button and a "ripple" is triggered.
    - When activated (clicked) and held down, a smaller version of the same effect takes place simulating a "pulse".
    - Both effects work in tandem: when a click is released the hover effect triggers again.
2. **Button 2 - Pointing Arrow**
    - An "ADHD" button that simulates urgency.
    - On hover, the button starts "urging" the user into the right hand direction.
    - On hover, a double arrow appears pointing the user into the right hand direction.
    - On click, the arrow "sprints" to right hand side indicating the user's desire to GO!
3. **Button 3 - Danger Door**
    - A button with serious consequences.
    - Hidden behind a "safety door". The user cannot activate the button while the "door" is closed.
    - On hover, the "door" will slowly start to open, revealing the button inside. Only now may the user access the button.
    - On click, the button disappears briefly and flashes across the screen, indicating the seriousness of the action.

## Challenges

**Button 1:** Understanding the transformations of the _radial-gradient_ function. Took a while before I found the correct settings to simulate a waterdrop. It has some room for improvement still - there is a pixelated sharpness to the ripples that I struggle to get rid of.

**Button 2:** Originally wanted to create a "cat and mouse hunt" button, where on hover a little mouse (emoji) would "peek" its head from behind, and on click, would "release" cats (emojis) starting a "chase" within the button's parent div. Discovered that CSS animations can only be applied to and affects only the specified element: you can only change the elements' CSS properties you trigger (no JS allowed for this project). Granted, it may still be possible to implement this original idea, but would involve some serious "acrobatics" with nested elements. Simply do not have the time. Pivoted to something simpler but still challenging: this button uses transitions and animations, and makes good use of the _::after_ pseudo-element.

**Button 3:** Simpler than it seems. The parent div simply widens on hover, and the 2 last child elements (the "doors") are anchored on either side. The mix of absolute and relative positioning was crucial for this one, as the button had to stay in place while the images moved out of the way. Initially thought I had to fiddle with z-indexes, but HTML ordering (and stacking) proved sufficient to complete the design.

**Git:** To improve upon my git skills, I decided to develop each button in its own branch concurrently, and merge the final products back into the main branch. A ton of fun. Learned quite a lot. Had to deal with merge conflicts each time, and even had to rebase the original main, as the remote origin url was changed and its main branch updated since I started working on the project. Now comfortable with commands such as _reset --hard_, _pull --rebase_, _remote_, _commit --amend_ and _merge_. Granted, the main tree might not be squeaky clean, but nothing's lost or broken! Made a habit of backing up the repo before running serious commands.

## Inspirations
**Button 1:** Curiosity about CSS3 functions and SDF04's checkered background.

**Button 2:** https://www.w3schools.com/css/css3_buttons.asp . And no, I did not just copy code verbatim. I took the time to go through every property to understand it, commenting along the way, adjusting to my use case and removing the redundant pieces.

**Button 3:** Red Alert, the video game. Always wanted to have a nuke button.
