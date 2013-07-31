# SASS/Compass responsive SVG mixin
Copyright (C) 2013 Jerad Gallinger - [[Website]](http://jeradgallinger.ca "jeradgallinger.ca") - [[GitHub]](https://github.com/jeradg/compass-responsive-svg "github.com/jeradg/compass-responsive-svg")
Released under the GPLv3 license. [[View the license]](http://www.gnu.org/licenses/ "GPLv3")

## What is this?

This is a Compass mixin for responsive inline SVGs with PNG sprite fallbacks. The mixin creates an inline SVG background image in the CSS, with fallback to a PNG sprite.

## Requires

The mixin requires [[Modernizr]](http://modernizr.com/ "Modernizr") inline SVG detection and [[Compass]](http://compass-style.org/ "Compass").

## Using the mixin

``@import`` the mixin in your style.scss file.

Place an SVG in the ``img/svg-src`` folder (where 'img' is your Compass project's image folder), and a corresponding PNG in the ``img/svg-png-fallbacks`` folder. (E.g., ``my-image.svg`` and ``my-image.png``.)

### Default usage

``@include responsive-svg( my-image );``

(Note: Don't put quote marks around $img-name.)

### Arguments

The mixin takes one required argument, ``$img-name`` (the image's name, without the file extension), and two optional arguments:

- ``$set-dimensions``: If ``true``, uses the PNG's height and width to set the height and width of the selector in which the mixin is called. If ``false``, the mixin doesn't set the selector's dimensions. (Default: ``true``.)
- ``$image-replace``: If ``true``, uses ``text-indent: -9999px`` to replace text with the image. If false, doesn't hide text. (Default: ``true``.)

## See it in action

I developed the mixin for the sponsor logos on the Stephen Lewis Foundation's [[Solidarity Tour website]](http://www.solidaritytour.ca/#sponsors "Solidarity Tour").
