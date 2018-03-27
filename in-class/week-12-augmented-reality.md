## March 28th: Augmented Reality

### Introduction

Augmented reality (AR) has become an increasingly popular technology: overlaying  digital media (images, video, text, sound, etc.) onto "real-world" objects and locations, most often experienced by looking through the camera lens a smartphone, tablet, or other electronic device. AR's "moment" arguably came in the summer of 2016:

![Pokemon Go](https://upload.wikimedia.org/wikipedia/en/9/90/Pok%C3%A9mon_Go_AR_Mode%2C_Dec_2017.png)

*Source: [Wikipedia](https://en.wikipedia.org/wiki/File:Pok%C3%A9mon_Go_AR_Mode,_Dec_2017.png)*

Augmented reality brings up a host of fascinating questions for how societies create space and experience place. Today, we're going to be creating our own (very basic) augmented reality experiences to get us thinking about this technology, its creation, and its implications for the humanities and social sciences.

### Getting Familiar with the Technology

The current standard for augmented reality is the Unity game development platform. It also has a steep learning curve and requires a fair bit of installation steps on your computer. Instead, we're going to be using a much lighter-weight application called [HP Reveal](https://studio.hpreveal.com/landing) (formerly Aurasma). This has very limited options in terms of customizing the AR experience, but it is useful for getting our feet wet. If you are interested in learning how to use Unity, I would suggest Jacob Greene's tutorial at [Programming Historian](https://programminghistorian.org/lessons/intro-to-augmented-reality-with-unity).

First, if you have not already done so please [sign up for an account with HP Reveal](https://studio.hpreveal.com/landing) and then download the accompanying mobile app on your phone. Although you can technically create new AR content in this mobile app, it's best to use the web browser version of HP Reveal ("Studio") to create content and the mobile app to experience it. 

It's helpful to think of two different AR components: `triggers` and `overlays`. A `trigger` is some kind of marker that, when a user sees it through their camera will "trigger" new content to get overlaid on top of the trigger. This content is the `overlay`. A real-world example might be: a historical marker on the side of a highway is a `trigger`. When a user looks through their camera using the app, it will recognize the historical marker as a `trigger` and then overlay a historical image onto it as the `overlay`:

![Programming Historian](https://programminghistorian.org/images/intro-to-augmented-reality-with-unity/new-ar-dev-1.png)
*Source: Jacob Greene, ["Introduction to Mobile Augmented Reality Development in Unity"](https://programminghistorian.org/lessons/intro-to-augmented-reality-with-unity) Programming Historian. Based on an original photograph by Nicholas Henderson.*

### Create your first AR experience

To create your first AR experience, we're all going to use a common `trigger`: our old friend Yi-Fu Tuan's book *Space and Place: The Perspective of Experience*:

![Yi-Fu Tuan](https://images-na.ssl-images-amazon.com/images/I/419QSeiwcJL._SX324_BO1,204,203,200_.jpg) 

*Source: [Amazon](https://www.amazon.com/Space-Place-Perspective-Yi-Fu-Tuan/dp/0816638772)*

Log in to your HP Reveal account in a browser and click `Create new aura`. Upload a trigger image (in this case, the JPG of Tuan's book cover). Once you have the trigger image, you'll need to add the `overlay`, or what will appear on top of the book cover on your user's mobile screen. For the `overlay`, find an image that you think in some way embodies or relates to Tuan's theory of place and upload it to your trigger image.

Now open up the mobile app and see if you can get your AR experience to load. Does the image appear when you point your camera at the real-world cover of Tuan's *Space and Place*?

### Build an AR "Exhibit"

Museums are increasingly turning to AR to engage with visitors. We're going to create an AR experience for our own museum "exhibit": the History Department in Meserve Hall. We're going to pretend that each faculty member's office door is a different museum item. Build an AR experience using at least three `triggers`. Try and experiment with different kinds of overlays. Once everyone has a working "exhibit", follow one other person's account using your HP Reveal mobile app and go through their "exhibit." As you do so, think about: 

- What worked? How does this add to the experience of the "exhibit"?
- What didn't work? Does any of this detract from the experience?
- How does AR fit with some of the theories of space and place that we've read about during this semester?
