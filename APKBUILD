# Contributor:
# Maintainer:
pkgname=librabbitmq
pkgver=0.7.1
pkgrel=0
pkgdesc="RabbitMQ C Client"
url="https://github.com/alanxz/rabbitmq-c"
arch="all"
license="MIT"
depends="openssl"
depends_dev="openssl-dev"
makedepends="$depends_dev"
install=""
subpackages="$pkgname-dev"
source="https://github.com/alanxz/rabbitmq-c/releases/download/v$pkgver/rabbitmq-c-$pkgver.tar.gz"

_builddir=${srcdir}/rabbitmq-c-${pkgver}
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
	mkdir build
	cd build
	cmake -DCMAKE_INSTALL_PREFIX=$pkgdir/usr ..
}

package() {
	cd "$_builddir"
	cd build
	cmake --build . --target install
}

md5sums="6216c8876299a5efc4ff5ff84dc636d8  rabbitmq-c-0.7.1.tar.gz"
sha256sums="23df349a7d157543e756acc67e47b217843ecbdafaefe3e4974073bb99d8a26d  rabbitmq-c-0.7.1.tar.gz"
sha512sums="197b8476373e3a9056d5f24e0d932a37a556a946d2b6471c95e8b0e693b611de51882be4911bd099f2c2e76153225d83cac1bec8106c031058315f062a8a4ab4  rabbitmq-c-0.7.1.tar.gz"
