================================================
wmwm
================================================

.. default-role:: code

`wmwm` is a wacky manager of window manager.

Intro
================================================

`wmwm` stands for *Wacky Manager of Window Manager*. `wmwm` accepts a layout
argument from user and then drives the window manager to lay windows in that
layout pattern. If the result looks funny, you should laugh.

`wmwm` works with any X window manager that is EWMH_-compatible.

Usage
================================================

`wmwm` is very easy to use. Simply call it with the layout name on the command
line:

::

    wmwm <layout>

And it will arrange all the windows in the current viewport.

Available layouts:

::

    cascade, hstack, vstack, bmain, lmain, rmain, tmain, rowgrid22, rowgrid23,
    rowgrid24, rowgrid32, rowgrid33, rowgrid34, rowgrid42, rowgrid43, rowgrid44,
    colgrid22, colgrid23, colgrid24, colgrid32, colgrid33, colgrid34, colgrid42,
    colgrid43, colgrid44.

Install
================================================

To install via `pip`, run:

::

    pip install wmwm

To install from source, run:

::

    python setup.py install --prefix=/usr

Dependency
================================================

`wmwm` depends on `wmctrl` and `xdotool`.

License
================================================

The source code is licensed under the `GNU General Public License v3.0`_.

Copyright (C) 2016 Cyker Way

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.


.. _EWMH: https://specifications.freedesktop.org/wm-spec/wm-spec-latest.html
.. _GNU General Public License v3.0: https://www.gnu.org/licenses/gpl-3.0.txt