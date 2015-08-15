# Maintainer: Felipe Hommen <felibank at gmail dot com>
# Contributor: moostik <mooostik_at_gmail.com>

pkgname=geogebra
pkgver=4.2.12.0
pkgrel=1
pkgdesc="Dynamic mathematics software with interactive graphics, algebra and spreadsheet"
arch=('any')
url="http://www.geogebra.org/"
license=('custom:GPL3 and CCPL:by-sa')
# Application and source code under GPL / Language files under CCPL:by-sa
depends=('java-runtime' 'shared-mime-info' 'hicolor-icon-theme' 'desktop-file-utils' 'xdg-utils')
optdepends=('kde-thumbnailer-geogebra: generates thumbnails of GeoGebra files in KDE'
	    'gnome-thumbnailer-geogebra: generates thumbnails of GeoGebra files in GNOME'
	    'geogebra-prim: adds a menu entry for the primary school version')
install='geogebra.install'
source=("http://${pkgname}.googlecode.com/files/GeoGebra-Unixlike-Installer-${pkgver}.tar.gz")

package() {
  install -d -m 755 ${pkgdir}/usr/bin
  install -d -m 755 ${pkgdir}/usr/share/applications
  install -d -m 755 ${pkgdir}/usr/share/mime/packages
  install -d -m 755 ${pkgdir}/usr/share/geogebra
  cd "${srcdir}/${pkgname}-${pkgver}"
  sed -i 's/\/usr/\$\{pkgdir\}\/usr/g' install.sh
  source install.sh
  install -D -m 644 _license.txt "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}

md5sums=('0e473d42c07409238a20f67de91fbb39')
