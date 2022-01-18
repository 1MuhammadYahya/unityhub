# Maintainer: HunabKu <hunabku@gmx.com>
pkgname=unityhub
pkgver=3.0.0
pkgrel=1
pkgdesc="Unity Hub beta"
arch=('x86_64')
url="https://unity.com/"
license=('custom')
depends=('nss' 'gtk3')
optdepends=('libappindicator-gtk3: The DEB says this an optional dependency')
provides=('unityhub')
install='unityhub.install'
source=(
  "$pkgname-$pkgver.deb::https://hub.unity3d.com/linux/repos/deb/pool/main/u/unity/unityhub_amd64/unityhub-amd64-3.0.0.deb"
  'license.txt'
)
sha256sums=(
  'c358dbbe590a2777719686a26494fee8b55bbcec8a0f4378dccb50715f2a7fde'
  'f0eb3a4bb148bb7f426e4f5b97e891265ac487710cbcba9282518537c7b5d833'
)
OPTIONS=(!strip)

package() {
  tar -xf 'data.tar.bz2' -C "$pkgdir/"
  mkdir -p "$pkgdir/usr/bin"
  ln -sf '/opt/unityhub/unityhub' "$pkgdir/usr/bin/unityhub"

  install -Dm644 "$srcdir/license.txt" "$pkgdir/usr/share/licenses/$pkgname/license.txt"
}
