# Maintainer: Konstantin Unruh <freaxmate@protonmail.com>
pkgname=pop-metacity-theme
pkgver=5.3.1
pkgrel=1
pkgdesc="System76 Pop Metacity Theme"
arch=('any')
url="https://github.com/FreaxMATE/$pkgname"
license=('GPL3')
makedepends=('meson')
optdepends=('pop-gtk-theme: for Pop GTK Theme'
            'pop-icon-theme: for Pop Icon Theme')

source=("$pkgname-$pkgver.tar.gz::https://github.com/FreaxMATE/$pkgname/archive/v$pkgver.tar.gz")


build() {
  cd "$pkgname-$pkgver"
  meson --prefix=/usr build
}

package() {
  cd "$pkgname-$pkgver"
  DESTDIR="$pkgdir" ninja install -C build
}

