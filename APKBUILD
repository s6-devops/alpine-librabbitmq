# Contributor:
# Maintainer:
pkgname=librabbitmq
pkgver=0.8.0
pkgrel=0
pkgdesc="RabbitMQ C Client"
url="https://github.com/alanxz/rabbitmq-c"
arch="all"
license="MIT"
depends="libressl"
depends_dev="libressl-dev"
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

md5sums="c15dbcd2dbb8e254c1de0494c1bb8c91  rabbitmq-c-0.8.0.tar.gz"
sha256sums="277acd9f624a03a0918d3ba517b9b2950718821844b29d7115e12a716c9d1a07  rabbitmq-c-0.8.0.tar.gz"
sha512sums="f333e378fe7d7d083f10edd7e47869e22c56efe1f508cfea12b741b41e3ed0f6bed236f2aeefc564e6c547676ed1e5d11a9023b20eee27b11984eb0b5f5dc9b2  rabbitmq-c-0.8.0.tar.gz"
