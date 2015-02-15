===========================
Custom X11 Keyboard Layouts
===========================


First, get ``setxkbmap``. For me (on Gentoo), it wasn't installed by default.


Dumping the present layout
==========================

``setxkbmap -print`` will show you the very high level view::

    % setxkbmap -print
    xkb_keymap {
        xkb_keycodes  { include "evdev+aliases(qwerty)"	};
        xkb_types     { include "complete"	};
        xkb_compat    { include "complete"	};
        xkb_symbols   { include "pc+us+inet(evdev)+compose(ralt)"	};
        xkb_geometry  { include "pc(pc104)"	};
    };

(This is all ``original-layout`` in this repository is, in fact!)

You can also run ``xkbcomp :0 - | less``, which will show you the compiled
version. This is basically after all the includes have been expanded and
whatnot.

Resources that helped me
========================

* The `Neo Keyboard Layout`_, very much an inspiration.
* Madduck's `Extending the X Keyboard Map with XKB`_.
* `Madduck's keyboard layout`_.

.. _Neo Keyboard Layout: http://wiki.neo-layout.org/browser/linux/X/
.. _Extending the X Keyboard Map with XKB: http://madduck.net/docs/extending-xkb/
.. _Madduck's keyboard layout: http://git.madduck.net/v/etc/xsession.git/tree/HEAD:/.xkb
