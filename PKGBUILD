# Maintainer: Subash Aryal <blacpythoz@@gmail.com>

pkgname=ttf-nepali-fonts
pkgver=r1.f6e9b4c
pkgrel=1
pkgdesc='A collection of popular Nepali Fonts. Preeti,Himalaya,Kantipur,Sagarmatha etc .'
arch=('any')
url='https://github.com/blacpythoz/nepali-fonts.git'
license=('custom:OFL')
makedepends=('git')
depends=('fontconfig' 'xorg-font-utils')
conflicts=('')
provides=('ttf-nepali-fonts')
source=("git+https://github.com/blacpythoz/nepali-fonts")
md5sums=('SKIP')

pkgver() {
  cd "nepali-fonts"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
  cd "nepali-fonts"
}

package() {
  install -d "${pkgdir}/usr/share/fonts/TTF"
  install -m644 nepali-fonts/fonts/*.ttf "${pkgdir}/usr/share/fonts/TTF/"
  install -d "${pkgdir}/usr/share/licenses/${pkgname}"
  install -m644 nepali-fonts/LICENSE.md "${pkgdir}/usr/share/licenses/${pkgname}/"
}
