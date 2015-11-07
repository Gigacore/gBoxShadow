gBoxShadow.js
============
###### Enable gravity to your "box-shadow" CSS property.

gBoxShadow.js induces gravity to the CSS "box-shadow" property and seemlessly changes the direction based on the device motion and orientation. This adds a natural experience to the UI especially when used with Material Design.

![Screenshot](http://i.imgur.com/U1iuGjE.gif)


Setup
============

######1. Include jQuery and ```gBoxShadow.js``` into your html file.

######2. Add the class ```g-enabled``` to the element 

```HTML
	<div class="g-enabled btn">I am a button</div>
```

######3. Apply ```box-shadow``` styling of your choice to the element in your CSS:

```CSS
	box-shadow: 10px 10px 15px #A01818;
```

######4. Ensure to define the same color and blur values to your HTML element using ```data-shadow-color``` and ```data-shadow-blur```:

```HTML
	<div class="g-enabled btn" data-shadow-color="#A01818" data-shadow-blur="15">I am a button</div>
```

License
===================
The MIT License (MIT)
