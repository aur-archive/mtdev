# Maintainer: SpepS <dreamspepser at yahoo dot it>

pkgname=mtdev
pkgver=1.1.2
pkgrel=1
pkgdesc="A stand-alone library which transforms all variants of kernel MT events to the slotted type B protocol"
arch=(i686 x86_64)
url="http://bitmath.org/code/mtdev/"
license=('custom:MIT')
depends=('glibc')
options=('!libtool')
source=("$url$pkgname-$pkgver.tar.bz2")
md5sums=('d9c7700918fc392e29da7477ae20c5c2')

build() {
  cd "$srcdir/$pkgname-$pkgver"

  ./configure --prefix=/usr \
              --enable-static=no
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"

  make DESTDIR="$pkgdir/" install

  # license
  install -Dm644 COPYING \
    "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

# vim:set ts=2 sw=2 et:
