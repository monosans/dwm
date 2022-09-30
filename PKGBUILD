_pkgname=dwm
pkgname=${_pkgname}-monosans-git
pkgver=6.4.r628.3881ad4
pkgrel=1
pkgdesc='monosans dwm build'
url=https://github.com/monosans/dwm
arch=(any)
license=(MIT)
makedepends=(git)
depends=(libx11 libxinerama libxft freetype2)
provides=("${_pkgname}")
conflicts=("${_pkgname}")
source=("${pkgname}::git+${url}.git")
sha256sums=('SKIP')

pkgver() {
	cd "${pkgname}"
	echo "$(awk '/^VERSION =/ {print $3}' config.mk).r$(git rev-list --count HEAD).$(git rev-parse --short HEAD)"
}

prepare() {
	cd "${pkgname}"
	{
		echo "CPPFLAGS+=${CPPFLAGS}"
		echo "CFLAGS+=${CFLAGS}"
		echo "LDFLAGS+=${LDFLAGS}"
	} >>config.mk
}

build() {
	cd "${pkgname}"
	make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11
}

package() {
	cd "${pkgname}"
	make PREFIX=/usr DESTDIR="${pkgdir}" install
	install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
