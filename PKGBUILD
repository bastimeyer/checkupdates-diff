# Maintainer: Sebastian Meyer <mail@bastimeyer.de>

pkgname=checkupdates-diff
pkgver=1.0.0
pkgrel=1
pkgdesc='Reformats and colorizes the output of the checkupdates utility, similar to yay'
arch=('any')
license=('GPL-3.0-or-later')
depends=(
  'pacman-contrib'
  'expac'
  'gawk'
)
source=(
  "${pkgname}.awk"
)
sha256sums=(
  '62e9dcfaf75232ed0de3b9043c1501b5b0817a742c1affd1b9298eb6166a4aee'
)

package() {
  install -Dm644 "${srcdir}/${pkgname}.awk" "${pkgdir}/usr/share/${pkgname}/${pkgname}.awk"
  install -Dm755 /dev/stdin "${pkgdir}/usr/bin/${pkgname}" <<EOF
#!/usr/bin/env bash
set -eo pipefail
/usr/bin/checkupdates "\${@}" --nocolor | /usr/bin/gawk -f /usr/share/${pkgname}/${pkgname}.awk
EOF
}
