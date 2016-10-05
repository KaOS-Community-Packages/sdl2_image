pkgname=sdl2_image
pkgver=2.0.1
pkgrel=1
pkgdesc="A simple library to load images of various formats as SDL surfaces"
arch=('x86_64')
license=('custom')
depends=('sdl2' 'libpng' 'libjpeg-turbo' 'libtiff' 'zlib')
options=('!libtool')
url="http://www.libsdl.org/projects/SDL_image/"
source=("http://192.241.223.99/projects/SDL_image/release/SDL2_image-$pkgver.tar.gz")
md5sums=('d94b94555ba022fa249a53a021dc3606')

build() {
  cd "${srcdir}/SDL2_image-$pkgver"
  
  ./configure --prefix=/usr --disable-static
  make 
}

package() {
  cd "${srcdir}/SDL2_image-$pkgver"
  
  make DESTDIR=${pkgdir} install
  install -Dm644 COPYING.txt "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
