gBoxShadow.js
============
###### Enable gravity to your "box-shadow" CSS property.

gBoxShadow.js induces gravity to the CSS "box-shadow" property and seemlessly changes the direction based on the device motion data retrived from accelerometer and gyroscope. This adds a natural experience to the UI, especially when used with Material Design.

The plugin uses ```DeviceMotionEvent``` and ```DeviceOrientationEvent``` Web APIs to detect the moment of your device. gBoxShadow.js is built on top of [gyronorm.js](https://github.com/dorukeker/gyronorm.js) to enable consistency of data across different devices.

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
	.btn {
		box-shadow: 10px 10px 15px #A01818;
	}
```

######4. Ensure to define the same color and blur values in your HTML using ```data-shadow-color``` and ```data-shadow-blur```:

```HTML
	<div class="g-enabled btn" data-shadow-color="#A01818" data-shadow-blur="15">I am a button</div>
```

Fallback for unsupported devices
===================
The plugin applies the effect only to the devices that support ```DeviceMotionEvent``` and ```DeviceOrientationEvent``` Web APIs. To those that doesn't, it picks the ```box-shadow``` property from the CSS file that you added.

![Screenshot](http://i.imgur.com/HAPTQhT.png)


Demo
===================
http://gigacore.github.io/demos/gBoxShadow/

License
===================
The MIT License (MIT)

MIT © 2015 Santhosh Sundar