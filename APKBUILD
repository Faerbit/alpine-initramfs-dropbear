# Maintainer: Faerbit <faerbit@gmail.com>
pkgname=initfs-dropbear
pkgver=0.1
pkgrel=1
pkgdesc="Initfs with support for remote unlocking via ssh"
url="https://github.com/Faerbit/alpine-initramfs-dropbear"
arch="noarch"
license="MIT"
depends="dropbear dropbear-convert mkinitfs"
makedepends="coreutils"
install=""
options="!check"
#source="http://downloads.sourceforge.net/project/$pkgname/$pkgname/$pkgver/$pkgname-$pkgver.tar.gz"
source="initramfs-init-dropbear unlock_disk dropbear.files dropbear.modules"

build() {
    return 0
}

package() {
    install -m644 -D "${srcdir}/initramfs-init-dropbear" "${pkgdir}/usr/share/mkinitfs/initramfs-init-dropbear"
    install -m755 -D "${srcdir}/unlock_disk" "${pkgdir}/etc/dropbear/unlock_disk"
    install -m644 -D "${srcdir}/dropbear.files" "${pkgdir}/etc/mkinitfs/features.d/dropbear.files"
    install -m644 -D "${srcdir}/dropbear.modules" "${pkgdir}/etc/mkinitfs/features.d/dropbear.modules"
}

sha512sums="c4d269f19234f620991ce2915cd6a9ded91d2aa0da9a259849996d04b734009cb23c16f2821314d2c81d07990d20310fd75524b4a88d0a7258dfd132742ebeba  initramfs-init-dropbear
fd9cc2f2816e44faa1ada14e48d9dc974955aa1eef14e82b678b2e94652d6ac22bda42eb3b5c0a52ad63e43931cfa0903f3829bf334fbf45cf5c81e2a8f64d9a  unlock_disk
98fec9927077401c2639d85406f8f1d88708c32795c3ce4eb5f106cba175abf1bb9f4fac56936f6183b61801eb74ccc92b115ff6e622f4e4026d0fadb820ddb8  dropbear.files
79d4687fd8b7a4260dfa16ff0b2f1d4c4bff56e9803cbbe75ea9cc8cc409a154d1ab9981dc86cb4aa6d91eceef4c5d50d9b65622ce547b477f6d97b371fa0783  dropbear.modules"
