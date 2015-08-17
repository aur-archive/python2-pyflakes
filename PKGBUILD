# $Id: PKGBUILD 64234 2012-02-11 00:28:07Z arodseth $
# Maintainer: Thomas Dziedzic < gostrc at gmail >
# Contributor: TDY <tdy@gmx.com>
# Contributor: Tiago Pierezan Camargo <tcamargo@gmail.com>

pkgname=python2-pyflakes
pkgver=0.8
pkgrel=1
pkgdesc='A lint-like tool for Python to identify common errors quickly without executing code'
arch=('any')
url='http://pypi.python.org/pypi/pyflakes'
license=('custom:MIT')
depends=('python2')
provides=('pyflakes')
conflicts=('pyflakes')
replaces=('pyflakes')
source=("http://pypi.python.org/packages/source/p/pyflakes/pyflakes-${pkgver}.tar.gz")
md5sums=('64bbf98be68f2d781bfe2aaa97aa77d0')

build() {
  cd pyflakes-${pkgver}

  python2 setup.py build
}

package() {
  cd pyflakes-${pkgver}

  python2 setup.py install --prefix=/usr --root=${pkgdir} --optimize=1

  install -D -m644 LICENSE \
    ${pkgdir}/usr/share/licenses/pyflakes/LICENSE
}
