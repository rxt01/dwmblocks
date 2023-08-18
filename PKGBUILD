# Maintainer: Rxt01 <rxt012713@proton.me>

pkgname=rxtdwmblocks
_pkgname=dwmblocks
pkgver=1.1
pkgrel=1
epoch=1
pkgdesc="dwmblocks"
url='https://github.com/rxt01/dwmblocks'
arch=('i686' 'x86_64')
license=('MIT')
options=('zipman')
depends=('playerctl')
makedepends=('git')
source=('git+https://github.com/rxt01/dwmblocks')
sha1sums=('SKIP')

provides=("${_pkgname}")
conflicts=("${_pkgname}")


build(){
    cd "${_pkgname}"
    make
}

package() {
	cd "${_pkgname}"
	make PREFIX=/usr DESTDIR="${pkgdir}" install
	install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
	install -Dm644 README.md "${pkgdir}/usr/share/doc/${pkgname}/README.md"
}
