
SVGSlice version 0.13
#####################




First of all, read "Issues", below.

Installation
============

In a normal inkscape distro installation, copy the files:

  svgslice.inx
  svgslice.py

to:

  /usr/share/inkscape/extensions

If your inkscape extensions directory is somewhere other than this, then you need
to edit both files to use your chosen directory.

Usage
=====

* Draw something.

* Create a layer called "slices".

* Draw rectangles in this layer representing the areas you want to slice 
(note: it helps if you make the rectangles semi-transparent)

* Optionally, name any/all slices by using the built-in XML editor to edit the 
"id" attributes of the rectangles.

* Hide the slices layer.

* Choose "Save as..." from the File menu.

* Select "XHTML file with PNG slices" as the file type to use.

* Enter a filename (e.g., "test.xhtml"), and save.


Result
======
* You should have the test.xhtml file on your disk, alongside the PNG slices 
for each area of the drawing that you made a rectangle for.



Issues
======

Starting Inkscape from the right directory
------------------------------------------

The Inkscape plugin mechanism was never really designed for outputting more than one file at a time.  As such, it doesn't give plugins any idea of where they should save their output.  So, the only way that SVGSlice can save slices in the same directory as your svg drawing is if Inkscape is started IN that directory.  Generally, the way to do this is to load the SVG drawing by double-clicking on it, rather than loading Inkscape and then opening your drawing.

AGAIN: open your SVG files from their icons, rather then from a pre-loaded copy if inkscape, if you want slices to be saved in the right place.

Sorry for this inconvenience, but there's really nothing I can do until the Inkscape developers come up with a better plugin system.


Windows Support
---------------

SVGSlice is developed for unix workstations like BSD and Linux; not Microsoft Windows.  Furthermore, the Inkscape plugin API seems to work differently on each platform.  How to get it working on a non-POSIX-compliant platform like Windows is left as an exercise for the reader.  The main things you'll need to do are: a) install in the right place and change directory paths within the files to match; and b) modify the command lines executed within svgslice.py so that windows understands them.


Support
=======

Please email any bug reports, questions, or comments to:

  lee.b@digitalunleashed.com
