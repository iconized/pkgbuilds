# Maintainer: Abhiraj Roy <iconized@outlook.in>
pkgname=commitizen-iconized
pkgver=1.0
pkgrel=1
pkgdesc="Command line utility to standardize git commit messages, golang version"
arch=(x86_64)
url="https://github.com/iconized/commitizen-iconized"
license=('GPL')
makedepends=(git go)
source=("https://github.com/iconized/${pkgname}/archive/refs/tags/${pkgver}.tar.gz")

build() {
	cd "$pkgname-$pkgver"
    make
}

package() {
    git_exec_path=$(git --exec-path)
	cd "$pkgname-$pkgver"
    install -Dm755 "$pkgname" "$pkgdir/$git_exec_path/git-cz"
}
