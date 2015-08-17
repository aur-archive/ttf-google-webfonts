# Maintainer: Sarkasper <echo a2FzcGVyLm1lbnRlbkBnbXguY29tCg== | base64 -d>
# Contributor: Daniel Micay <danielmicay@gmail.com>
# Contributor: Michalis Georgiou <mechmg93@gmail.comr>
# Contributor: Alexander De Sousa <archaur.xandy21@spamgourmet.com>

pkgname=ttf-google-webfonts
pkgver=130325
pkgrel=1
pkgdesc="Google Web Fonts catalogue."
arch=('any')
url="http://code.google.com/p/googlefontdirectory/issues/detail?id=2"
license=('various')
depends=('fontconfig' 'xorg-fonts-encodings')
conflicts=('googlefontdirectory'
           'jsmath-fonts'
           'lohit-fonts'
           'oldstand-font'
           'sintony'
           'otf-goudy'
           'ttf-andika'
           'ttf-anonymous-pro'
           'ttf-cantarell'
           'ttf-cardo'
           'ttf-chromeos-fonts'
           'ttf-droid'
           'ttf-google-webfonts-hg'
           'ttf-inconsolata'
           'ttf-kimberly_geswein_print'
           'ttf-nova'
           'ttf-oldstandard'
           'ttf-oxygen'
           'ttf-pt-mono'
           'ttf-pt-sans'
           'ttf-ptsans'
           'ttf-roboto'
           'ttf-sil-fonts'
           'ttf-sortsmillgoudy'
           'ttf-source-code-pro'
           'ttf-source-sans-pro'
           'ttf-ubuntu-font-family'
           'ttf-vollkorn')
provides=("${conflicts[@]}")
install=font.install
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/w0ng/googlefontdirectory/archive/master.tar.gz")
md5sums=('d133fc4b8c9f767436470b175d0a9b1a')

package() {
  cd "$srcdir"
  install -dm755 "$pkgdir/usr/share/fonts/TTF"
  find . -type f -name \*.ttf -exec install -Dm644 '{}' \
    "$pkgdir/usr/share/fonts/TTF" \;
}
