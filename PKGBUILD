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
source=("$pkgname-$pkgver.tar.gz::https://github.com/Inkvisto/cedra-cli/archive/v$pkgver.tar.gz")
sha256sums=('3c4ce63e19fb516147c8d1281bc560099e01d4ea1cd88e6176869d4043421bf3')  # Replace with actual SHA256 checksum

build() {
  cd "$pkgname-$pkgver"
  cargo build --release
}

package() {
  cd "$pkgname-$pkgver"
  install -Dm755 "target/release/cedra-cli" "$pkgdir/usr/bin/cedra-cli"
}
