# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Alireza Savand <alireza.savand@gmail.com>

_gemname=lotus-router
pkgname=ruby-$_gemname
pkgver=0.1.1
pkgrel=1
pkgdesc='Ruby HTTP Router for Lotus'
arch=(any)
url='http://lotusrb.org'
license=(MIT)
depends=(ruby ruby-http_router ruby-lotus-utils)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('8e3ed6a71b26c4d4aee6f8140cb1190dd90cb429')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/LICENSE.md" "$pkgdir/usr/share/licenses/$pkgname/LICENSE.md"
}
