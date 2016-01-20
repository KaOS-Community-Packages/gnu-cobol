pkgname=gnu-cobol
pkgver=2.0
_pkgsubver=nightly_r658
pkgrel=3
pkgdesc="An open-source COBOL compiler"
arch=('x86_64')
url="http://sourceforge.net/projects/open-cobol/"
license=('GPL')
depends=('db' 'gmp')
options=('!libtool')
install=${pkgname}.install
source=("http://sourceforge.net/projects/open-cobol/files/${pkgname}/${pkgver}/${pkgname}-${pkgver}_${_pkgsubver}.tar.gz")
md5sums=('b7c9a4c7507c79b06f9af6d664b2eacd')


build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr --infodir=/usr/share/info
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
}
