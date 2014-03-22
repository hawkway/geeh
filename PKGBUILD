# Maintainer: pdq <pdq@localhost>
pkgname=geeh
pkgver=0.1
pkgrel=5
pkgdesc="Pretty Damn Quick Github command line tool for Arch linux - GIT Version"
arch=(any)
url="https://github.com/idk/gh.git"
license=('GPL')
conflicts=(geeh-git)
depends=('pacman' 'git' 'hub')
optdepends=()
makedepends=('git')
groups=moo

_gitroot="git://github.com/idk/gh.git"
_gitname="gh"

#install=$pkgname.install

build() {
	cd "$srcdir"
	msg "Connecting to GIT server...."
	if [ -d $_gitname-build ] ; then
		cd $_gitname-build && git pull origin
		msg "The local files are updated."
	else
		msg "Starting make..."
		git clone "$_gitroot" "$srcdir/$_gitname-build"
	fi
}

package() {
	cd "$srcdir/$_gitname-build"
	mkdir -p "$pkgdir/etc/xdg/$pkgname"
	install -Dm644 "$srcdir/$_gitname-build/$pkgname.conf" "$pkgdir/etc/xdg/$pkgname/$pkgname.conf"
	install -Dm755 "$srcdir/$_gitname-build/geeh" "$pkgdir/usr/bin/geeh"
	install -Dm644 "$srcdir/$_gitname-build/man/$pkgname.1" "$pkgdir/usr/local/man/man1/$pkgname.1"
	gzip $pkgdir/usr/local/man/man1/$pkgname.1
	rm -rf "$srcdir/$_gitname-build"
}