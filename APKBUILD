# Contributor:
# Maintainer:
pkgname=librabbitmq
pkgver=0.7.1
pkgrel=0
pkgdesc=""
url=""
arch="all"
license=""
depends="openssl"
depends_dev="openssl-dev"
makedepends="$depends_dev"
install=""
subpackages="$pkgname-dev $pkgname-doc"
source="https://github.com/alanxz/rabbitmq-c/archive/v$pkgver.tar.gz"

_builddir=
prepare() {
	local i
	cd "$_builddir"
	for i in $source; do
		case $i in
		*.patch) msg $i; patch -p1 -i "$srcdir"/$i || return 1;;
		esac
	done
}

build() {
	cd "$_builddir"
}

package() {
	cd "$_builddir"
}

md5sums="c40427844e7a2b94f9687fa7606829ee  v0.7.1.tar.gz"
sha256sums="0b9b81d05b3e629c3449521690de400fe4539a8ba1feacadcbd6e9a50c8a4625  v0.7.1.tar.gz"
sha512sums="63cca5e0022d7e655438c0701b55ac49de1702e4324ef1cf335801e4699ca8bfc2268836b7694fa0a0d2ba4d1f7f0408f64c9c4d5e6e23d99d26d2c1c7f00211  v0.7.1.tar.gz"
