# Maintainer: Bardia Moshiri <fakeshell@bardia.tech>

pkgname=halium10-post-install
pkgver=1$(date +%y%m%d)
pkgrel=3
pkgdesc="Manjaro libhybris Halium 10 post install script"
arch=('any')
url="https://github.com/manjaro-libhybris/halium10-post-install"
license=('GPL')
depends=('gzip' 'glibc-locales' 'wget' 'systemd')
source=("halium10-post-install"
        "halium10-post-install.service"
        "android.conf")
install=$pkgname.install
sha256sums=('e5bc39ff45ad1d29cfa389bc1417df2625e5cd28a863cc45a8db701dc1d96943'
            '89e445612f00b448165453daedd7b2c2fc91bbf9aaf62e95070f3acb0be94849'
            '5571610e4cee293e8776b33ec225ca24af05197cfd7c3ebd3c2e8d830efd55b0')

package() {
    install -Dm755 "${srcdir}/halium10-post-install" -t "${pkgdir}/usr/bin/"
    install -Dm644 "${srcdir}/halium10-post-install.service" -t "${pkgdir}/usr/lib/systemd/system/"
    install -Dm644 "${srcdir}/android.conf" -t "${pkgdir}/usr/lib/sysusers.d/"
}
