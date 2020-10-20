pkgname=python-magics
pkgver=1.5.3
pkgrel=1
pkgdesc="magics++ python module"
arch=(any)
license=('APACHE')
depends=('python' 'magics++')
makedepends=('python-setuptools')
# the blake2-256 is actually part of the link: 
source=("https://files.pythonhosted.org/packages/b9/a5/59c2776235987a898c1f8c265268be31590d78245bbfcf879409f267991c/Magics-$pkgver.tar.gz")
# can also do md5 sum, this shuould be enough 
sha256sums=('b0e2da0ec005c3628c66e51f7ba5fbc047e6198ff523d485edf02ffa125c81b6')

build() {
    cd "$srcdir"/Magics-$pkgver
    python setup.py build
}

package() {
    cd "$srcdir"/Magics-$pkgver
    python setup.py install -O1 --skip-build --root="$pkgdir"
}
