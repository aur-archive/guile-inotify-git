pkgname=guile-inotify-git
_gitname=guile-inotify
pkgver=5.646d0ff
pkgrel=1
pkgdesc='guile bindings for linux inotify'
arch=(any)
license=(GPL3)
makedepends=(git)
depends=(guile linux)
conflicts=(guile-inotify)
source=("git://sph.mn/guile-inotify")
url=http://sph.mn/browse/name/guile-inotify/overview
md5sums=(SKIP)

pkgver() {
  cd $_gitname
  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

build() {
  cd $_gitname
  make
}

package() {
  cd $_gitname
  sh setup.sh $pkgdir/usr
}