# Maintainer: Francesco Pira <dev at fpira dot com>

pkgname=poof-bin
pkgver=0.6.0
pkgrel=1
pkgdesc="Magic manager of pre-built software (Prebuilt Binary)"
url="https://github.com/pirafrank/poof"
license=('MIT')
provides=('poof')
conflicts=('poof')

# List ALL Arch-compatible architectures you support
arch=('x86_64' 'aarch64')

# Dynamic source URL selection based on the build architecture
source_x86_64=("${url}/releases/download/v${pkgver}/poof-${pkgver}-x86_64-unknown-linux-gnu.tar.gz")
sha256sums_x86_64=('11ba94a2a6e879f1b531efacb10f6519192a46b77cd01f81898d6793d76231a2')

source_aarch64=("${url}/releases/download/v${pkgver}/poof-${pkgver}-aarch64-unknown-linux-gnu.tar.gz")
sha256sums_aarch64=('813f0f4444e632782b7c36bcc7b2f3e69d7eb73dbfd191407ec3e44570f4dc97')

package() {
    # Arch automatically downloads only the source_CARCH file
    # But it puts it in srcdir, so you might need a wildcard or specific logic if filenames differ

    install -Dm755 "${srcdir}/poof" "${pkgdir}/usr/bin/poof"
}