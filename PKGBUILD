# Maintainer: pdq <pdq@localhost>
pkgname=geeh
pkgver=0.1
pkgrel=7
pkgdesc="Pretty Damn Quick Github command line tool for Arch linux - GIT Version"
arch=(any)
url="https://github.com/idk/geeh.git"
license=('GPL')
conflicts=(geeh-git)
depends=('git' 'hub')
optdepends=()
makedepends=()
groups=moo
source=('git://github.com/idk/geeh.git')
sha512sums=('SKIP')

package() {
	install -d "$pkgdir/etc/xdg/$pkgname"
	install -Dm644 "$srcdir/$pkgname/$pkgname.conf" "$pkgdir/etc/xdg/$pkgname/$pkgname.conf"
	install -Dm755 "$srcdir/$pkgname/geeh" "$pkgdir/usr/bin/geeh"
	install -Dm644 "$srcdir/$pkgname/man/$pkgname.1" "$pkgdir/usr/local/man/man1/$pkgname.1"
	gzip $pkgdir/usr/local/man/man1/$pkgname.1
}