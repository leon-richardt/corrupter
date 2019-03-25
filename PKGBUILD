# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Leon Richardt <leon.richardt@gmail.com>
pkgname=corrupter
pkgver=0.3
pkgrel=1
pkgdesc="Image glither for PNG files"
arch=("x86_64")
url="https://github.com/leon-richardt/corrupter"
license=("custom:BSD 2-Clause")
makedepends=("go")
conflicts=("corrupter")
provides=("corrupter")
source=("corrupter::git+$url")
md5sums=("SKIP")

build() {
	cd "$srcdir/$pkgname"
	go build -o corrupter
}

package() {
    install -Dm755 "$srcdir/$pkgname/corrupter" "$pkgdir"/usr/bin/corrupter
}
