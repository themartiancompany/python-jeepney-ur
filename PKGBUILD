# Maintainer: Felix Yan <felixonmars@archlinux.org>

pkgname=python-jeepney
pkgver=0.3.1
pkgrel=1
pkgdesc="Low-level, pure Python DBus protocol wrapper"
url="https://gitlab.com/takluyver/jeepney"
license=('MIT')
arch=('any')
depends=('python')
source=("https://pypi.io/packages/source/j/jeepney/jeepney-$pkgver.tar.gz")
sha512sums=('ad1a2d220a7626a3bdadf6fba6a591d1b498a9f6bb34607860213efddf49bbe67a4dc2d504decd906c560c519302f1fa45b85ba348156e8bec288f525d502e82')

build() {
  cd jeepney-$pkgver
  python setup.py build
}

package() {
  cd jeepney-$pkgver
  python setup.py install --root="$pkgdir" --optimize=1
  install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
}
