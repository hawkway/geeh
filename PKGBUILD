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
	if [ -d $_gitname-build ] ; then
		cd $_gitname && git pull origin
		msg "The local files are updated."
	else
		git clone $_gitroot $_gitname
	fi
	
	msg "GIT checkout done or server timeout"
	msg "Starting make..."
	git clone "$srcdir/$_gitname" "$srcdir/$_gitname-build"
}

package() {
	cd "$srcdir/$_gitname-build"
	# Install
	install -Dm755 "$srcdir/$_gitname-build/$pkgname" "$pkgdir/usr/bin/$pkgname"
	install -Dm644 "$srcdir/$_gitname-build/man/$pkgname.1" "$pkgdir/usr/local/man/man1/$pkgname.1"
	gzip $pkgdir/usr/local/man/man1/$pkgname.1
	rm -rf "$srcdir/$_gitname-build"
}