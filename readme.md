## Overview ##
The YUI Compressor Bundle enables easy compression of JavaScript and CSS files using the [YUI Compressor][yui], right from within [TextMate][tm].

No more faffing about on the command line or within separate apps in order to combine and compress your JavaScript and CSS files for production.

Just select the files you want to process in the TextMate project drawer, hit a shortcut, and you're done.

## Requirements ##
The YUI Compressor TextMate Bundle requires:

* [The Yahoo! YUI Compressor][yui_dwn].
* Python version 2.5 or greater (installed as standard on Mac OS 10.5 and above).
* [TextMate][tm] (obviously).

## Installation ##
1. Extract the YUI Compressor TextMate Bundle ZIP file.
2. Copy the `yuicompressor.jar` file to a location of your choosing.
3. Double-click `YUI Compressor.tmbundle` to install the bundle in TextMate.
4. Open TextMate, and navigate to [the Bundle Editor][bundle].
5. Select the `Preferences...` item from the `YUI Compressor` bundle, and replace the text `/absolute/path/to/yuicompressor.jar` with the actual path to the `.jar` file from step 2. Note that this must be an _absolute_ path; `~/` won't work.

## Usage ##
Select the files you want to compress in the Project Drawer, and execute the command using `⌃⇧Y` (control-shift-Y).

The compressed files share the same root filename, with the addition of `.min` before the file extension. For example:

* `my_css_file.css` becomes `my_css_file.min.css`.
* `my_js_file.js` becomes `my_js_file.min.js`.

It's worth noting that:

* Existing files with the same name will be overwritten without warning.
* Files with an extension other than `.css` or `.js` will be silently ignored.
* When compressing a JavaScript file, the `--nomunge` option is automatically enabled.

## License ##
The YUI Compressor TextMate Bundle is made available under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0" title="Creative Commons license">Creative Commons Attribution-Share Alike 3.0 Unported License</a>.

All code specific to the YUI Compressor itself is issued under a BSD license. YUI Compressor extends and implements code from Mozilla's Rhino project, which is issued under the Mozilla Public License (MPL).

## Support ##
The YUI Compressor TextMate Bundle is no longer under active development, but if you have a problem please [post a support request][support].

## Changelog ##
### 1.0.3 (released 16th June, 2009) ###

* Fixed bug whereby file paths with spaces were not being processed.
* Updated bundled YUI Compressor to version 2.4.2.

### 1.0.2 (released 8th April, 2009) ###

* Added changelog.
* Implemented a friendlier error message when the user attempts to run the compressor without first selecting any files.

[bundle]:http://manual.macromates.com/en/bundles "Find out more about the TextMate Bundle Editor"
[support]:http://support.experienceinternet.co.uk/discussions/yui-compressor-tm-bundle/ "Official support for the YUI Compressor TextMate Bundle"
[tm]:http://macromates.com/ "Visit the TextMate website"
[yui]:http://developer.yahoo.com/yui/compressor/ "Find out more about the YUI Compressor from Yahoo!"
[yui_dwn]:http://www.julienlecomte.net/yuicompressor/ "Download the YUI Compressor"