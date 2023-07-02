# Scroll Driven Animations

Kilian Valkhof heeft het gehad in zijn presentaties over animations on scroll, waarbij bepaalde css animaties met keyframes, gelinked zijn aan de scroll positie van een html element, waarbij elk element kan scrollen. Als bron heeft hij bram.us meegegeven. Ik vond dit zelf een interessant onderwerp, omdat het de ux van een website kan verbeteren voor de gebruiker, door leuke maar fijne animaties te gebruiken die gelinked zijn met het scrollen. De rest zal ik in het engels schrijven, omdat de meeste bronnen in het engels zijn geschreven.

# What are scroll driven animations?

On [this website](https://scroll-driven-animations.style/) it is said that "scroll-driven animations are a common UX pattern on the web". It essentially means that on a certain scroll position there's an animation that will be going on. This also means that when you scroll down or "forward" the animation will be played "forward" and if you were to scroll up or "back-wards" then the animation will also be played back-wards. You may have heard of a parallax effects, where there are layers stacked on top of each other and each layer has it's own animation duration. Then when a user scrolls, the parallax animation will "play" and eventually transition to the next part of the page.

# What can you use to achieve this?

1. Using Javascript
   So there are different ways to implement scroll driven animations. In [this article](https://scroll-driven-animations.style/), it is said that the classis way of achieving scroll driven animations was to "respond to scroll events on the main thread". Javascript is according to [this article](https://www.keycdn.com/blog/animation-performance), always executed by the main thread. What this means is that the code that's responsible for handling these scroll events and updating the animations, is directly applied on the main thread. The issue with this is that it can cause performance issues, depending on the size of the animations you want to implement. A complex example of this could be (but doesn't have to be) a parallax effect.

2. Using CSS `will-change`

You can use `will-change` to change an element's properties. Be mindful with this, as overuse can impact the perfomance of your application. Somtimes it can help a bit with the optimization of your page, but only use this option as last resort, according to https://www.keycdn.com/blog/animation-performance.

You can use `will-change` as following:

```

/*src: https://www.keycdn.com/blog/animation-performance*/

.element {
    will-change: transform, opacity;
}

```

3. APIs and conceptsthat enable declarative scroll driven animations that work with [WAAPI](https://drafts.csswg.org/web-animations-1/) and [CSS animations API](https://drafts.csswg.org/css-animations/)

# Fixing performance issues

Like I've mentioned earlier, using a lot of javascript for complex scroll driven animations, can impact the performance of your application. To fix these issues, there are several ways you can do according to [this article](https://www.keycdn.com/blog/animation-performance):

1. Use CSS for simple animations but not for on scroll
   Instead of using only Javascript, try implementing some CSS for simple animations, such as fade-ins or fade-outs. You can essentially animate: position, scale, rotation and opacity, which is most things you will need to animate stuff anyway. Do keep in mind that you probably don't want to bind CSS animations to scroll at all, since it can drag down the performance of everything else on the screen.

2. Only use Javascript for more complex animations
   When you want more complex animations that you cannot achieve by only using CSS, only then use Javascript. A lot of Javascript can after all impact the performance of your application.

3. Use `requestAnimationFrame()`
   You can use `requestAnimationFrame()` to decide when your animation code needs to be executed. According to [this article](https://www.keycdn.com/blog/animation-performance), it uses "appropriate frame rate for the user's device, so mobile visitors will see a different frame rate than desktop". That way, the animations are run the way they're "supposed" to run even on different devices. This method also would replace `setTimeOut()` and `setInterval()`, which obviously don't have the frame rate adjustments.

4. Decouple animations from events
   Your animation code and your eventlistener should be kept seperate.

5. Keep your Javascript code concise
   If you have huge blocks of code, it can massively impact your application. Apparently you can try using web workes to tackle this issue. You can read more on web workers on [this page](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers). In shorts: "A web worker is an object that runs a named js file, which will run in the worker thread" as is said on MDN. I'm not going too much into this, because this article isn't about web workers at all.

6. Don't use jQuery
   There are newer and better options than jQuery, such as Velocity.js, which is faster and supports more features.

# Examples

On [this website](https://scroll-driven-animations.style/) you can find some more examples on scroll driven animations.

# Bronnen

- Bram.us
- https://scroll-driven-animations.style/
- https://developer.mozilla.org/en-US/docs/Glossary/Main_thread
- https://www.keycdn.com/blog/animation-performance
- https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers

Bepaalde css animaties (keyframes), linken aan de scroll positie van de html element en ieder element dat kan scrollen. Je kan bv. een cover flow maken met alleen css. Kan ook met scrollsnap. Reflectie is ook met css gedaan.

3d transform van 0 in het midden. Meer naar ene kant 0%, andere kant 100%.

Over 2/3 versies kan het in chrome zitten.

Voorbeeld bekijken: bram.us
