# Tab Counter Wide

This is a fork of Loirooriol's fantastic [Tab Counter Plus](https://github.com/Loirooriol/tab-counter-plus) to do some slightly messy customization to allow for a wider tab counter. Please see the README on that page for full details.

This provides the ability to include the current tab index in addition to the total number of tabs in the window.

[Download on addons.mozilla.org](https://addons.mozilla.org/en-US/firefox/addon/tab-counter-wide/)!

![screenshot](docs/screenshot.png)

This is accomplished by **requiring** the following to be added to the userChrome.css file:
``` css
/* Normally has right/left-padding of 1px - remove it all */
toolbarbutton#tab-counter-wide_jmmerz_github-browser-action {
    padding-left: 0px !important;
    padding-right: 0px !important;
}
/* Normally has right/left-padding of 6px - remove it all */
toolbarbutton#tab-counter-wide_jmmerz_github-browser-action > .toolbarbutton-badge-stack {
    padding-top: 0px !important;
    padding-bottom: 0px !important;
    padding-left: 0px !important;
    padding-right: 0px !important;
}

/* Standard height/width is 16px/16px. Tabbar height is 28px so that's pretty fixed,
 * but we can adjust width as needed. These should match the icon dimensions in the code. */
toolbarbutton#tab-counter-wide_jmmerz_github-browser-action > .toolbarbutton-badge-stack > .toolbarbutton-icon {
    height: 28px !important;
    width: 56px !important;
}
```

## Version History:

#### [1.4.1](https://github.com/jmmerz/tab-counter-wide/releases/tag/v1.4.0):
* Update minimum Firefox version to 62.0.

#### [1.4.0](https://github.com/jmmerz/tab-counter-wide/releases/tag/v1.4.0):
* Fix performance issue that could cause browser to slow down, especially with a moderate to large
  number of tabs open.
* Switch to a better name.
* Add standardized instructions to make this this extension more usable.

#### [1.3.0](https://github.com/jmmerz/tab-counter-wide/releases/tag/v1.3.0):
* Update name to "Tab Counter Wide" to better describe what's unique about it.

#### [1.2.1](https://github.com/jmmerz/tab-counter-wide/releases/tag/v1.2.1):
* Various updates/improvements
* Provide additional options for counting hidden tabs.
* General code cleanup.

#### [1.0.0](https://github.com/jmmerz/tab-counter-wide/releases/tag/v1.0.0):
* Initial release - this provides the ability to use a 28x56px button and include the tab number in the count.

