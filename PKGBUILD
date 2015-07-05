# vim:set ts=2 sw=2 et:
# Maintainer: Alad Wenter <aladw@linuxbbq.org>
# Contributor: Xavier D. <magicrhesus@ouranos.be>
# Contributor: Valère Monseur <valere.monseur@ymail.com>

pkgname=eid-mw
pkgver=4.0.6
pkgrel=2
pkgdesc="The eID middleware for the Belgian eID"
url="http://eid.belgium.be/"
arch=('i686' 'x86_64')
license=('LGPL3')
depends=('pcsclite' 'gtk2')
optdepends=('firefox: extension for Belgian eid'
'acsccid: ACS CCID smart card readers'
'pcsc-tools: PC/SC smartcard tools')
source=("http://eid.belgium.be/nl/binaries/${pkgname}-${pkgver}-1480.tar_tcm227-250016.gz")
options=('!libtool')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr --libexecdir=/usr/bin
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make install DESTDIR="${pkgdir}"
}

sha256sums=('1ff3a7740a30891df2da12fca66cb5324dc286f9490ee839d61d9f1028b9127c')
