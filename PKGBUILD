# Maintainer: Roberto Catini <roberto.catini@gmail.com>

pkgname=regetron
pkgver=1.4
pkgrel=1
pkgdesc="A simple shell for playing with regular expressions."
arch=(any)
url="https://gitorious.org/regetron"
license=('custom')
depends=('python2')
makedepends=('git')

package() {
	git clone git://gitorious.org/regetron/regetron.git $pkgname
	cd "$srcdir/$pkgname"
	git checkout 51ae65125c5dc56c8794959802cbc3115411b0ea
	python2 setup.py install --root="$pkgdir/" --optimize=1
	install -D -m644 "$srcdir/$pkgname/LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
