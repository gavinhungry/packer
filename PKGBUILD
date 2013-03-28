pkgname=packer-gh-git
pkgver=20130328
pkgrel=1
pkgdesc="Bash wrapper for pacman and the AUR"
url="https://github.com/gavinhungry/packer"
license="GPL"
arch=('any')
makedepends=('git')
depends=('grep' 'sed' 'bash' 'curl' 'pacman' 'jshon')
conflicts=('packer')
optdepends=('sudo: install and update packages as non-root'
            'customizepkg: apply customizepkg modifications')
_gitroot='https://github.com/gavinhungry/packer.git'
_gitname='packer'

build() {
  cd "${srcdir}"
  msg "Connecting to github GIT server ..."
  if [ -d ${_gitname} ] ; then
    cd ${_gitname} && git pull origin
    msg "The local files are updated."
  else
    git clone --depth=1 ${_gitroot} ${_gitname}
  fi
}

package() {
  cd "${srcdir}/${_gitname}"
  mkdir -p ${pkgdir}/usr/bin
  mkdir -p ${pkgdir}/usr/share/man/man8
  install -m 755 packer ${pkgdir}/usr/bin/packer
  install -m 644 packer.8 ${pkgdir}/usr/share/man/man8/packer.8
}
