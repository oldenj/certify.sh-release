# Maintainer: Jurek Olden <jurek.olden@in.tum.de>

pkgname=certify
pkgver=0.1.5
pkgrel=1
pkgdesc="Simple, easy-to-use helper script for Letsencrypt certification"
url="https://github.com/oldenj/${pkgname}.sh"
depends=("acme-tiny")
license=("GPL3")
arch=("any")
source=("${url}/archive/v${pkgver}.tar.gz")
md5sums=('4cce5f5ac1238c71c4a535b3422bd68b')

package()
{
  cd ${srcdir}/${pkgname}.sh-${pkgver}

  install -Dm755 certify.sh "${pkgdir}/usr/bin/certify"
  install -Dm644 config/openssl.cnf "${pkgdir}/var/lib/${pkgname}/openssl.cnf"
  install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
