# Maintainer: pdq <pdq@hush.com>
pkgname=gh
pkgver=0.0.1
pkgrel=1
pkgdesc="Pretty Damn Quick Github command line tool for Arch linux - GIT Version"
arch=(any)
url="https://github.com/idk/gh.git"
license=('GPL')
conflicts=(gh-alpha)
depends=('pacman' 'git' 'hub')
optdepends=()
makedepends=('git')

_gitroot="git://github.com/idk/gh.git"
_gitname="gh"

#install=$pkgname.install

build() {
	cd "$srcdir"
	msg "Connecting to GIT server...."

	if [ -d $_gitname ] ; then
		cd $_gitname && git pull origin
		msg "The local files are updated."
	else
		git clone $_gitroot $_gitname
	fi

	msg "GIT checkout done or server timeout"
	msg "Starting make..."

	rm -rf "$srcdir/$_gitname-build"
	git clone "$srcdir/$_gitname" "$srcdir/$_gitname-build"
	cd "$srcdir/$_gitname-build"

	# Create pkgdir folders
	install -d $pkgdir/usr/bin

	# Install
	cp -r gh $pkgdir/usr/bin/gh
}

