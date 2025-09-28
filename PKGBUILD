pkgname=snowfall-ascii
pkgver=1.0
pkgrel=1
pkgdesc="Full screen ASCII snowfall art"
arch=('any')
url="https://example.com"   # optional
license=('GPL')
depends=('bash' 'jp2a' 'coreutils' 'ncurses')

# local files in same folder as PKGBUILD
source=("snowfall" "snowfall.png")
noextract=("snowfall" "snowfall.png")
sha256sums=('SKIP' 'SKIP')   # <--- Add this line

package() {
    # install script to /usr/bin
    install -Dm755 "$srcdir/snowfall" "$pkgdir/usr/bin/snowfall"

    # install image to /usr/share/snowfall-ascii
    install -Dm644 "$srcdir/snowfall.png" "$pkgdir/usr/share/snowfall-ascii/snowfall.png"

    # optional README
    if [[ -f "$srcdir/README.md" ]]; then
        install -Dm644 "$srcdir/README.md" "$pkgdir/usr/share/doc/$pkgname/README.md"
    fi
}
