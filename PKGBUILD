# Maintainer: Eric Lay <ericlaytm@gmail.com>
pkgname=fuzzy-pokedex-dev
pkgver=r49.aeb1671
pkgrel=1
pkgdesc="A Pokedex for your terminal -DEV VERSION"
arch=('any')
url="https://github.com/ericlay/fuzzy-pokedex"
license=('GPL3')
depends=('fzf'
    'parallel'
    'jq'
    'espeak-ng'
    'pokemon-colorscripts-git'
    'ttf-font-nerd')
makedepends=('git')
source=("git+https://github.com/ericlay/fuzzy-pokedex.git#branch=dev")
md5sums=('SKIP')

pkgver(){
    cd "${pkgname:0:-4}"
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
	cd "$srcdir/${pkgname:0:-4}"
    install -Dm666 pokeData/* -t "$pkgdir/usr/share/$pkgname/pokeData"
    install -Dm666 keybindings-preview -t "$pkgdir/usr/share/$pkgname"
    install -Dm755 pokeParse -t "$pkgdir/usr/bin"
    install -Dm755 pokeUpdate -t "$pkgdir/usr/bin"
	install -Dm755 pokedex-dev -t "$pkgdir/usr/bin"
}
