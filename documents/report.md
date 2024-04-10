# Oblig 2, advanced CSS. IDG1293

Group 2

## Starting

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

## Report, Completing the project.

### Animations: which and why.

1. Text under headline
   - Done with CSS keyframes, because it is a p element and css is a good tool for this.
   - Wanted to animate it to make it more noticeable.
2. Moon.
   - Done with css. The moon is a css drawing, therefore doing it with css keyframes is suitable considering there is no svg
3. Star.
   - Done with animateTransform because it is a path inside an svg. The goal was to animate the large star, therefore using CSS to animate/affect the svg element/both stars is not suitable. Since they should act differently, using animateTransform allowed us to do that.
4. Car.
   - Used css keyframes. Wanted to move the whole svg element since it had been placed using absolute positioning. Css keyframes allows to modify both positioning, scale, rotateY and z-index, so its on the back-side of the moon one way, and in front the other way
5. Person on the left.
   - Moving arm, hand and mouth
     - Using path animation. chose to use it since it allows for modifying the shape/location of points. Allows to modify the path.
6. All the people
   - Making them jump up using CSS keyframes. Used css keyframes since all of them were supposed to move at the same time and could therefore use keyframes to move the parent container using absolute positioning.
7. Planet jumping:
   - Used animateTransform to move the elements on the Y-axis. Not using absolute positioning, therefor not using keyframes, moving each of the elements inside the svg so they move in a syncronized manner.
8. Particles:
   - Used both css keyframes and animateTransform and animate.
     1. Animate: Used for changing fill colors of some of the particles. Used animate instead of CSS keyframes so it can be done directly at the specific chosen elements.
     2. animateTransform: used to scale a particle. the behaviour it provided was the one we wanted to achieve, therefor we chose to do it this way.
     3. CSS keyframes. Used for transform(translateY, rotate, rotateX). Targeting the groups inside svg to affect them independently. Used CSS keyframes as it allowed to easily move the entire group.
