pkgname=netrunner
pkgver=2.0
pkgrel=18
epoch=1
pkgdesc="NetRunner is a telnet client originally developed in the late 90s in sync with the release of Windows XP. It was intended to be a console telnet client which stayed true to ANSI-BBS emulation and the old school feel of DOS terminals. Some features include batch upload/download Zmodem and Zmodem 8K, multiple phone book, mTelnet and SyncTerm phone book importers, original MSDOS and Amiga fonts with font switching, full screen mode, basic scripting language, mouse support, and font UPSCALING that (when enabled) provides the highest quality BBS terminal, even at 2K full screen resolutions! The current release is version 2.0 Beta 18 which is based on the SDL2 graphics engine, providing the most accurate and highest quality ANSI-BBS experience. Optimiziations for CPU usage and speed are still on-going for the beta cycle amd improvements should be seen as versions progress."
url="http://www.mysticbbs.com/"
depends=('sdl')
arch=('i686' 'x86_64')
makedepends=("unrar")
source_i686=("http://www.mysticbbs.com/downloads/nr20b18l.rar")
source_x86_64=("http://www.mysticbbs.com/downloads/nr20b186.rar")
source=("netrunner.sh" "netrunner.desktop")
noextract=("nr20b18l.rar" "nr20b186.rar")
sha256sums_i686=('155e69f98d8f394365cc890d07ddc981be80eaa4a1b171cc133dac21e16b7838')
sha256sums_x86_64=('a76bd19bfe97f708242985595f17fd1d16d7e3ca19fd4f0ea5f1256f48f97abb')
sha256sums=('e1d178f1b3376ddddac2167234d7a4f2cfabba612baf69b746277bdda150ec99'
	'b9e06d3097f4b8ab91709f8fa68826706e5ae961d2443092749ff72d032b3549')

prepare() {
	[[ -n $(uname -a | grep x86_64) ]] && unrar x nr20b186.rar || unrar x nr20b18l.rar
}

package() {
	cd "$srcdir/"

	install -Dm755 netrunner.sh "$pkgdir"/usr/bin/netrunner
	install -Dm644 netrunner.desktop "$pkgdir"/usr/share/applications/netrunner.desktop

	install -Dm755 file_id.diz "$pkgdir"/opt/netrunner/file_id.diz
	install -Dm755 netrunner "$pkgdir"/opt/netrunner/netrunner
	install -Dm755 netrunner.icn "$pkgdir"/opt/netrunner/netrunner.icn
	install -Dm755 netrunner.manual.txt "$pkgdir"/opt/netrunner/netrunner.manual.txt
	install -Dm755 test.scr "$pkgdir"/opt/netrunner/test.scr
	install -Dm755 whatsnew.txt "$pkgdir"/opt/netrunner/whatsnew.txt
}
