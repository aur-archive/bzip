# Maintainer: Kovivchak Evgen <oneonfire@gmail.com> 

pkgname=bzip
pkgver=0.21
pkgrel=2
pkgdesc="A block-sorting file compressor"
arch=('i686' 'x86_64')
license=('GPL')
url="http://archlinux.org"
depends=('glibc')
source=(${pkgname}-${pkgver}.tar.gz)
md5sums=('03a7fe24ced5ac4401a32092409c78be')

package() {
  cd ${srcdir}/${pkgname}-${pkgver}
  make	  
  install -Dm755 bzip ${pkgdir}/usr/bin/bzip 
  ln -s ${pkgdir}/usr/bin/bzip ${pkgdir}/usr/bin/bunzip
  install -Dm644 ${pkgname}.1 ${pkgdir}/usr/share/man/man1/${pkgname}.1 
  install -Dm644 ${srcdir}/${pkgname}-${pkgver}/LICENSE \
                 ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE 
}

