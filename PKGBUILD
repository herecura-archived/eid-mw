# Maintainer: Xavier D. <magicrhesus@ouranos.be>

pkgname=eid-mw
pkgver=4.0.2
pkgrel=1
pkgdesc="eID MiddlewareS"
url="https://code.google.com/p/eid-mw/"
arch=('i686' 'x86_64')
license=('GPL')
depends=('pcsclite' 'gtk2')
makedepends=('autoconf' 'automake')
source=("https://eid-mw.googlecode.com/files/${pkgname}-${pkgver}-1188.tar.gz"
	"patch-gcc47.patch")
sha1sums=('a659800484f993a403881ab593df655ee834da1e'
	'f65332bffdec987464b24fc2039d16b8a079317e')
options=('!libtool')

build() {
    cd "${srcdir}/${pkgname}-${pkgver}"
    patch -p1 < ${srcdir}/patch-gcc47.patch
    ./configure --prefix=/usr
    #./configure
    make
    make DESTDIR=${pkgdir} install
}
