# Maintainer: Fabian Bornschein <fabiscafe@archlinux.org>
# Maintainer: Jan Alexander Steffens (heftig) <heftig@archlinux.org>
# Contributor: Jan de Groot <jgc@archlinux.org>
# Ported to AcreetionOS by: Johnathan Spiva <sprungles.me@tuta.io>
pkgname=acreetionos-backgrounds
pkgver=0.0.1
pkgrel=1
pkgdesc="Background images and data for AcreetinOS GNOME"
url="https://github.com/Sprunglesonthehub/acreetionos-backgrounds"
arch=(any)
license=(CC-BY-SA-3.0)
depends=(libjxl)
makedepends=(
  glib2
  git
  meson
)
groups=(gnome)
source=("git+https://github.com/Sprunglesonthehub/acreetionos-backgrounds.git")
b2sums=('SKIP')

build() {
  arch-meson $pkgname build
  meson compile -C build
}

check() {
  meson test -C build --print-errorlogs
}

package() {
  meson install -C build --destdir "$pkgdir"
}

# vim:set sw=2 sts=-1 et:
