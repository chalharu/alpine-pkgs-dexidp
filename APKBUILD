# Contributor: Mitsuharu Seki <mitsu1986@gmail.com>
# Maintainer: Mitsuharu Seki <mitsu1986@gmail.com>
pkgname=dexidp
pkgver=2.39.1
pkgrel=0
pkgdesc="OpenID Connect (OIDC) identity and OAuth 2.0 provider with pluggable connectors"
url="https://github.com/dexidp/dex"
arch="all"
license="Apache-2.0"
depends=""
makedepends="go"
checkdepends=""
install=""
subpackages="$pkgname-examples:examples"
source="$pkgname-$pkgver.tar.gz::https://github.com/dexidp/dex/archive/refs/tags/v$pkgver.tar.gz"
builddir="$srcdir/dex-$pkgver"

build() {
	make build
	make examples
}

check() {
	# make test
	return 0
}

package() {
	# Replace with proper package command(s)
	install -Dm755 -t "$pkgdir"/usr/bin/ \
		bin/dex
}

examples() {
	cd "$builddir"
	install -Dm755 -t "$subpkgdir"/usr/bin/ \
		bin/example-app \
		bin/grpc-client
}

sha512sums="
ea0d1c817d23252040314a888fc17f56b9666aa37fb903e0cfdb2272948da05abc43a9782c93e288b94010e9f638fdd2d7e975a704d24f7168cd40be663d3083  dexidp-2.39.1.tar.gz
"
