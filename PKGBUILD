pkgname=python-magics
pkgver=1.5.5
pkgrel=1
pkgdesc="magics++ python module"
arch=(any)
license=('APACHE')
depends=('python' 'magics++')
makedepends=('python-setuptools')
# the blake2-256 is actually part of the link: 
source=("https://files.pythonhosted.org/packages/c5/c6/8770a858ddf74bb69e3801a9f2ccf5784fda4d8c5196493aa27882a68fa9/Magics-$pkgver.tar.gz")
# can also do md5 sum, this shuould be enough 
sha256sums=('9709929782b50f27c72c46a22e7cc38a7567d3309a77510a2f9b1194654cc478')

build() {
    cd "$srcdir"/Magics-$pkgver
    python setup.py build
}

package() {
    cd "$srcdir"/Magics-$pkgver
    python setup.py install -O1 --skip-build --root="$pkgdir"
}
