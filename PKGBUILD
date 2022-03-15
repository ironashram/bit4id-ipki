pkgname=bit4id-ipki
pkgver=1.4.10.622
pkgrel=1
pkgdesc="Bit4ID Universal Middleware (Smart Card driver)"
arch=('x86_64')
license=('unknown')
url="http://www.bit4id.com/"
install=$pkgname.install
options=('!strip')

ARCH='amd64'
md5sums=('1a65703ee7298e21842041a722ee4831')

_file_name='libbit4xpki-idemia-'$ARCH'.1.4.10-622.deb'
source=('https://swdownload1.agenziaentrate.gov.it/pub/sanita/'$_file_name)

package() {
        ar -xv $_file_name || return 1
        tar -xvf data.tar.[xg]z -C $pkgdir || return 1

        # Delete the graphical "Bit4id PKI Manager" utility, etc.
        # We only retain the actual driver (usr/lib).
        # rm -rf $pkgdir/usr/share
}
