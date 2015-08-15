# $Id: PKGBUILD 70879 2012-05-18 11:38:46Z lfleischer $
# Maintainer: Lukas Fleischer <archlinux at cryptocrack dot de>
# Contributor: Alexey Yakovenko <waker@users.sourceforge.net>
#
#	Custom AUR Package Maintainer: Diogo B. <db_eee.at.hotmail.dot.com>

pkgname=deadbeef-gtk3
pkgver=0.5.5
pkgrel=2
pkgdesc='An audio player for GNU/Linux. GTK3 support.'
arch=('i686' 'x86_64')
url='http://deadbeef.sourceforge.net'
license=('GPL2')
depends=('gtk3' 'alsa-lib' 'hicolor-icon-theme' 'desktop-file-utils')
makedepends=('libvorbis' 'libmad' 'flac' 'curl' 'imlib2' 'wavpack' 'libsndfile' 'libcdio' 'libcddb'
             'ffmpeg' 'libx11' 'faad2' 'zlib' 'intltool' 'pkgconfig' 'libpulse' 'libzip'
             'libsamplerate' 'yasm')
optdepends=('libsamplerate: for Resampler plugin'
            'libvorbis: for Ogg Vorbis playback'
            'libmad: for MP1/MP2/MP3 playback'
            'flac: for FLAC playback'
            'curl: for Last.fm scrobbler, SHOUTcast, Icecast, Podcast support'
            'imlib2: for artwork plugin'
            'wavpack: for WavPack playback'
            'libsndfile: for Wave playback'
            'libcdio: audio cd plugin'
            'libcddb: audio cd plugin'
            'ffmpeg: for WMA, AA, OMA, AC, etc.'
            'faad2: for AAC/MP4 support'
            'dbus: for OSD notifications support'
            'pulseaudio: for PulseAudio output plugin'
            'libx11: for global hotkeys plugin'
            'zlib: for Audio Overload plugin'
            'libzip: for vfs_zip plugin')
options=('!libtool')
provides=('deadbeef=0.5.5')
conflicts=('deadbeef')
install='deadbeef.install'
source=("http://downloads.sourceforge.net/project/deadbeef/deadbeef-${pkgver}.tar.bz2")
md5sums=('7cc10cefda0f4044eea897893e4cc1a9')

build() {
  cd "${srcdir}/deadbeef-${pkgver}"

  ./configure --prefix=/usr --enable-gtk3 --disable-gtk2 --disable-ffmpeg
  make
}

package () {
  cd "${srcdir}/deadbeef-${pkgver}"

  make prefix="${pkgdir}/usr" install
}
