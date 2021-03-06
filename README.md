# transporter

Simple [magic-wormhole](https://github.com/warner/magic-wormhole) client designed for GNOME.
This is a fork of the elementary OS app [Transporter](https://github.com/bleakgrey/Transporter).

![Transporter Screenshot](https://raw.githubusercontent.com/1enn0/transporter/master/data/screenshot.png)

## Building and Installation

You'll need some dependencies to build:
* libgranite-dev
* meson
* valac

And you'll need these to actually run [magic-wormhole](https://github.com/warner/magic-wormhole):
* build-essential
* libffi-dev
* libssl-dev
* python-pip
* python-dev
* zip


Run these commands to configure the build environment:

    meson build --prefix=/usr
    cd build

Finally, install and execute with:

    sudo ninja install
    com.github.bleakgrey.transporter

## Contributing

If you feel like contributing, you're always welcome to help the project in many ways:
* Reporting any issues
* Suggesting ideas and functionality
* Submitting pull requests

## Credits
* Lithuanian translation by <a href="https://github.com/welaq">@welaq</a>
* French and Italian translation by <a href="https://github.com/papou84">@papou84</a>
* Brazilian Portuguese translation by <a href="https://github.com/btd1337">@btd1337</a>
* German translation by <a href="https://github.com/p3732">@p3732</a>
