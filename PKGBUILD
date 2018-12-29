# Maintainer: Jurek Olden <jurek.olden@in.tum.de>

pkgname=certify
pkgver=0.1.1
pkgrel=1
provides=("${pkgname}")
conflicts=("${pkgname}")
pkgdesc="Simple, easy-to-use helper script for Letsencrypt certification"
url="https://github.com/oldenj/${pkgname}.sh"
arch=("any")
license=("GPL3")
depends=("curl")
source=("${url}/archive/v${pkgver}.tar.gz")
md5sums=('c8422da2202710a72526b13120ca7520')

package()
{
  cd ${srcdir}/${pkgname}.sh-${pkgver}
  install -dm755 "${pkgdir}/usr/bin"
  install -dm755 "${pkgdir}/var/lib/$pkgname"
  install -dm755 "${pkgdir}/usr/share/licenses/$pkgname"


  install -Dm755 "${pkgname}.sh" \
    "${pkgdir}/usr/bin/${pkgname}"
  install -Dm755 "config/openssl.cnf" \
    "${pkgdir}/var/lib/${pkgname}/openssl.cnf"
  install -Dm755 "LICENSE" \
    "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
