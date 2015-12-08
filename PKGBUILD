# vim:set ts=2 sw=2 et:
# Maintainer: Alad Wenter <alad@archlinux.info>
# Contributor: Xavier D. <magicrhesus@ouranos.be>
# Contributor: Valère Monseur <valere.monseur@ymail.com>

pkgname=eid-mw
pkgver=4.1.9
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
source=("https://dist.eid.belgium.be/continuous/sources/$pkgname-$pkgver-v$pkgver.tar.gz"{,.asc})
sha256sums=('0c46c73b805884dd4ae739eb6025c137c1055ad119eac1ab37cb83eb32d92953'
            'SKIP')
validpgpkeys=('D95426E309C0492990D8E8E2824A5E0010A04D46')

build() {
	cd "$pkgname-$pkgver-v$pkgver"
  ./configure --prefix=/usr --libexecdir=/usr/bin
  make
}

package() {
	cd "$pkgname-$pkgver-v$pkgver"
	make install DESTDIR="$pkgdir"
}

