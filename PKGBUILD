# Maintainer: Bruno Goncalves <bigbruno@gmail.com>

pkgname=calamares-biglinux
pkgver=$(date +%y.%m.%d)
pkgrel=$(date +%H%M)
arch=('any')
license=('')
depends=('biglinux-calamares-gnome' 'biglinux-calamares-cutefish' 'biglinux-calamares-lxqt' 'biglinux-calamares-base')
url="https://github.com/biglinux/calamares-biglinux"
pkgdesc="Calamares tweaks to BigLinux, like using btrfs+zstd for default"
source=('https://github.com/Sevenoslinux/calamare-seven')
sha256sums=('SKIP')
makedepends=('git')
install=${pkgname}.install

package() {
    # Verify default folder
    if [ -d "${srcdir}/${pkgname}/${pkgname}" ]; then
        InternalDir="${srcdir}/${pkgname}/${pkgname}"
    else
        InternalDir="${srcdir}/${pkgname}"
    fi


    # Copy files
    if [ -d "${InternalDir}/usr" ]; then
        cp -r "${InternalDir}/usr" "${pkgdir}/"
    fi

    if [ -d "${InternalDir}/etc" ]; then
        cp -r "${InternalDir}/etc" "${pkgdir}/"
    fi

    if [ -d "${InternalDir}/opt" ]; then
        cp -r "${InternalDir}/opt" "${pkgdir}/"
    fi
}

