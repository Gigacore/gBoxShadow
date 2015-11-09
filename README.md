gBoxShadow.js
============
###### Use gravity to update CSS "box-shadow" property.

gBoxShadow.js uses gravity to alter the CSS "box-shadow" property and seamlessly updates ```offset-x``` and ```offset-y``` values based on the device motion data retrieved from accelerometer & gyroscope of the device to always position the direction of the shadow to the bottom assuming the light source is to your zenith. This adds a natural experience to the UI, especially when used with Material Design.

The plugin uses ```DeviceMotionEvent``` and ```DeviceOrientationEvent``` Web APIs to detect the moment of your device. gBoxShadow.js is built on top of [gyronorm.js](https://github.com/dorukeker/gyronorm.js) to enable consistency of data across different devices.

![Screenshot](http://i.imgur.com/U1iuGjE.gif)

######NOTE: 
This is a concept / experimental work. The idea is to re-introduce real-world entity to UI/UX in an much more interactive and intuitive way. [Four Shadows](https://github.com/Gigacore/four-shadows) is one such attempt that I tried last year, but that was time-aware and nothing to do with physical entity. It is not recommended to use with your production app, but no harm in trying as the fallback will always ensure that nothing breaks though.

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
The plugin applies the effect only to the devices that support ```DeviceMotionEvent``` and ```DeviceOrientationEvent``` Web APIs. To those that doesn't, the ```box-shadow``` property you set in the CSS will be applied.

![Screenshot](http://i.imgur.com/HAPTQhT.png)


Demos
===================
Live: http://gigacore.github.io/demos/gBoxShadow/

Video: https://youtu.be/vkKDyIstcb0

License
===================
The MIT License (MIT)

MIT © 2015 Santhosh Sundar
