pkgname=qmidi
pkgdesc="QMidi wrapper for rtmidi"
pkgver=0.1.0
pkgrel=6
arch=("x86_64")
url="https://github.com/OXI-Instruments/QMidi"
license=("GPL3")
depends=("rtmidi")
makedepends=("rtmidi" "cmake" "make" "gcc")
#source=("https://github.com/OXI-Instruments/QMidi")
#sha256sums=("SKIP")

build() {
  mkdir -p ${srcdir}/build
  cd ${srcdir}/build
  cmake -DCMAKE_INSTALL_PREFIX=/usr \
        ${srcdir}/QMidi
  make
}

package() {
  cd ${srcdir}/build
  make DESTDIR="${pkgdir}/" install
}
