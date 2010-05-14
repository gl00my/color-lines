# Contributor: Peter Kosyh <p.kosyhgmail.com>
pkgname=lines
pkgver=0.5
pkgrel=1
pkgdesc="color lines game"
arch=('i686' 'x86_64')
url="http://instead.googlecode.com/"
license=('GPL')

depends=('sdl' 'sdl_image' 'sdl_mixer')
makedepends=( 'pkgconfig' )

source=(http://instead.googlecode.com/files/lines_$pkgver.tar.gz)
md5sums=(54a39c16d42260a17f8fe15e582e946b)

build() {
cd $startdir/src/lines-$pkgver
make BINDIR=/usr/bin/ PREFIX=/usr GAMEDATADIR=/usr/share/color-lines/ || return 1.
make GAMEDATADIR=${startdir}/pkg/usr/share/color-lines/ DESTDIR=${startdir}/pkg PREFIX=/usr BINDIR=${startdir}/pkg/usr/bin/ install
}
