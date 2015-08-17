# $Id: PKGBUILD 23714 2010-08-15 06:01:03Z shusmann $
# Contributor: Allan McRae <allan@archlinux.org>
# Contributor: Claudio Riva <firetux83@gmail.com>
# Maintainer: Stefan Husmann <stefan-husmann@t-online.de>

pkgname=winefish-gtk
_pkgname=winefish
pkgver=1.3.3
pkgrel=9
pkgdesc="LaTeX editor based on Bluefish with auto-completion and syntax highlighting"
url="http://winefish.berlios.de/"
arch=('i686' 'x86_64')
license=('GPL')
depends=('gtk2')
makedepends=('pkgconfig')
optdepends=('aspell: for spell check')
install=$_pkgname.install
source=(http://download.berlios.de/$_pkgname/$_pkgname-$pkgver.tgz)
md5sums=('63531e4dde7a53ab3a74e1152c7af1e9')

build() {
  cd ${srcdir}/${_pkgname}-${pkgver}
  ./configure --prefix=/usr --disable-update-databases \
    --with-freedesktop_org-menu=/usr/share/applications \
    --with-icon-path=/usr/share/pixmaps --mandir=/usr/share/man
  make
}
package() {
  cd ${srcdir}/${_pkgname}-${pkgver}
  make DESTDIR=${pkgdir} install
}
