# Contributor: Ralf Schmitt <ralf@systemexit.de>
# Last changed: 2014-01-11 by evilgnome

pkgname=python-greenlet
pkgver=0.4.2
pkgrel=1
pkgdesc="Lightweight in-process concurrent programming"
license=("MIT")
url="http://pypi.python.org/pypi/greenlet"
depends=('python')
source=(http://pypi.python.org/packages/source/g/greenlet/greenlet-$pkgver.zip)
arch=('i686' 'x86_64')
sha512sums=('9596b740921e4a80bcb43adb725a7a4ea428dadc10ba55f8840837ba685b010c273a4a2bd62c5ba4bfdf27ce87c914a83714d762bacafb8e0a3cd7e2a9675992')

build() {
  cd greenlet-$pkgver
  python setup.py build
}

package() {
  cd greenlet-$pkgver
  python setup.py install --root="$pkgdir"
  install -Dm0644 LICENSE.PSF "$pkgdir/usr/share/licenses/$pkgname/LICENSE.PSF"
}
