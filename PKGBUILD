# Maintainer: filirom1 <filirom1 at gmail dot com>
# Maintainer: Micha Alt <micha.tucker at gmail dot com>

_npmname=brunch
pkgname=nodejs-$_npmname
pkgver=2.0.1
pkgrel=1
pkgdesc="A lightweight approach to building HTML5 applications with emphasis on elegance and simplicity."
arch=('any')
url="http://brunch.io/"
license=('MIT')
depends=('nodejs' )
makedepends=('npm' )
optdepends=()
source=(http://registry.npmjs.org/$_npmname/-/$_npmname-$pkgver.tgz
        'LICENSE')
noextract=($_npmname-$pkgver.tgz)
sha1sums=('d016c1aa7a2400578704b82d512b5473b67cc6e3'
          'de1abc751d24ab2b3ee1dff74f86aeeaee3854b3')

package() {
  install -D -m644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"

  cd "$srcdir"
  local _npmdir="$pkgdir/usr/lib/node_modules/"
  mkdir -p "$_npmdir"
  cd "$_npmdir"
  npm install --user root -g --prefix "$pkgdir/usr" $_npmname@$pkgver
}
