================================================
wmwm
================================================

.. default-role:: code

`wmwm` is a wacky manager of window manager.

Intro
================================================

`wmwm` stands for **Wacky Manager of Window Manager**. `wmwm` accepts a layout
argument from user and then drives the window manager to lay windows in that
layout pattern. If the result looks funny, you should laugh.

`wmwm` is not a window manager but a manager of window manager. Since `wmwm` is
not a window manager, you don't have to replace your current window manager to
use `wmwm`. `wmwm` works with any X window manager that is EWMH_-compatible.

`wmwm` will layout all windows, excluding maximized and fullscreen ones, in the
current viewport.

Usage
================================================

::

    usage: wmwm [options] <args>

    A wacky manager of window manager.

    positional arguments:
      <layout>              layout name

    optional arguments:
      -h, --help            show this help message and exit
      --loglevel <loglevel>
                            log level
      --exclude <exclude>   exclude window names matching pattern

    available layouts:
        cascade             cascade windows
        hstack              stack windows horizontally
        vstack              stack windows vertically
        bmain               main window on the bottom
        lmain               main window on the left
        rmain               main window on the right
        tmain               main window on the top
        rowgrid[x][y]       row-major grid layout (2 <= x, y <= 4)
        colgrid[x][y]       col-major grid layout (2 <= x, y <= 4)

Shortcuts
------------------------------------------------

Optionally, you can bind `wmwm` to a keyboard shortcut. The binding method may
be WM-specific. Some notable examples are:

-   In `compiz`, you can configure keyboard shortcuts with `ccsm` in menu item
    `General -> Commands`.

-   In a plain X window system, you can use `xbindkeys` to configure keyboard
    shortcuts. `xbindkeys` features a tool `xbindkeys_config` for easy GUI
    configuration.

For other window managers, please consult their manuals.

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

`wmwm` depends on `python-xlib` and `ewmh`.

To install them, run:

::

    pip install python-xlib ewmh

Troubleshooting
================================================

Enable debug mode
------------------------------------------------

Enable debug mode to dump window information:

::

    wmwm --loglevel debug <layout>

Hide all desktop icons
------------------------------------------------

Some file managers manage the desktop by adding a window containing icons. The
desktop can be disabled with either of these two commands:

::

    dconf write /org/gnome/desktop/background/show-desktop-icons false

::

    gsettings set org.gnome.background show-desktop-icons false

Hide windows by names
------------------------------------------------

If there are windows that `wmwm` doesn't handle properly, they can be excluded:

::

    wmwm --exclude <name> <layout>

Window names matching `name` won't be handled by `wmwm`.

Multiple `--exclude` options are supported.

Screenshots
================================================

.. image:: http://projects.cykerway.com/images/wmwm/cascade.png
   :height: 180px
   :width: 320px
   :alt: cascade.png

.. image:: http://projects.cykerway.com/images/wmwm/vstack.png
   :height: 180px
   :width: 320px
   :alt: vstack.png

.. image:: http://projects.cykerway.com/images/wmwm/lmain.png
   :height: 180px
   :width: 320px
   :alt: lmain.png

.. image:: http://projects.cykerway.com/images/wmwm/colgrid23.png
   :height: 180px
   :width: 320px
   :alt: colgrid23.png

More screenshots available at `Project Homepage`_.

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
.. _Project Homepage: http://projects.cykerway.com/wmwm
