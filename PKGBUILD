# Maintainer: Eric Lay <ericlaytm@gmail.com>
pkgname=fuzzy-pokedex
pkgver=r16.0c9b118
pkgrel=1
pkgdesc="A Pokedex for your terminal"
arch=('any')
url="https://github.com/ericlay/fuzzy-pokedex"
license=('GPL3')
depends=('python-beautifulsoup4'
    'fzf'
    'parallel'
    'espeak-ng'
    'pokemon-colorscripts-git'
    'ttf-font-nerd')
makedepends=('git')
source=("git+https://github.com/ericlay/fuzzy-pokedex.git")
md5sums=('SKIP')

pkgver(){
    cd "$pkgname"
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
	cd "$srcdir/$pkgname"
    install -Dm666 pokeData/* -t "$pkgdir/usr/share/$pkgname/pokeData"
	install -Dm755 pokedex -t "$pkgdir/usr/bin"
	install -Dm755 pokeInfo -t "$pkgdir/usr/bin"
}
