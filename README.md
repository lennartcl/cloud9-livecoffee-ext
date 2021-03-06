Cloud9 Live CoffeeScript Extension
==================================

This live CoffeeScript extension for Cloud9 provides a window view of the live
formatted JavaScript output of a CoffeeScript file as you type.

The window provided has the option to view the output with bare compiling (i.e
not closure) on or off via a checkbox.

Installation
------------

This extension works with c9.io and with self-hosted copies of Cloud9 (either via
cloning `https://github.com/ajaxorg/cloud9` or `npm install cloud9`). To install
it, open the `Tools -> Extension Manager` window in Cloud9, and enter the extension
path:

    https://github.com/lennartcl/cloud9-livecoffee-ext

or

    ext/livecoffee/livecoffee

for a self-hosted copy.

Click add. You can now view the window via the Edit menu.

Options
-------

* Approx Line Match: During compile, the live view will match the line number of
the file you are working on. This is an approximate match of the code output
location. When the livecoffee window is open, matching blocks of CoffeeScript
and JavaScript are also automatically highlighted as you click in the source
code. The approximate line matching is provided thanks to the [CoffeeScriptLineMatcher project](https://github.com/showell/CoffeeScriptLineMatcher)

* Compile Bare: Compile the output without the surrounding closure

* Compile Nodes: Enable the nodes tab and output the node structure of the code

* Compile Tokens: Enable the tokens tab and output the tokens from the lexer

Shortcut Keys & Command
-----------------------
This extension comes with the `livecoffee` command that you can type into the
command area to launch the window.

You can also add shortcut keys to your `ext/keybindings_default` files.  Edit
`default_win.js` or `default_mac.js` depending on your platform.  To enable
it add the following:

    return keys.onLoad({
        "ext" : {
            "livecoffee": {
                "livecoffee": "Ctrl-Shift-K"   
            }
        }
    })

For the Mac, use `Command-Option-K`, or choose your own key shortcuts.

Author: Tane Piper (@tanepiper)

Thanks to Matt Pardee for helping solve the key and command issues.

Screenshot
----------
![A picture of Livecoffee](http://dl.dropbox.com/u/147175/livecoffee.png)
