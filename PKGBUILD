pkgname="wretch"
pkgver="nightly"
pkgrel=1
pkgdesc="A simple Fetch CLI program Built with Rust"
arch=("x86_64")
source=("$pkgname-nightly.tar.gz::https://github.com/addy10s/wretch/archive/refs/tags/nightly.tar.gz")
url="https://github.com/addy10s/wretch"
makedepends=("rustup" "git")
sha512sums=("SKIP")
license=("GPL3")
build() {
    cd "${srcdir}/$pkgname-nightly"
    cargo build --release
}
package() {
    cd "${srcdir}/$pkgname-nightly"
    mkdir -p "${pkgdir}/usr/bin"
    cp target/release/wretch "${pkgdir}/usr/bin/"
    chmod +x "${pkgdir}/usr/bin/wretch"
}