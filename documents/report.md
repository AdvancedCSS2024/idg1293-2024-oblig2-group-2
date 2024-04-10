# Oblig 2, advanced CSS. IDG1293

## Starting

First we decided on a poster.

We then decided on which elements we should animate (the people having their arms move, the car moving in a wave motion, the stars shrinking and growing, the "pollution" clouds shrinking and growing again while moving up and down slightly.)

What class name we should give the different elements.

When we have done that, extract elements from the poster. Add those into the HTML as SVGs.

Implement class names.

And then style things in CSS (transfer the styling from HTML to CSS).

After that, we should make sure scalability works, then implement the animations.

## Process

1. Decide poster
2. Select elements and which animations:
   Goal-list of animations we hope to achieve below. Not all have to be achieved. Ment as guide/thoughts for what/how to animate and make sure all variations are used.

   Moon: Wobbling _(css keyframes)_, mouth moving _(SMIL transform)_

   - Decides not to move mouth

   Stars: Rotating back and forths while shrinking/growing _(css keyframes)_

   - Used svg animation instead.

   Car: Left to right _(SMIL path animation)_ in wavy motion - rotating _(CSS keyframes)_

   - Changed(car): used css keyframes instead and made it look like it was driving on its rear-wheels towards the moon, goes around the moon, then back to its start point. Makes more sense concidering the text.

   pollution:

   - Particles:
     - Shrink and grow from 0% - 100% - 0% _(css keyframes)_
     - Some rotate back and forth _(CSS keyframes)_
     - Moving upwards _(SMIL Path)_
     - Eyebrows moving _(SMIL animate)_
     - Mouths moving _(SMIL transform)_
     - changing color nuance _(SMIL animate)_

   People:

   - Waving/moving with arms _(SMIL transform)_
   - Mouth moving _(SMIL transform)_
     - added "bounce" css keyframe: so it reacts to earth jumping

   Earth:

   - Color changing - becomming sick _(SMIL animate)_
     - Decided not to do this animation
   - Eyes moving _(SMIL animate)_
     - Decided do make it "jump" instead

3. Select classnames for elements to animate
4. Download correct and simplify elements
5. Extract from PDF
6. Import SVG to html and implement classnames
7. Styling in SCSS
   - Decide units to use
8. Design poster
   - Match with original
9. Fix scalability
10. Add animations
11. Check and correct animations regarding scalability

## Classnames(options):

### Moon and moon-elements:

moon
moon\_\_eye--left
moon\_\_eye--right
moon\_\_mouth
moon\_\_left-flare--top
moon\_\_left-flare--bottom
moon\_\_right-flare--top
moon\_\_right-flare--bottom
moon\_\_crater--forehead
moon\_\_crater--left
moon\_\_crater--chin
moon\_\_crater--mid-right
moon\_\_crater--right

### Stars

star--large
star--small

### Pollution

particle-one
particle-two
particle-three
particle-four
particle-five
particle-six
particle-seven
particle-eight
particle-none
particle-ten
particle-eleven

### Car

car\_\_body
car\_\_wheel--rear
car\_\_wheel--front
car\_\_window

### People

#### Left person

left-person\_\_head
left-person\_\_eye--left
left-person\_\_flare--left-top
left-person\_\_flare--left-bottom
left-person\_\_eye--right
left-person\_\_flare--right-top
left-person\_\_flare--right-bottom
left-person\_\_arm--left
left-person\_\_arm--right
left-person\_\_hand--left
left-person\_\_phone
left-person\_\_phone--icon
left-person\_\_t-shirt
left-person\_\_shorts
left-person\_\_leg--left
left-person\_\_leg--right
left-person\_\_foot--left
left-person\_\_foot--right

#### Middle person

mid-person\_\_head
mid-person\_\_eye--left
mid-person\_\_flare--left-top
mid-person\_\_flare--left-bottom
mid-person\_\_eye--right
mid-person\_\_flare--right-top
mid-person\_\_flare--right-bottom
mid-person\_\_arm--left
mid-person\_\_arm--right
mid-person\_\_hand--right
mid-person\_\_phone
mid-person\_\_phone--icon
mid-person\_\_t-shirt
mid-person\_\_skirt
mid-person\_\_leg--left
mid-person\_\_leg--right
mid-person\_\_foot--left
mid-person\_\_foot--right

#### Right person

right-person\_\_head
right-person\_\_eye--left
right-person\_\_flare--left-top
right-person\_\_flare--left-bottom
right-person\_\_eye--right
right-person\_\_flare--right-top
right-person\_\_flare--right-bottom
right-person\_\_arm--left
right-person\_\_arm--right
right-person\_\_hand--left
right-person\_\_phone
right-person\_\_phone--icon
right-person\_\_t-shirt
right-person\_\_shorts
right-person\_\_leg--left
right-person\_\_leg--right
right-person\_\_foot--left
right-person\_\_foot--right

## Working on the project

While fixing the svg's we saw some issues and potential problems with the aproach we planned, so we had to adjust some things. Some of the classnames were changed to be more suitable. We also saw that more/other animations were relevant, so we included that in our tasks.
