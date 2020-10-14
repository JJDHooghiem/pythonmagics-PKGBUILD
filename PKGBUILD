pkgname=python-magics
pkgver=1.5.2
pkgrel=1
pkgdesc="magics++ python module"
arch=(any)
license=('APACHE')
depends=('python','magics++')
makedepends=('python-setuptools')
# the blake2-256 is actually part of the link: 
source=("https://files.pythonhosted.org/packages/53/7c/9127b4373219da1dc725f01b55d75a84e4213152379e5ac6634a03fd7fba/Magics-$pkgver.tar.gz")
# can also do md5 sum, this shuould be enough 
sha256sums=('20f6a331b3ffa5c0460fe9273b4d9a32db8a95936759736bef0e393ac1b3817b')

build() {
    cd "$srcdir"/Magics-$pkgver
    python setup.py build
}

package() {
    cd "$srcdir"/Magics-$pkgver
    python setup.py install -O1 --skip-build --root="$pkgdir"
}
