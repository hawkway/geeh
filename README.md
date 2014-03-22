geeh
==

A Github command line tool for Arch Linux

https://github.com/idk/gh

[linuxdistrocommunity][6]

Install:
--------
    $ wget https://raw.github.com/idk/gh/master/PKGBUILD && makepkg -sfi

Depends on: git, hub

    sudo pacman -S git hub

Setup:
------

Copy and edit the config file:
    
    mkdir -p ~/.config/geeh && cp /etc/xdg/geeh/geeh.conf ~/.config/geeh/geeh.conf

Usage:
------

    geeh (GitHub -option)

    -V print version number
    -b backup [-b]
    -m backup commit message [-m]
    -c clone github repo [-c user/repo]
    -r create github repo [-r user/repo]
    -s create submodule [-s user/submodule -r /user/repo]
    -q quiet

Contributing:
-------------

1. Fork it.
2. Create a branch (`git checkout -b my_geeh`)
3. Commit your changes (`git commit -am "Added foo and bar"`)
4. Push to the branch (`git push origin my_geeh`)
5. Create an [Issue][7] with a link to your branch
6. Join the Linux Distro Community IRC or Mumble! :D

SHARE AND ENJOY!
----------------

[6]: http://www.linuxdistrocommunity.com
[7]: https://github.com/idk/gh/issues