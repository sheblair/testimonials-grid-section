
# Frontend Mentor - Testimonials grid section solution

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-Nnw6J7Un7). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#usefulresources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot

![](/images/testimonials-grid-section-screenshot.png)

### Links

- [Solution](https://www.frontendmentor.io/solutions/testimonials-grid-using-html-and-css-zfkbxKe7kD)
- [Live Site](https://sheblair.github.io/testimonials-grid-section/)

## My process
*PART ONE*
1. The first time I tried to build this, I hadn't yet been introduced to CSS Grid, and it was actually through doing this challenge that I taught myself how to use CSS Grid.
2. Because when I started I only knew Flexbox, that's what I tried first. I soon realized that the layout couldn't be achieved (or at least not very easily or elegantly) with Flexbox, so I looked into Grid and started trying to figure out how to make it work. 
3. I looked at other people's solutions using Grid and tried to work backwards from what they had done. I looked up a bunch of static information about Grid and Googled things and got really overwhelmed and stuck.
4. I took a couple of days off from the whole thing, then came back. I watched a short tutorial on egghead.io, read through the CSS grid explanation on css-tricks.com for the 10th or 15th time, and started over again.
5. This time, something was clicking, and I was able to figure out how to get the appropriate columns and how to reposition my grid items according to the design mockup.
6. I got stuck again because there was all this extra white space between and I couldn't figure out where it was coming from (it wasn't the grid gap). I spent a long time on Stack Overflow and Google trying to figure this out.
7. I finally had my eureka/facepalm moment when I realized that in my mobile CSS, the width of the grid items was set to 87%. I changed this to 100% and voila, the grid items slid nicely into place--no more extra white space!

*PART TWO*
1. So I thought I had my layout all setup but then I realized there was an odd space between my first and second testimonial blocks that was causing a shift in the layout. It took me **ages** to figure out what was causing this, because I assumed it had something to do with how I'd set up my grid initially. I confirmed, by looking at a few other solution codes, that in fact my grid was set up properly. So then it just became a task of scanning through my CSS, line by line, trying to figure out what innocent-seeming thing was causing this weird break in the layout. It ended up being a width property set to 90% on my class for styling all my testimonial blocks. I had the width set to 90%, probably way back from when I started the project using Flexbox instead of grid, and once I unchecked the box in DevTools the layout break disappeared! Hallelujah.
2. Then decided to create an appropriate layout for my tablet styles, because even though that's not part of the challenge description, it bothers me to build a responsive site that doesn't have a nice and unique layout for tablet screen sizes.
    - After building a nice tablet layout, I realized that now my tablet styles were breaking my desktop layout, so I went into the desktop styles and added some more CSS to fix those issues. 
    - And with that, my project was finally complete!!!
    - Oh - I also added a box-shadow to the testimonials, which made it look more like the design, and I also added a top margin on the desktop layout so that it wouldn't sit flush to the top of the screen, because I think it looks nicer that way. On phone and tablet sizes, I don't mind the content aligning flush with the top, but for some reason it doesn't work on desktop. And that's it!

*PART THREE*
1. That was, in fact, not it. Returning to the project weeks later, I realized that some of the margins and padding seemed wonky. I used the universal selector to zero-out the browser defaults (this was a trick I had learned in meantime). This cleaned things up a bit.
2. There was also this weird thing happening with the text on one of the sections--it wasn't filling the height of the container, so there was this awkward extra space above and below. It took me ages to figure this out. I did a lot of tweaks to fix this, so here they are: 
    - Removed Flexbox from the entire card and instead applied it more selectively to create flex containers within the testimonial card. 
    - Changed the size of my rows to percentages instead of fractional units
    - Something in my tablet styles was creating extra unnecessary columns in my grid. I removed tablet styles (RIP but also they weren't part of the challenge technically so I figured I should focus on MVP and think about tablet later).
    - I decreased the width of the entire layout to 75%
    - More adjustments to margins and padding.
    - Adjusted the width of the pull quote only in one section. This fixed a spacing issue
3. All of these things together solved the issue and the layout looked great. Unfortunately, I lost my tablet styles, and I also suspect there are more elegant/simple ways to solve this problem. But I am still proud of myself for making it work, and I hope to get even better at identifying simpler and more elegant solutions as I continue to learn. 

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

This was truly a huge challenge for me. I had to stop and take a time off here and there before I was finally able to finish it, mostly because I had actually never used CSS Grid before trying this challenge, so it took a lot of error and experimentation to figure out how to use it. I learned a lot about how Grid works, including how powerful it is, and that you are able to position things pretty much wherever you want, which is an incredible thing to be able to do. I think I learned that Grid has much more flexibility than Flexbox and other CSS layouts I've been working with, so that was cool.

The other main thing I learned, and this is definitely not the first time I've encountered this nor will it be the last, that some seemingly innocuous line of code can end up causing a kind of major issue. In this case, it was a width property that was causing my whole layout to break. I never would have guessed that this would be the cause of the issue. What this teaches me is to think outside the box when facing a mysterious issue--don't assume anything, let yourself scan through all the code and remember that it can be a very small thing, so just try everything. Use DevTools and just click on and off whatever you can think of, and eventually you'll find it.

A couple other important things that  I learned or were reinforced by this challenge are:
1. Use the universal selector to zero-out browser defaults
2. Margins can affect layout and spacing in ways that padding won't, so be careful what you use where

### Continued development

I definitely want to keep working with and experimenting with CSS Grid. It was difficult at first but once I started feeling more confident and getting the hang of it, I realized how useful and powerful it is and how great a tool it really is. 

I also need to keep practicing using margins vs. padding, measuring column and row size, and I still want to figure out how to add in tablet styles that won't break my desktop layout.

### Useful resources

- [CSS Tricks - A Complete Guide to CSS Grid](https://css-tricks.com/snippets/css/complete-guide-grid/) - This helped me figure out how to use CSS Grid. It was instrumental for covering the basics and I kept returning to it -- a well organized and designed resource.
- [Create a Card Layout with CSS Grid](https://egghead.io/lessons/css-create-a-card-layout-with-css-grid) - This is a short but really helpful tutorial on egghead.io from instructor Ali Spittel that really helped me figure out how to work with Grid and create a responsive layout.

## Author

- Website - [Sheila Blair](https://github.com/sheblair)
- Frontend Mentor - [@sheblair](https://www.frontendmentor.io/profile/sheblair)

