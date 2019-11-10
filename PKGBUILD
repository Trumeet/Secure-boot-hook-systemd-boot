# Maintainer: YuutaW <i@yuuta.moe>
# Thanks: https://aur.archlinux.org/cgit/aur.git/tree/PKGBUILD?h=systemd-boot-pacman-hook
pkgname=secure-boot-hook-systemd-boot
pkgver=1
pkgrel=1
pkgdesc="Auto sign boot files after upgrading systemd and/or kernel"
arch=("any")
url="https://github.com/Trumeet/Secure-boot-hook-systemd-boot"
license=('GPL')
depends=("linux"
        "systemd")
source=(z-secureboot.hook
        sign-boot)
md5sums=('3a056cc86d60579547c728b6c1a53e6b'
         '32e7f794d9d04e50409a443d1477e41a')

package() {
    install -m755 -d "${pkgdir}/etc/pacman.d/hooks/"
    install -m755 -d "${pkgdir}/usr/bin/"
    install -m644 "${srcdir}/z-secureboot.hook" "${pkgdir}/etc/pacman.d/hooks/"
    install -m755 "${srcdir}/sign-boot" "${pkgdir}/usr/bin/"
}
