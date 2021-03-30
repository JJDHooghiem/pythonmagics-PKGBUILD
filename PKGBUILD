pkgname=python-magics
pkgver=1.5.6
pkgrel=1
pkgdesc="magics++ python module"
arch=(any)
license=('APACHE')
depends=('python' 'magics++')
url="https://pypi.org/project/Magics/"
makedepends=('python-setuptools')
# the blake2-256 is actually part of the link: 
source=("https://files.pythonhosted.org/packages/34/71/a8e8c413525b7be131dc4b421ce0c19493989b4fff6f3929e2b5e1fcf75e/Magics-$pkgver.tar.gz")
# can also do md5 sum, this shuould be enough 
sha256sums=('ffb759e82577925f7ac790b59a5a467d0dabf2e655aa5fa89726160869f6b50b')

build() {
    cd "$srcdir"/Magics-$pkgver
    python setup.py build
}

package() {
    cd "$srcdir"/Magics-$pkgver
    python setup.py install -O1 --skip-build --root="$pkgdir"
}
