# vim:set ts=2 sw=2 et:
# Maintainer: Alad Wenter <alad@archlinux.info>
# Contributor: Xavier D. <magicrhesus@ouranos.be>
# Contributor: Valère Monseur <valere.monseur@ymail.com>

pkgname=eid-mw
pkgver=4.1.2
_pkgver=$pkgver-v4.1.2
_tarver=tcm227-258906
pkgrel=1
pkgdesc="The eID middleware for the Belgian eID"
url="http://eid.belgium.be/"
arch=('i686' 'x86_64')
license=('LGPL3')
depends=('pcsclite' 'gtk2')
optdepends=('firefox: extension for Belgian eid'
	'acsccid: ACS CCID smart card readers'
	'ccid: A generic USB Chip/Smart Card Interface Devices driver'
	'pcsc-tools: PC/SC smartcard tools')
source=("http://eid.belgium.be/nl/binaries/$pkgname-$_pkgver.tar_$_tarver.gz")
sha256sums=('7907cfe9f21e5b4f008badbd09d282ec201742aa5f1a67f6c1ec7e838bf7ab89')
options=('!libtool')

build() {
	cd "$pkgname-$_pkgver"
  ./configure --prefix=/usr --libexecdir=/usr/bin
  make
}

package() {
	cd "$pkgname-$_pkgver"
	make install DESTDIR="$pkgdir"
}

