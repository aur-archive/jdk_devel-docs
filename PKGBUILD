# Maintainer: Det <nimetonmaili g-mail>

pkgname=jdk-devel-docs
_major=9
#_minor=none
_build=b48
_date=28_jan_2015
_date_fx=27_jan_2015
pkgver=${_major}${_build}
#pkgver=${_major}u${_minor}.${_build}
pkgrel=1
pkgdesc="Oracle Java $_major Development Kit Snapshot - Documentation"
arch=('any')
url="https://jdk$_major.java.net/"
license=('custom:Oracle')
options=('!strip')
optdepends=('java-environment>=$_major: Compile and run the examples')
source=('http://download.java.net/jdk$_major/archive/$_build/binaries/jdk-$_major-ea-docs-$_build-all-$_date.zip'
        'http://download.java.net/jdk$_major/archive/$_build/binaries/javafx-$_major-ea-apidocs-$_build-$_date_fx.zip'
        'LICENSE')
md5sums=('3276e2c72e717fcc34646a3a059b3b8f'
         '6c68d681ad1e6b4952d1734a9ab26e0f'
         'f09947a67691a2d78d20a3885889981c')

package() {
  # JDK Docs
  mkdir -p "$pkgdir"/usr/share/doc/java$_major/
  mv docs/* "$pkgdir"/usr/share/doc/java$_major/

  # JavaFX Docs
  mv api "$pkgdir"/usr/share/doc/java$_major/javafx/

  # License
  install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
}
