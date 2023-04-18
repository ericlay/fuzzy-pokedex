# Maintainer: Eric Lay <ericlaytm@gmail.com>
pkgname=fuzzy-pokedex-git
_pkgname=fuzzy-pokedex
pkgver=r16.0c9b118
pkgrel=1
pkgdesc="A Pokedex for your terminal"
arch=('any')
url="https://github.com/ericlay/$_pkgname"
license=('GPL3')
depends=('python-beautifulsoup4'
    'fzf'
    'parallel'
    'pokemon-colorscripts-git'
    'ttf-font-nerd')
makedepends=('git')
source=("git+$url.git")
md5sums=('SKIP')

pkgver(){
    cd "$_pkgname"
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
	cd "$srcdir/$_pkgname"
    mkdir -p "$pkgdir/usr/share/$_pkgname/pokeData"
    install -Dm644 pokeData/* -t "$pkgdir/usr/share/$_pkgname/pokeData"
	install -Dm755 fuzzy-pokedex -t "$pkgdir/usr/bin"
	install -Dm755 pokeinfo -t "$pkgdir/usr/bin"
}
