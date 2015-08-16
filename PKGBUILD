# Maintainer: Evgeniy Ka. <genues@mail.ru>
pkgname=licq-plugin-jabber
pkgver=1.8.2
pkgrel=5
pkgdesc="Jabber plugin for Licq"
arch=('any')
license=('GPL')
url="http://licq.org"
depends=('licq' 'gloox')
makedepends=('boost' 'cmake')
source="http://downloads.sourceforge.net/licq/licq-${pkgver}.tar.bz2"
sha256sums=('16aa514888379a12f538becbaeb81f77017d05c94c15f3b2a5e0ffb60315180f')

build() {

	cd licq-${pkgver}/plugins/jabber/src
	cmake -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_MODULE_PATH="${srcdir}/licq-${pkgver}/cmake" ..
	make

}

package() {
	cd licq-${pkgver}/plugins/jabber/src
	make DESTDIR="${pkgdir}" install
}

