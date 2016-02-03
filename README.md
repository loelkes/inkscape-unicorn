SphereBot G-Code Output for Inkscape
===========================================

This is an Inkscape extension that allows you to save your Inkscape drawings as
G-Code files suitable for plotting with the [SphereBot](http://pleasantsoftware.com/developer/3d/spherebot/).

It is based on the [MakerBot Unicorn G-Code](https://github.com/martymcguire/inkscape-unicorn) from [Marty McGuire](http://github.com/martymcguire).

**This is under developpment and not working yet**

Credits
=======

* [Marty McGuire](http://github.com/martymcguire) pulled this all together into an Inkscape extension.
* [Inkscape](http://www.inkscape.org/) is an awesome open source vector graphics app.
* [Scribbles](https://github.com/makerbot/Makerbot/tree/master/Unicorn/Scribbles%20Scripts) is the original DXF-to-Unicorn Python script.
* [The Egg-Bot Driver for Inkscape](http://code.google.com/p/eggbotcode/) provided inspiration and good examples for working with Inkscape's extensions API.
* [Christian Lölkes](https://github.com/loelkes) adapted this for the SphereBot with a Marlin firmware.

Install
=======

Copy the contents of `src/` to your Inkscape `extensions/` folder.

Typical locations include:

* OS X - `/Applications/Inkscape.app/Contents/Resources/extensions`
* Linux - `/usr/share/inkscape/extensions`
* Windows - `C:\Program Files\Inkscape\share\extensions`

Usage
=====

* Size and locate your image appropriately:
	* The SphereBot draw size is 3200 x 800 pixel.
	* Setting units to **pixel** in Inkscape makes it easy to size your drawing.
	* The extension will automatically attempt to center everything.
	* 3200 pixel is the complete sphere, 800 pixel 1/4 of it.
* Convert all text to paths:
	* Select all text objects.
	* Choose **Path | Object to Path**.
* Save as G-Code:
	* **File | Save a Copy**.
	* Select **MakerBot Unicorn G-Code (\*.gcode)**.
	* Save your file.
* Preview
	* For OS X, [Pleasant3D](http://www.pleasantsoftware.com/developer/pleasant3d/index.shtml) is great for this.
	* For other operating systems... I don't know!
* Print!
	* Use your normal 3D printing software together with the SphereBot.

TODOs
=====

* Rename `*PolyLine` stuff to `*Path` to be less misleading.
* Formalize "home" to be a reasonable place to change pages/pens.
* Parameterize smoothness for curve approximation.
* Use native curve G-Codes instead of converting to paths?
* Include example templates?
