---
title: FontFace
readiness: 'Ready to Use'
summary: 'An introduction to the JavaScript FontFace object and font loading. Part of the  Typography tutorials section.'
tags:
  - Tutorials
uri: tutorials/typography/fontface

---
**By Dave Gash**
Originally published 15 May 2014

## Summary

An introduction to the JavaScript FontFace object and font loading. Part of the Typography tutorials section.

## Introduction

The FontFace object is conceptually based on the CSS @font-face property, a powerful and flexible feature that allows you to use custom fonts in your web pages. If you aren't familiar with @font-face, please read Paul Irish's excellent [@font-face tutorial](/tutorials/typography/font-face) first and then come back. It's okay, we'll wait.

While @font-face works fine for pre-coded pages, many developers would also like to use custom fonts on the fly via scripting. This has historically been difficult to accomplish, but has now become much more straightforward with the introduction of the Javascript **FontFace** object.

At its core, FontFace is a new interface used for dynamically accessing font resources through scripting. With FontFace, you can load, add, and use custom fonts at any time by manipulating the object in script.

**Note:** As of this writing the FontFace object is only available in Google Chrome Canary, which you can get [here](https://www.google.com/intl/en/chrome/browser/canary.html).

## Background

Interestingly, a manually created CSS @font-face rule implicitly defines a Javascript FontFace object, with its properties set to the same values as the @font-face rule's. The FontFace object is said to be "CSS-connected". Thus, you can manipulate a manual @font-face with script, but that isn't exactly what we're after.

Of course, you can also create any document element, such as a @font-face rule, with script and "shoehorn" it into the page's stylesheet using the **.insertRule()** method, but that's also not the goal here.

While your script can certainly interact with manual @font-face rules, or create and manipulate CSS rules directly, in this tutorial we'll be focusing on independently creating and using FontFace objects.

## Preparing the Fonts

Before we can begin using a custom font, we have to *have* a custom font. As covered in the [@font-face tutorial](/tutorials/typography/font-face), in order to ensure cross-browser compatibility you should have these versions of your font available:

-   Embedded Open Type (.eot), specifically for Internet Explorer
-   True Type Font (.ttf), for Safari, Opera, Firefox, and Chrome
-   Web Open Font Format (.woff), for Firefox, Chrome, Opera, and IE9
-   Scalable Vector Graphics (.svg), for iPhones, iPads, and other devices that run Mobile Safari

The easiest way to convert an existing font in any of these formats to all the others is with the amazing [Font Squirrel](http://www.fontsquirrel.com/tools/webfont-generator) webfonts generator. Font Squirrel is a free online tool that uploads your original font, creates the required variants, and zips it up into a convenient downloadable package.

Naturally, the font variants must all be available on the server to the pages that use them, either in the same folder or in a defined path. And -- this should go without saying, but let's say it anyway -- you **must** be sure that the font you want to use is licensed for web use. For this article we're using an absolutely free and web-licensed font called [FingerPaint](http://www.fontsquirrel.com/fonts/finger-paint), available (along with many others) at Font Squirrel. Finger Paint is a fun, decorative font; here's how it looks.

![fingerpaintfont1.png](/assets/public/a/af/fingerpaintfont1.png)

## Creating the FontFace Object

This is pretty straightforward; you create a FontFace with the JavaScript **new** keyword as you would any other object.

    var f = new FontFace("fingerpaint", "url(fingerpaint-regular-webfont.ttf)", {});

The first parameter is the user-defined name. Call it whatever you like, but use common sense; later, you'll need to refer to the font by that name.

The second parameter is the URL of the font file. As you can see, we're using the True Type version for this example.

The third parameter is the attribute list, such as *family*, *style*, *weight*, etc. As these values are optional, just include the empty braces and don't worry about it for now.

That defines the JavaScript FontFace object and requests that the browser locate the font file and associate it with the object. But the page doesn't know it's there yet.

## Adding the Font to the Page

The next step is to add the FontFace to the document; a font cannot be used until it exists in the document's **FontFaceSet** object. The FontFaceSet is implicitly referenced through the document's **fonts** property. It would seem, then, that we could just use the **add()** method to include the font in the page. That is, this

    var f = new FontFace("fingerpaint", "url(fingerpaint-regular-webfont.ttf)", {});
    document.fonts.add(f);

should add the FontFace to the page's font list. And it would, *if the font were actually loaded* -- but it isn't. Before we can add the font to the document, we must explictly force it to be loaded with (what else?) the **load()** method.

Interestingly, the load process raises an issue. We have to be sure that the font is done loading before trying to add it to the document, but in an async world, that can be a tricky business. However, we can use an innovative method to wait for the load to finish by combining the load call with the (also new) JavaScript **Promise** feature. If you want to read up on promises, see [this HTML5Rocks article](http://www.html5rocks.com/en/tutorials/es6/promises/). But briefly, a JavaScript promise is a pattern for handling asynchronous operations. It operates a bit like an event listener, and lets you call a **then()** method that contains a callback function to be executed only when the calling method is complete ("the promise is fulfilled"). So this

    var f = new FontFace("fingerpaint", "url(fingerpaint-regular-webfont.ttf)", {});
    f.load().then(function (loadedFace) {
      //statements
    });

will invoke the load, wait for it to complete, and only execute the then() method's anonymous function when the load is done.

Now, what should the function do? At the very least, it should add the now loaded font to the FontFaceSet via the fonts list (as we tried to do earlier), like this.

    var f = new FontFace("fingerpaint", "url(fingerpaint-regular-webfont.ttf)", {});
    f.load().then(function (loadedFace) {
      document.fonts.add(loadedFace);
    });

So far, so good. The font is identified, loaded, and added, but we still haven't actually seen it anywhere on the page. That is, we've made the font available to the page, but haven't used it yet.

## Using the FontFace

For the examples in this section, we'll use this simple bit of HTML, with a mix of unclassed and class="fp" elements.

    <h2>This is an H2.</h2>
    <p>This is a regular paragraph.</p>
    <p class="fp">This is a class="fp" paragraph.</p>
    <h2 class="fp">This is a class="fp" H2.</h2>
    <p>This is another regular paragraph.</p>
    <p class="fp">This is another class="fp" paragraph.</p>

There are any number of ways to assign the font to one or more HTML elements, and any number of places to put the assignment in the page. Perhaps the most straightforward location is within the anonymous function itself; that's a good idea because it keeps all the font usage code localized. All the action is in one place, so that when the FontFace load is complete, the font is added to the document.fonts property and then immediately applied to the desired elements. For example, this

    var f = new FontFace("fingerpaint", "url(fingerpaint-regular-webfont.ttf)", {});
    f.load().then(function (loadedFace) {
      document.fonts.add(loadedFace);
      document.body.style.fontFamily = "fingerpaint, serif";
    });

sets the entire document body to the new font, and falls back to *serif* if there's a problem. (As with any font assignment, always include one or more fallbacks.) Here's the output.

![fingerpaintfont2.png](/assets/public/e/e4/fingerpaintfont2.png)

Okay, that's a pretty broad application, especially for a whimsical font like Finger Paint. It would make more sense to only apply the font to a specific set of tags, such as just those with a class of "fp". So this

    var f = new FontFace("fingerpaint", "url(fingerpaint-regular-webfont.ttf)", {});
    f.load().then(function (loadedFace) {
      document.fonts.add(loadedFace);
      var fptags = document.getElementsByClassName("fp");
      for (var i = 0; i < fptags.length; i++) {
        fptags[i].style.fontFamily = "fingerpaint, serif";
      }
    });

would do the trick, selecting all tags with the class of "fp" and looping through them to apply the Finger Paint font to each. That output looks like this.

![fingerpaintfont3.png](/assets/public/3/3f/fingerpaintfont3.png)

Or, if you'd rather not rely on pre-assigned classes, you might opt to display all the H2s in the document in Finger Paint. If so, this

    var f = new FontFace("fingerpaint", "url(fingerpaint-regular-webfont.ttf)", {});
    f.load().then(function (loadedFace) {
      document.fonts.add(loadedFace);
      var h2s = document.getElementsByTagName("h2");
      for (var i = 0; i < h2s.length; i++) {
        h2s[i].style.fontFamily = "fingerpaint, serif";
      }
    });

is what you need, selecting all H2 elements regardless of class and applying the font to them. That produces this output.

![fingerpaintfont4.png](/assets/public/d/d3/fingerpaintfont4.png)

Again, applying the font in the same place, code-wise, where it is identified, loaded, and added keeps the font code together and aids in debugging and maintenance.

## Conclusion

Although the CSS @font-face rule has been around for a long time and is the go-to guy for pre-written pages using custom web fonts, it doesn't satisfy the scripter's need to identify, load, and use custom fonts dynamically. The JavaScript FontFace object does just that, cleanly and without hassle.

Now it's your turn. Have a go!

