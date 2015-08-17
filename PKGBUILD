# Maintainer: Antonio Rojas <nqn1976 @ gmail.com>

pkgname=plasma-applet-calendar
pkgver=0.1.0
pkgrel=2
pkgdesc="A plasmoid for displaying events from Akonadi resources"
arch=('i686' 'x86_64')
url="http://kde-apps.org/content/show.php/Calendar+plasmoid?content=150034"
license=('GPL')
source=('http://kde-apps.org/CONTENT/content-files/150034-calendar_plasmoid.tar.gz')
md5sums=('8f317888f82c684f22cfd261d1c616c8')
depends=('kdebase-workspace' 'akonadi-google')
makedepends=('cmake' 'automoc4' 'boost')
install=$pkgname.install

build() {
  cd $srcdir/calendar
  mkdir build 
  cd build
  cmake -DCMAKE_INSTALL_PREFIX=/usr -DALL_COLLECTIONS=true ..
  make
}

package() {
  cd $srcdir/calendar/build
  make DESTDIR=$pkgdir install
}