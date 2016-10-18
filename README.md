# devtools-demos

> A collection of demos for features in Firefox DevTools

We use these for the posts in [the Firefox Nightly blog](http://blog.nightly.mozilla.org/), twitter announcements in [@FirefoxDevTools](https://twitter.com/FirefoxDevTools) and generally everywhere we want to talk about these features.

## Contributing

Contributions are more than welcome! There are many features and bugs fixed in [DevTools](https://wiki.mozilla.org/DevTools) every week and we would totally *love* your help talking about them.

### Choosing a feature to talk about

We want to talk about new features or closed bugs in DevTools recently, not in Firefox in general, so find recently resolved bugs with this [Bugzilla search](https://mzl.la/2dKlnV2) (Firefox Devtools bugs are tracked there).

To avoid duplicating work, look in the [issues page](https://github.com/mozdevs/devtools-demos/issues) to see if someone is already working on making a demo for a specific feature. Issues should be named in the format `bug-number - description of bug`, where the bug number is the number in Bugzilla. For example, `bug 12345678 - demo feature ABC` would correspond to the bug 12345678 in Bugzilla. If no one is working on it, create a new issue with the same format so others can find it, and state that you want to work on it.

### Demoing a feature

We suggest you create a new branch to work on the feature. Name it something like `bug-number`, as it makes things easy to track. Make it your current git branch. Then make a new directory, named like the feature you want to demonstrate (but with hyphens, like [this](./debugging-inline-whitespace)).

The Bugzilla page for the feature will often contain a lot of information, but that is normally just useful for the developer implementing the feature, code reviewers, QA/integration testers, and so on, and very rarely useful for the end web developer that uses Devtools.

Your challenge here is to find a way to demo the new feature to web developers. Some features can be explained with an image. Other features are best demoed with a short screen capture (videos or GIFs, but videos are better, because they can be paused AND converted to GIF if need be). This depends on each feature, and some people simply prefer to see a written description. To top it all, not all features are easily demoable, specially the ones that do not have user visible changes. If you're unsure, tell us about your ideas when you create the issue, and we can provide feedback.

At a minimum, a demo folder will contain:

* `index.html` page containing HTML to demonstrate the feature. Possibly additional JavaScript and CSS files, if required. This will be linked from the Nightly blog.
* `README.md` explaining what the demo is about, how to use the feature, etc. We will use this for the blog post as well as documentation for the tools in MDN, etc. And it's clear what the demo is when browsing the repository.
* And any additional images, videos or demonstrative assets. It's possible that there are already images you can use in the [assets](./assets) folder. Feel free to use these instead of adding new images.

<!--TODO: There's also [the template](./template) to guide you.-->

In case of doubt, or to get inspired, you can look at existing demos and follow the same style.

