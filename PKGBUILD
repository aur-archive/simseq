# Maintainer: Arch Haskell Team <arch-haskell@haskell.org>
_hkgname=simseq
pkgname=simseq
pkgver=0.0
pkgrel=3
pkgdesc="Simulate sequencing with different models for priming and errors"
url="http://hackage.haskell.org/package/${_hkgname}"
license=('GPL')
arch=('i686' 'x86_64')
makedepends=('ghc' 'haskell-bio>=0.2' 'haskell-bytestring=0.9.1.7' 'haskell-random=1.0.0.2')
depends=('gmp')
options=('strip')
source=(http://hackage.haskell.org/packages/archive/${_hkgname}/${pkgver}/${_hkgname}-${pkgver}.tar.gz)
build() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup configure --prefix=/usr --docdir=/usr/share/doc/${pkgname} -O
    runhaskell Setup build
}
package() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup copy --destdir=${pkgdir}
}
md5sums=('406aaf2ddd814a1171250056b7aae260')
