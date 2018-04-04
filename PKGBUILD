# Maintainer: Yasuo Ozu <yasuo@ozu.email>
pkgname=proxydriver
pkgver=1.0
pkgrel=1
epoch=
pkgdesc="Dynamically change the system proxy setting via NetworkManager"
arch=("x86_64")
url=""
license=('GPLv2')
groups=()
depends=("networkmanager")
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("99-proxydriver.sh" "profile.sh")
md5sums=("SKIP" "SKIP")

prepare() {
	:
}

build() {
	:
}

package() {
	DESTDIR="${pkgdir}"/usr/proxydriver
	HOOKDIR="${pkgdir}"/etc/NetworkManager/dispatcher.d
	mkdir -p "${DESTDIR}"
	mkdir -p "${HOOKDIR}"
	cp -f "${srcdir}/99-proxydriver.sh" "${DESTDIR}"
	cp -f "${srcdir}/profile.sh" "${DESTDIR}"
	ln -snf "${DESTDIR}/99-proxydriver.sh" "${HOOKDIR}/99-proxydriver.sh"
	chmod +x "${HOOKDIR}/99-proxydriver.sh"
}
