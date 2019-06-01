pkgname=netrunner
pkgver=2.0
pkgrel=18
epoch=1
pkgdesc="NetRunner is a telnet client originally developed in the late 90s in sync with the release of Windows XP. It was intended to be a console telnet client which stayed true to ANSI-BBS emulation and the old school feel of DOS terminals. Some features include batch upload/download Zmodem and Zmodem 8K, multiple phone book, mTelnet and SyncTerm phone book importers, original MSDOS and Amiga fonts with font switching, full screen mode, basic scripting language, mouse support, and font UPSCALING that (when enabled) provides the highest quality BBS terminal, even at 2K full screen resolutions! The current release is version 2.0 Beta 18 which is based on the SDL2 graphics engine, providing the most accurate and highest quality ANSI-BBS experience. Optimiziations for CPU usage and speed are still on-going for the beta cycle amd improvements should be seen as versions progress."
url="http://www.mysticbbs.com/"
depends=('sdl')
arch=('x86_64')
source=("http://www.mysticbbs.com/downloads/nr20b186.rar"
	"netrunner.sh"
	"netrunner.desktop")
sha256sums=('a76bd19bfe97f708242985595f17fd1d16d7e3ca19fd4f0ea5f1256f48f97abb'
	'd45e894523358bc29a2a8d119342e650a0bb13ef7031e3da5b3b12352f8f0501'
	'a52e3ad096bd27c0dfb87d0570393587652c946100624963b96541dcf0275d36')

package() {
	cd "srcdir/"
	install -Dm755 netrunner.sh "$pkgdir"/usr/bin/netrunner
	install -Dm644 netrunner.desktop "$pkgdir"/usr/share/applications/netrunner.desktop
	install -dm755 "$pkgdir"/opt/netrunner
}
