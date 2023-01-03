# Maintainer: Eric Torres <erictorres4@protonmail.com>
pkgname=snapraid-helpers
pkgver="1.0.0"
pkgrel=1
pkgdesc="Set of helper units/scripts for snapraid"
arch=(any)
url="https://gist.github.com/gbrks/ec189cc51b3df85189a3"
license=('MIT')
depends=(snapraid)
source=("$pkgname-$pkgver.tar.zst")
sha256sums=('0f0e653690faea0ab87449dd6974b5c34427f094db2e2ddf50afe215fef2fa52')

package() {
	cd "$srcdir"

    for unit in *.{service,timer}; do
        install -Dm644 "$unit" "$pkgdir/usr/lib/systemd/system/${unit##*/}"
    done
}
