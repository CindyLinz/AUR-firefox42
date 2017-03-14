# Maintainer: Cindy Wang (CindyLinz) <cindylinz@github>
#   modified from firefox-developer which is maintained by
#     John D Jones III AKA jnbek <jnbek1972 -_AT_- g m a i l -_Dot_- com>
pkgname=firefox42
pkgdesc="Standalone web browser from mozilla.org, version 42"
url='https://www.mozilla.org/en-US/firefox/42.0/releasenotes/'
pkgver=42.0
pkgrel=1
arch=('i686' 'x86_64')
license=('MPL' 'GPL' 'LGPL')
source=("https://download-installer.cdn.mozilla.net/pub/firefox/releases/$pkgver/linux-$CARCH/en-US/firefox-$pkgver.tar.bz2"
        "firefox42.desktop"
        "vendor.js")
sha512sums=('717e95a8db926d000edb5220b9d63344a4de4cc3d6af2e374d2a39eaf1e873066d7d1b1cef3fa2c744d7587b548035aeefbcaef41478a09012aa3581605d17ec'
            '16e02008fd7d432697b97661ed088e69299be9117913987bddba973f9574fa23430870f8fbfc6fd1e7432ef541f2c0f1462b40e6dd90923579e5fea82d9bbf4e'
            'bae5a952d9b92e7a0ccc82f2caac3578e0368ea6676f0a4bc69d3ce276ef4f70802888f882dda53f9eb8e52911fb31e09ef497188bcd630762e1c0f5293cc010')
depends=('alsa-lib' 'libxt' 'libnotify' 'mime-types' 'nss' 'gtk3' 'sqlite3' 'dbus-glib')

optdepends=('pulseaudio: audio/video playback')

package() {
  install -d $pkgdir/{usr/{bin,share/{applications,pixmaps}},opt}
  cp -r firefox $pkgdir/opt/$pkgname

  ln -s /opt/$pkgname/firefox $pkgdir/usr/bin/$pkgname
  install -m644 $srcdir/firefox42.desktop $pkgdir/usr/share/applications/
  install -m644 $srcdir/firefox/browser/icons/mozicon128.png $pkgdir/usr/share/pixmaps/$pkgname-icon.png
  install -Dm644 $srcdir/vendor.js $pkgdir/opt/$pkgname/browser/defaults/preferences/vendor.js
}

