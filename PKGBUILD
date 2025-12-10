pkgname=xero-gpu-tools
pkgver=1.0
pkgrel=1
pkgdesc="XeroLinux GPU hardware change detection and driver configuration tools"
arch=('any')
license=('GPL')
depends=('bash' 'kdialog' 'konsole' 'pciutils')
install=
source=(
    'xero-gpu-config'
    'xero-gpu-check'
    'xero-gpu-notify.sh'
    'xero-gpu-check.service'
    'xero-gpu-notify.desktop'
)
sha256sums=('SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP')

package() {
    install -Dm755 "${srcdir}/xero-gpu-config" "$pkgdir/usr/bin/xero-gpu-config"
    install -Dm755 "${srcdir}/xero-gpu-check" "$pkgdir/usr/bin/xero-gpu-check"
    install -Dm755 "${srcdir}/xero-gpu-notify.sh" "$pkgdir/usr/bin/xero-gpu-notify"

    # systemd unit
    install -Dm644 "${srcdir}/xero-gpu-check.service" "$pkgdir/usr/lib/systemd/system/xero-gpu-check.service"

    # autostart desktop entry
    install -Dm644 "${srcdir}/xero-gpu-notify.desktop" "$pkgdir/etc/xdg/autostart/xero-gpu-notify.desktop"
}
