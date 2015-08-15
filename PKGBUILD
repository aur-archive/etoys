# Maintainer: Christophe Gueret <christophe.gueret@gmail.com>
# Contributor: Cilyan Olowen <gaknar@gmail.com>

pkgname=etoys
pkgver=5.0.2408
_realver=5.0.2408
pkgrel=1
pkgdesc="Educational tool for teaching children powerful ideas in compelling ways. For Sugar"
arch=('i686' 'x86_64')
url="http://www.sugarlabs.org/"
license=('GPL')
groups=('sucrose' 'glucose')
depends=('sugar' 'squeak-vm' 'shared-mime-info')
install=etoys.install
source=(http://download.sugarlabs.org/sources/sucrose/glucose/${pkgname}/${pkgname}-${_realver}.tar.gz)
md5sums=('c79ee59d8e100cfc2934af8da90519b5')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"

  PYTHON=python2 ./configure --prefix=/usr --sysconfdir=/etc || return 1
  make || return 1
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make ROOT="$pkgdir" install-etoys install-activity || return 1
}

