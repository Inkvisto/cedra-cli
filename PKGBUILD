# Maintainer: Your Name <qwertuasdfgh@gmail.com>
pkgname=cedra-cli
pkgver=1.0.0
pkgrel=1
pkgdesc="A CLI tool for cedra"
arch=('x86_64')  # or 'any' if architecture-independent
url="https://github.com/Inkvisto/cedra-cli"
license=('MIT')  # Change to correct license
depends=()      # Add dependencies (e.g., 'rust' if compiled)
makedepends=('cargo' 'git')  # For Rust projects
source=("https://github.com/Inkvisto/cedra-cli/archive/refs/tags/v1.0.0.tar.gz")
sha256sums=('2ee44cdcda843843052352cdac2e5c10222cca9495637ebc72ecc5b5f9386396')  # Replace with actual SHA256 checksum

build() {
  cd "$pkgname-$pkgver"
  cargo build --release
}

package() {
  cd "$pkgname-$pkgver"
  install -Dm755 "target/release/cedra-cli" "$pkgdir/usr/bin/cedra-cli"
}
