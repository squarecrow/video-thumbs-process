Synfig LP Thumbnail Template

Tested in
Synfig 1.2.2 Windows 64 Portable (Wine 1.6.2)
Synfig 1.2.2 Appimage (Linux Mint 17.2 [Ubuntu 14.04] 64bit)

META
----
This README is written in the MarkDown formatting syntax.
This file should also come with:
An example synfig project: "vid-th-synfig.sifz".
A screenshot image: "vid-th-synfig-scr.jpg".

Introduction
------------
Synfig is a vector-based, tween-based animation program,
 not suitable at all for frame-by-frame drawing.

Current URL: https://www.synfig.org/

Synfig can set and animate any properties of any layer type,
be it gradient, external image, text, shape etc.

This template, and method, is for making sequenced video
 thumbnail/cover images, with labels for video number and 
 commentary, or other visual demarcation.


Advantages over image editors
(Photoshop, Photopea, Krita, GIMP)
----------------------------------
The method for most image editors would be:

Create video thumbnail project, slightly edit
 contents for each thumbnail in the sequence,
 export for each one with a different filename.

The more you want to differentiate the thumbnails,
 the more time you have to spend editing for each one.

When correctly prepared, this project can churn
 out all of the required final images in just four clicks,
 even with drastic or long gradual changes across the images,
 without any manual layer editing or visibility toggling.

Create once, render everything.


Disadvantages
-------------
Synfig's default interface and use is for tween-animators,
not image editors, compositors, or illustrators.

This method is very specific to Synfig, though it
might accidentally teach or clear up related concepts.

Synfig may be unstable and error-prone on certain platforms.

Currently, Synfig can only store one render pathname at a time.
So thumbnails that are different in more ways than just
sequence numbers need a new pathname each time.

The text tool does not always properly use the font field,
is unable to detect the font, or unable to use variants such
as italic or bold. One solution is to put the full pathname
of the font with the desired variant, in the font field.
For example: "path/to/TheFontItBd.ttf"

Example
-------
The example file, that comes with this Read Me,
contains the following visuals:

Labels for voice-over, toggled with VOCut.

A number label, increases every frame.

A video duration indicator, scaled for 168x94 thumbnails.


TODO
----
Multiple thumbnail modes, besides just cut and uncut,
probably not operated through Switch statements.


The Method
----------
Library
  * ValueBase Nodes
    * VOCut
      * Type: Boolean (On/Off)
        * A variable that other layer
          properties can connect to,
          meant for switching between
          "cut" and "uncut" mode.

Layers
  * Group
    * Layer1,Layer2, etc
  * Switch
    * LayerA,LayerB, etc

Parameters (Current layer)
  * Property A:
    * Gets value from this:
      * On
      * Off
      * Switch: Connected to VOCut.
  * Property B:
    * Gets value from this:
      * Rate: Increase by this number every frame.
    
File
  * Render
    * Render sequence filename will be
      numbered, but "cut" and "uncut"
      must be added manually, for each.


Conclusion
----------
Depending on the user's personal tastes, hardware, operating
 system, knowledge, time and money, this method may be
 preferable to others.

Under some conditions it may save a lot of time and confusion
 with batch image writing, under others it may just waste more
 time and add confusion and frustration.

Beginners should avoid using it on critical deadlines or
 projects.

This is far from the only program out there that can be
 repurposed for this. There may be others that you will be
 more familiar or comfortable with. This is one of the real
 points; finding new (sometimes strange) ways to render
 sequences of images with multiple forms of visual media
 in batch.
