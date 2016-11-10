# Making demos: a quite possibly incomplete guide

The general rule: **demos should be short and self-explanatory.**

If your screenshot/video/gif needs an explanation, either the feature is not obvious or the demo needs work.

Save people's time. Get straight to the point!

## Script for a demo

The best way to save other people's time is to put in plenty of yours writing a script for your demo.

You don't need to get over-the-top creative. Write a script that answers these questions:

1. What is the name of the new feature and its purpose?
2. How to access it?
3. What is the outcome of using the feature? (and where appropriate: how do settings affect the output of the feature?)

For example, the answers for demoing a hypothetical 'tool that takes screenshots' could be:

1. Screenshot tool, to capture screenshots of the current website.
2. Enable tool in settings. Then click on the icon that represents a camera to capture the current website.
3. A capture of the contents of the current tab is captured and downloaded to the user's computer. The image file is placed on the user's `Downloads` folder (or equivalent).

Now that you've thought of this rough script, try to go through the demo steps yourself, to make sure you're not overlooking any step. They might seem obvious to you as developer of the tool, but users cannot read your brain.

Some features can be illustrated with a screenshot. Others, specially if they involve things that happen in a series of steps, tend to be better illustrated with a video. This depends on each case. At the bare minimum, try to provide a screenshot.

## General rules

If you desktop is going to be shown in the demo, make sure you remove all the clutter from it, and possibly also change to a plain, neutral colour for the background.

When capturing images, try as much as possible to show only the bits of the browser that are relevant to the feature. We normally don't need to see the contents of your desktop, or the names of your bookmarks, or any possible browser extension you might have installed. All these are distracting away from the feature you want to talk about.

Set up a new browser profile for demos. This makes it harder to 'leak' your previous history in the URL bar, and ensures that your environment is closer to what a generic user will find. Note any step to activate the feature that you might have forgotten when writing the demo script: `about:config` changes, enabling panels in the devtools settings area, etc.

When you create a new browser profile, you get a 'default' look and feel and you might also get all sorts of doorhanger bars. There's a chance they can ruin your demo recording, so be prepared to dismiss them and re-capture the demo again.

A safe url to use for demos is [mozilla.org](https://mozilla.org).

It's also often good to resize the browser so it is smaller than you would normally use. If you can make it fit in an image and the text is still readable, the better. Big browser windows have lots of space between corners that don't add anything to the demo, and the text in the browser chrome is unreadable when the images are scaled down (e.g. when displayed in contexts such as twitter).

Also, smaller assets use less space in disk, and for videos it makes it easier to be under the maximum threshold for sharing in social media.

Let's look at some examples:

### Bad: window is too big

![too big](./assets/demo-too-big.png)

The browser chrome here is barely visible when displayed within the context of this document.

### Bad: window is too small, doesn't show the URL

![URL is cut out](./assets/demo-bad-no-url.png)

The browser chrome is visible now! We can read the elements in the screenshot.

But if this was a demo about a website, it would be a failure because we don't know what we're looking at: the URL is cut out. There is a sense of missing out.

### Moderately bad: the content in the page is cut out

![URL is cut out](./assets/demo-bad-cuts-text-out.png)

This is better, we can read the full URL so we know what we're looking about. But the text in the website is cut half-way. This looks bad and is distracting from the demo.

### Good

![URL is cut out](./assets/demo-good.png)

This would be a good demonstration screenshot for the website. We can read the browser chrome elements, the full URL is displayed, and the text in the website is not cut out.

It looks balanced and complete, and users can focus on the website instead of being distracted.

## Taking screenshots

Taking a screenshot depends on the operating system you're using. Normally you can either take a screenshot of the whole desktop or just parts of it. For demo purposes, the latter is best, as we've described above.

### System shortcuts

#### Mac OS

* Full screen: <kbd>⌘</kbd> + <kbd>Shift</kbd> +<kbd>3</kbd>
* Partial: <kbd>⌘</kbd> + <kbd>Shift</kbd> +<kbd>4</kbd>, then...
  * move mouse to define the area of screen to capture, *or*
  * press <kbd>SPACE</kbd>, the cursor will change to a camera, move it over the window you want to take a screenshot of and click over it (this will create a screenshot of that window with drop shadow)

#### Windows

TODO

#### Linux

TODO

### Editing screenshots

Often it's not enough with just capturing a screenshot, and it needs editing to make it convey information even more easily.

You can use your favourite graphics editor for this; the process is fairly similar for all of them.

#### Highlighting elements

Use this when you want to draw attention to a single point in the screenshot. For example, if you're talking about a new button that has been added to a toolbar, you will want to point to that button in the screenshot.

A couple of common ways of doing this:

##### Drawing around the area of interest

E.g. using the "pencil" or "brush" tools to draw around element, or point to it with arrows (can be neat if your software has support for it)

![Using brush](./assets/demo-brush.png)

##### Blurring other elements

Select the area of interest, then invert selection, feather ~10px, and apply blur of ~10px too:

![Using blur](./assets/demo-blur.png)

Notice how in this case it doesn't really stand out much as most of the image is very plain and the blurring doesn't cause a significant contrast with the tool we want to highlight.

In this case it might be good to take it a step further and slightly darken the blurred area so we draw full attention to the screenshot button.

Other times we might want to combine several techniques together--play to see what makes the elements stand out more.

##### Avoid annotations with text

Ideally all text would be localised, but text in images is harder to localise than text in text files, as you need to keep the original image and make a localised copy per language.

If you need to highlight several elements in an image, try to just use numbers, and refer to the numbers in your instructions.

This makes it *way easier* to localise demos.

![Using annotations](./assets/demo-annotations.png)

#### Reducing file size

You can make images smaller with tools such as [ImageAlpha](https://pngmini.com/) or any other image optimiser.

## Recording and editing videos

Some people learn better with a video than with text. And some things are better explained with moving images than with lots of text.

Plus, short videos are often good social media material.

### Software for recording videos

#### Mac OS

##### Quicktime player

This comes by default with every Mac and it also allows to record, both fullscreen and just part of the screen.

The drawbacks is that you cannot record the computer's audio and you also cannot edit the recording before exporting (e.g. cropping). So you need to do it all right in just one take, or repeat it several times until you get it right.

However, for basic uses it's a good tool.

##### Screenflow

This is a really good tool. It can capture multiple sources of input, like your screen, external screen, microphone and even the computer's audio channel (great for audio demos), and displays all of them in separate tracks so you can adjust and edit their volumes etc individually.

It also lets you do simple but functional editing such as cropping, zooming in and out, changing the playback speed of clips, etc.

It is not free, but it pays back its worth really quickly.

#### Windows

TODO

#### Linux

TODO

### Other utilities

#### ffmpeg

This is a sort of "swiss army knife" for video manipulation. It can be handy if you want to convert between formats (for example, if you have a WebM video and want to publish to a website that only allows MP4).

TODO: add a few examples because ffmpeg syntax is quite "its own thing".

* convert to GIF
* convert to MP4
* take screenshots and make into movie

#### Keypress overlays

A very useful resource is to show the keys on the screen as you press them--otherwise it might just look as if things are magically happening on the demos. There are tools you can use for this.

##### [Keycastr](https://github.com/keycastr/keycastr) (Mac OS)

Free tool that displays keypresses on the screen. Easy to install with homebrew.

##### Screenflow

It allows you to not only record from your screen but it can also display the keys you pressed while the recording was happening, filter to show just keys used with modifiers (Alt, option, etc), and also adjust the size and position of the overlay.

## Recording GIFs

### [LICEcap](http://www.cockos.com/licecap/) (Mac OS, Windows)

It lets you select the part of the screen you want to capture.

### [GIFBrewery](http://gifbrewery.com/) (Mac OS)

Paid tool, but you can preview your exports and adjust settings, etc.
