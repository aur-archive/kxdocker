# Contributor: Sergej Pupykin <pupykin.s+arch@gmail.com>
# Contributor: Dario Mango <dario.mango@gmail.com>

pkgname=kxdocker
pkgver=1.1.4a
pkgrel=2
pkgdesc="A KDE animated docker, supports plugins and notifications"
arch=('i686' 'x86_64')
url="http://www.xiaprojects.com/www/prodotti/kxdocker/main.php"
license=("GPL")
depends=('kdelibs3')
options=('libtool')
source=(http://www.xiaprojects.com/downloads/KXDocker/sources/1.0.0/$pkgname-$pkgver.tar.bz2)
md5sums=('593a814b9ffde8d010a02498d6e32f2b')

build() {
  cd $srcdir/$pkgname-$pkgver

  export PATH=/opt/qt:$PATH

  ./configure --disable-debug --without-arts --prefix=/opt/kde
  make || return 1
  make DESTDIR=$pkgdir install
}
