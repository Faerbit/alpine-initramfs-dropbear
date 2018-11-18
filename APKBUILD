# Maintainer: Faerbit <faerbit@gmail.com>
pkgname=initfs-dropbear
pkgver=3.3.0
pkgrel=1
pkgdesc="Initfs with support for remote unlocking via ssh"
url="https://github.com/Faerbit/alpine-initramfs-dropbear"
arch="noarch"
license="MIT"
depends="dropbear mkinitfs"
makedepends="patch mkinitfs"
install=""
options="!check"
source="initramfs-init-dropbear.patch_ unlock_disk dropbear.files dropbear.modules"
builddir="$srcdir/$pkgname-$pkgver"

build() {
    mkdir -p "$builddir"
    patch /usr/share/mkinitfs/initramfs-init "${srcdir}/initramfs-init-dropbear.patch_" -o "${builddir}/initramfs-init-dropbear"
}

package() {
    install -m755 -D "${builddir}/initramfs-init-dropbear" "${pkgdir}/usr/share/mkinitfs/initramfs-init-dropbear"
    install -m755 -D "${srcdir}/unlock_disk" "${pkgdir}/etc/dropbear/unlock_disk"
    install -m644 -D "${srcdir}/dropbear.files" "${pkgdir}/etc/mkinitfs/features.d/dropbear.files"
    install -m644 -D "${srcdir}/dropbear.modules" "${pkgdir}/etc/mkinitfs/features.d/dropbear.modules"
}

sha512sums="9d88e41dc4807ef38103a64194335b942dc93da65ae22b99e7eab60e069b5c50eba0af14ff881e10a8f98d30af47776d91695f7b9cc0a1b43e2247581a0fb913  initramfs-init-dropbear.patch_
8508508e6dfc09bd4ec3acb5626ea643212d47d776c84b5ca8e8b1a4e3a31288aeee37e8935b0a129a6bad9df1255ee9d918cea030433ba0c71c5818660ffd60  unlock_disk
98fec9927077401c2639d85406f8f1d88708c32795c3ce4eb5f106cba175abf1bb9f4fac56936f6183b61801eb74ccc92b115ff6e622f4e4026d0fadb820ddb8  dropbear.files
79d4687fd8b7a4260dfa16ff0b2f1d4c4bff56e9803cbbe75ea9cc8cc409a154d1ab9981dc86cb4aa6d91eceef4c5d50d9b65622ce547b477f6d97b371fa0783  dropbear.modules"
