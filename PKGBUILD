# Maintainer: YuutaW <i@yuuta.moe>
pkgname=channelbot-git
pkgver=0.0.0.0
pkgrel=1
pkgdesc="forwards the link of a message from a chat to another"
arch=("any")
url="https://github.com/Trumeet/channelbot"
license=('GPL2')
depends=("jq"
		"coreutils"
		"bash")
source=('channelbot'
		'channelbot.conf'
		'channelbot.service')
md5sums=('411c63c64ad8e208dbbab0fd9786a9e1'
         '9d0638dc06d4037adc6316e762c1cf9e'
         'f25e10ca919f556114802934641a154c')
backup=('etc/channelbot.conf')

pkgver() {
	git rev-list --count master
}

package() {
    install -m755 -d "${pkgdir}/usr/bin/"
	install -m755 -d "${pkgdir}/usr/lib/systemd/system"
    install -m755 -d "${pkgdir}/var/lib/channelbot/"
    install -m755 -d "${pkgdir}/etc"
    install -m755 "${srcdir}/channelbot" "${pkgdir}/usr/bin/"
	install -m600 "${srcdir}/channelbot.conf" "${pkgdir}/etc/"
    install -m644 "${srcdir}/channelbot.service" "${pkgdir}/usr/lib/systemd/system/"
}
