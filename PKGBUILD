# Maintainer: Yurii Kolesnykov <root@yurikoles.com>
# Contributor: Brenton Horne <brentonhorne77 at gmail dot com>
# Contributor: Johannes Dewender arch at JonnyJD dot net
# Contributor: Andrea Scarpino <andrea@archlinux.org>
#
# Pull Requests are welcome here: https://github.com/yurikoles-aur/obs-service-format_spec_file

_servicename=format_spec_file
pkgname=obs-service-"${_servicename}"
_pkgver=20240121
_subpkgver=1.4
pkgver="${_pkgver}.${_subpkgver}"
_susepkgver="${_pkgver}-${_subpkgver}"
pkgrel=1
pkgdesc='An OBS source service: reformats a spec file to SUSE standard'
arch=('any')
url='https://github.com/openSUSE/obs-service-format_spec_file'
license=('GPL-2.0-only')
depends=('obs-service-source_validator')
source=("https://download.opensuse.org/source/tumbleweed/repo/oss/src/${pkgname}-${_susepkgver}.src.rpm")
sha256sums=('b63d605749109b88a789ed7313a35b646f121345b71888767e1446f52f27b538')

prepare() {
  bsdtar -xf "${pkgname}-${_pkgver}.tar.bz2"
}


package() {
  cd "${pkgname}-${_pkgver}"
  make DESTDIR="${pkgdir}" install
}
