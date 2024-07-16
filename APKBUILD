# Contributor: Mitsuharu Seki <mitsu1986@gmail.com>
# Maintainer: Mitsuharu Seki <mitsu1986@gmail.com>
pkgname=dexidp
# renovate: datasource=github-tags depName=dexidp/dex
pkgver=2.40.0
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
65b23c7d1a85431083e3ae68312a89273cc658d88cb0e93a10897e8521984bea6af6fab3a6e9b1507293d894ba3eed27a8790464deaf67af34d98436183266e1  dexidp-2.40.0.tar.gz
"
