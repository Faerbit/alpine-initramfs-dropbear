# Maintainer: Faerbit <faerbit at gmail dot com>
pkgname=initfs-dropbear
pkgver=0.1
pkgrel=1
pkgdesc="Initfs with support for remote unlocking via ssh"
url="https://github.com/Faerbit/alpine-initramfs-dropbear"
arch="all"
license="MIT"
depends="dropbear mkinitfs=3.3.0"
makedepends="coreutils"
install=""
#source="http://downloads.sourceforge.net/project/$pkgname/$pkgname/$pkgver/$pkgname-$pkgver.tar.gz"
source=("initramfs-init-dropbear"
    "unlock_disk"
    "dropbear.files"
    "dropbear.modules")

build() {
}

package() {
    install -m644 -D "${srcdir}/initramfs-init-dropbear" "${pkgdir}/usr/share/mkinitfs/initramfs-init-dropbear"
    install -m755 -D "${srcdir}/unlock_disk" "${pkgdir}/etc/dropbear/unlock_disk"
    install -m644 -D "${srcdir}/dropbear.files" "${pkgdir}/etc/mkinitfs/features.d/dropbear.files"
    install -m644 -D "${srcdir}/dropbear.modules" "${pkgdir}/etc/mkinitfs/features.d/dropbear.modules"
}

sha512sums="d65a43b834b1926097...c0b8c6017ffc6d9e011217fb7e86e80  gnuplot-4.4.4.tar.gz"
