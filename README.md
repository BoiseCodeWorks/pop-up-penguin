## Step 1: Div'ing up

---
Let’s start building our game. We’ll be adding a set of divs to our HTML and matching styles in our CSS.

Open the HTML tab and delete everything between the `<body>` tags.
Add the following code:
```html
<div id="gameholder">
		<div id="title"></div>
		<div class="mole1"></div>
		<div class="mole2"></div>
		<div class="mole3"></div>
		<div class="mole4"></div>
		<div class="mole5"></div>
		<div class="mole6"></div>
		<div class="mole7"></div>
		<div class="mole8"></div>
		<div class="badger"></div>
</div>
```
What this code is doing:

These divs are defining the structure for our game. Each “mole” div will be a little bump of dirt hiding a mole (or badger). We will be adding the images to them in the CSS.

Next, go to the CSS tab.
Go ahead and erase the code that’s already there.
Add the following code to the CSS tab:
```css
body {
    background-color: #996633;
}
#gameholder {
    width: 600px;
    margin-left: auto;
    margin-right: auto;
}
#title {
    width: 600px;
    height: 150px;
    background-image:url('');
}
```
What this code is doing:

body is making our background a nice brown color.

`#gameholder` is making our gameholder div 600px wide and centering it in the screen. It’s invisible, but helps us organize our other elements.

`#title` is setting a size for our our title div and giving that div a background image. In this case that image happens to be the title/instructions to our game. We’ll add that in the next step.

Let’s add some little dirt-covered mounds for our moles!

Add the following class to the CSS tab:
```css
.mole1 {
    width: 200px;
    height: 200px;
    float: left;
    background-image:url('');
}
```
Find an image of a dirt covered mound on the internet, then put your cursor between the (' ') at the end of the background image property and click “paste to code”
All of our CSS looks like this so far:
```css
body {
    background-color: #996633;
}
#gameholder {
    width: 600px;
    margin-left: auto;
    margin-right: auto;
}
#title {
    width: 600px;
    height: 150px;
    background-image:url('');
}
.mole1 {
    width: 200px;
    height: 200px;
    float: left;
    background-image:url('');
}
```
To finish this step:

Copy the `.mole1` class and use it to make styles for `.mole2` through `.mole8`. Make a `.badger` class as well.

## Step 2: Rolling over

---
Now let’s add a rollover or `:hover` effect to each one of our mounds. Find an image of another mound, possibly an uncovered one and we'll use that to add intrigue and suspense to our game.

In the CSS tab find our `.mole1` class.
Make a new line above the class and add the following style:
```css
.mole1:hover {
    background-image:url('');
    cursor: pointer;
}
```
This style is what’s called a pseudo-class. It’s a way to add effects and additional styles to elements that we’ve already created. In this case we will be changing the background image of that div when a mouse is over it. We will also be changing the cursor to a pointer, or little hand giving our users another clue that the mound is clickable.

Paste the image link inside the quotes ('') of the background-image property.
Go to the preview mode and run your mouse over the first mound. Did the image change? That’s `:hover` doing its job.
To finish this step:

Make new `:hover` classes for each of our `.mole` and `.badger` classes. You can find the images in our media folder.

## Step 4: Pop up the moles!

---
Now that we’ve got our mounds tempting us, let’s hide some moles (and a badger!) inside each one and use another pseudo-class to make them pop up when clicked.

In the CSS tab find the `.mole1:hover` class.
Underneath, that class add the following class:
```css
.mole1:active {
    background-image:url('');
}
```
`:active` is another type of pseudo-class. Similar `:hover` it adds/changes the style of `.mole1` when the div is clicked with the mouse.

The position in the code of pseudo-classes is important. An `:active` class should always come after or underneath `:hover` in the code for the effect to work properly.

Find an image of a mole and paste the code for the image inbetween the (‘’)
Go back to the preview and click the first mound. Did the mole pop up? Hold your mouse button down to keep the mole from popping back down.
To finish this step:

Make new `:active` classes for each of our `.mole` and `.badger` classes. Add mole images from the media tab. Make sure you hide the badger somewhere too.

## Step 5: Oh no a badger!

---
We’ve got all our moles and badger in place. Let’s add a badger alert that will pop up when the badger is clicked!

Go to the JS tab.
On the line below “//This code will run after your page loads” add a handler for the "mousedown" event to the .badger div. It will look like this:
```javascript
$(document).ready( function() {
    //This code will run after your page loads
    $(".badger").mousedown(function() {
        alert("Oh no!");
    });
});
```
This is a little bit of Javascript and jQuery that will pop up a browser alert with the text “Oh no!” when you press your mouse button on the badger. Try it out in the preview mode. To learn more about Javascript continue working through the projects.

## Step 6: Challenge accepted!

---
Now that we’ve got all our moles (and badger) hidden let’s play the game! Find a friend or a family member and challenge them to find all the moles without accidently clicking on the badger.

After they’ve had a go, mix the classes up in your HTML to reshuffle the mounds and let them try again. To make it extra challenging, change the images in the `:active` states to put different moles (and your badger) under different mounds.

To finish this step:

Teach your playing partner how to change the images in the `:active` states and trade off challenging each other to a game of “Find the moles.”
