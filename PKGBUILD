# Maintainer: Silent Robot <d3signr at gmail dot com>

pkgname=salientos-grub-theme
_pkgname=salient
pkgver=1.0
pkgrel=1
pkgdesc='Salient OS - Grub Theme'
arch=('any')
url='https://github.com/salientos/'
license=('GPL3')
makedepends=('git')
optdepends=('grub-customizer: GUI tool to configure GRUB')
provides=("${_pkgname}")
options=(!strip !emptydirs)
source=(${_pkgname}::"git+https://github.com/salientos/${pkgname}.git")
sha256sums=('SKIP')

#pkgver() {
#  cd ${_pkgname}
#  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
#}

package() {
  install -dm755 "${pkgdir}"/usr/share/grub/themes/
  install -Dm644 ${_pkgname}/LICENSE "${pkgdir}/usr/share/licenses/${_pkgname}/LICENSE"
  cp -r --no-preserve=ownership ${_pkgname} "${pkgdir}"/usr/share/grub/themes/
  rm -rf "${pkgdir}"/usr/share/grub/themes/${_pkgname}/.git
  rm "${pkgdir}"/usr/share/grub/themes/${_pkgname}/LICENSE
  rm "${pkgdir}"/usr/share/grub/themes/${_pkgname}/install.sh
}
