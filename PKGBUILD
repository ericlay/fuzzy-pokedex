# Maintainer: Eric Lay <ericlaytm@gmail.com>
pkgname=fuzzy-pokedex
pkgver=r38.ba9e1a3
pkgrel=1
pkgdesc="A Pokedex for your terminal"
arch=('any')
url="https://github.com/ericlay/fuzzy-pokedex"
license=('GPL3')
depends=('python-beautifulsoup4'
    'fzf'
    'parallel'
    'jq'
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
    install -Dm666 keybindings-preview -t "$pkgdir/usr/share/$pkgname/"
	install -Dm755 pokedex -t "$pkgdir/usr/bin"
	install -Dm755 pokeInfo -t "$pkgdir/usr/bin"
}
