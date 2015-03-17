#AnimateMe.css
Modified version of animate.css by Dan Eden
Modified by Afzal Hossain

I kept the useful parts and modified some animation to make it more practical (from my POV)

##Basic Usage
1. Include the stylesheet on your document's `<head>`

  ```html
  <head>
    <link rel="stylesheet" href="animateme.min.css">
  </head>
  ```
2. Add the class `animated` to the element you want to animate.
 You may also want to include the class `infinite` for an infinite loop.

3. Additionally you can add on of the following classes to speedup or slowdown the animation

    fast    vfast   slow    qslow   vslow   vvslow  infinite

4. Also you can add on of the following classes to add some delay (delayN = N/2 sec delay)

    delay1  delay2  delay3  delay4  delay5  delay6  delay7  delay8  delay9  delay10 delay11  delay12

3. Finally you need to add one of the following classes:

  * `bounce`
  * `shake`
  * `swing`
  * `fadeIn`
  * `fadeInDown`
  * `fadeInLeft`
  * `fadeInRight`
  * `fadeInUp`
  * `fadeOut`
  * `fadeOutDown`
  * `fadeOutLeft`
  * `fadeOutRight`
  * `fadeOutUp`
  * `flipInX`
  * `flipInY`
  * `flipOutX`
  * `rotateInDownLeft`
  * `rotateInDownRight`
  * `rotateInUpLeft`
  * `zoomIn`
  * `zoomOut`
  * `zoomOutDown`
  * `zoomOutRight`

Full example:
```html
<h1 class="animated infinite bounce">Example</h1>
```

##Usage
To use animateme.css in your website, simply drop the stylesheet into your document's `<head>`, and add the class `animated` to an element, along with any of the animation names. That's it! You've got a CSS animated element. Super!

```html
<head>
  <link rel="stylesheet" href="animateme.min.css">
</head>
```

You can do a whole bunch of other stuff with animate.css when you combine it with jQuery or add your own CSS rules. Dynamically add animations using jQuery with ease:


```javascript
$('#yourElement').addClass('animated bounceOutLeft');
```

or just use

    wow.js

You can also detect when an animation ends:

<!--
Before you make changes to this file, you should know that $('#yourElement').one() is *NOT A TYPO*

http://api.jquery.com/one/
-->

```javascript
$('#yourElement').one('webkitAnimationEnd mozAnimationEnd MSAnimationEnd oanimationend animationend', doSomething);
```

[View a video tutorial](https://www.youtube.com/watch?v=CBQGl6zokMs) on how to use Animate.css with jQuery here. 

**Note:** `jQuery.one()` is used when you want to execute the event handler at most *once*. More information [here](http://api.jquery.com/one/).

You can change the duration of your animations, add a delay or change the number of times that it plays:

```css
#yourElement {
  -vendor-animation-duration: 3s;
  -vendor-animation-delay: 2s;
  -vendor-animation-iteration-count: infinite;
}
```

*Note: be sure to replace "vendor" in the CSS with the applicable vendor prefixes (webkit, moz, etc)*

## Custom Builds
Animate.css is powered by [Grunt](http://gruntjs.com), and you can create custom builds pretty easily. First of all, you’ll need Grunt and all other dependencies:

```sh
$ cd path/to/animate.css/
$ sudo npm install
```

Next, run `grunt watch` to watch for changes and compile your custom builds. For example, if you want only some of the the “attention seekers”, simply edit the `animate-config.json` file to select only the animations you want to use.

```javascript
"attention_seekers": {
  "bounce": true,
  "flash": false,
  "pulse": false,
  "shake": true,
  "swing": true,
  "tada": true,
  "wobble": true
}
```

## License
Animate.css is licensed under the MIT license. (http://opensource.org/licenses/MIT)

## Contributing
Pull requests are the way to go here. I apologise in advance for the slow action on pull requests and issues. I only have two rules for submitting a pull request: match the naming convention (camelCase, categorised [fades, bounces, etc]) and let us see a demo of submitted animations in a [pen](http://codepen.io). That last one is important.
