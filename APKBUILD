# Maintainer: Aleksandr Zelenin <aleksandr@zelenin.me>

pkgname=tdlib
_pkgname_short=td
pkgver=1.3.0
pkgrel=0
pkgdesc="Cross-platform library for building Telegram clients"
url="https://core.telegram.org/tdlib"
arch="all"
license="Boost"
depends="libcrypto1.0 libssl1.0 libgcc libstdc++"
depends_dev="g++ libc-dev openssl-dev zlib-dev"
makedepends="ccache cmake gperf openssl-dev readline-dev zlib-dev"
subpackages="${pkgname}-dev"
source="${pkgname}-${pkgver}.tar.gz::https://github.com/tdlib/td/archive/v$pkgver.tar.gz"
builddir="$srcdir/${_pkgname_short}-$pkgver"

build() {
    mkdir -p "${builddir}/build"
    cd "${builddir}/build"
    cmake \
        -DCMAKE_INSTALL_PREFIX=/usr \
        -DCMAKE_BUILD_TYPE=Release ..
    cmake --build .
}

package() {
    cd "${builddir}/build"
    make DESTDIR="$pkgdir" install
    rm -rf "$pkgdir/usr/lib/cmake"
}

sha512sums="d69a0d0821e4d06b2d15c1eab15b6a2f374a022eecebe9f9fc7e8115213cc6f26fd1ff8dd72b77d469f10cb62548c326516b1b3cdf9a8164aae071cda0490c67  tdlib-1.3.0.tar.gz"
