gh
==

Github command line tool for Arch Linux

https://github.com/idk/gh

[linuxdistrocommunity][6]

Install with:

    $ wget https://raw.github.com/idk/gh/master/PKGBUILD -O /tmp/PKGBUILD && cd /tmp && makepkg -sf PKGBUILD && sudo pacman -U gh* && cd


Depends on: git, hub

Setup:
------

Edit the file: /usr/bin/gh

    ## configuration begin ##
    <EDIT AND ADD PERSONAL GITHUB REPOS>
    ## configuration end ##


Usage:
-------------

    gh (GitHub -option)

    -V print version number
    -b backup [-b]
    -m backup commit message [-m]
    -c clone github repo [-c user/repo]
    -r create github repo [-r user/repo]
    -s create submodule [-s user/submodule -r /user/repo]
    -q quiet

Contributing
------------

1. Fork it.
2. Create a branch (`git checkout -b my_gh`)
3. Commit your changes (`git commit -am "Added foo and bar"`)
4. Push to the branch (`git push origin my_gh`)
5. Create an [Issue][7] with a link to your branch
6. Join the Linux Distro Community IRC or Mumble! :D

SHARE AND ENJOY!
----------------

[6]: http://www.linuxdistrocommunity.com
[7]: https://github.com/idk/gh/issues