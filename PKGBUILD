# Contributor: Snorre Jensen snojen@gmail.com

pkgname=openttd-trunk
pkgver=r22729
pkgrel=1
pkgdesc="OpenTTD is an Open Source clone of Transport Tycoon Deluxe"
arch=('i686' 'x86_64')
url="http://www.openttd.org"
license=('GPL')
depends=(libpng sdl fontconfig icu)
makedepends=()
optdepends=('openttd-opengfx: free graphics' 
            'openttd-opensfx: free soundset'
            'openttd-openmsx: free musicset')

source=(http://binaries.openttd.org/nightlies/trunk/${pkgver/_/-}/openttd-trunk-${pkgver/_/-}-source.tar.xz)
md5sums=('a7f10afc387a76cc9d306d433db97ab8')

build() {
    cd $startdir/src/openttd-trunk-${pkgver/_/-}
     
    ./configure \
    --prefix-dir=/usr \
    --binary-dir=bin \
    --binary-name=${pkgname} \
    --data-dir=share/${pkgname} \
    --doc-dir=share/doc/${pkgname} \
    --personal-dir=.${pkgname} \
    --install-dir=$startdir/pkg/ \
    --menu-name="OpenTTD ${pkgver/_/-}"
    make || return 1
    make install || return 1

   cd $pkgdir/usr/share/${pkgname}/data

   ln -s /usr/share/openttd/data/ogfx1_base.grf .
   ln -s /usr/share/openttd/data/ogfxc_arctic.grf .
   ln -s /usr/share/openttd/data/ogfxe_extra.grf .
   ln -s /usr/share/openttd/data/ogfxh_tropical.grf .
   ln -s /usr/share/openttd/data/ogfxi_logos.grf .
   ln -s /usr/share/openttd/data/ogfxt_toyland.grf .
   ln -s /usr/share/openttd/data/opengfx.obg .
   ln -s /usr/share/openttd/data/opensfx.cat .
   ln -s /usr/share/openttd/data/opensfx.obs .

   cd $pkgdir/usr/share/${pkgname}/gm

   ln -s /usr/share/openttd/gm/5432gone_redfarn.mid .
   ln -s /usr/share/openttd/gm/be_sharp_bw_redfarn.mid .
   ln -s /usr/share/openttd/gm/big_man_boogie_redfarn.mid .
   ln -s /usr/share/openttd/gm/boogi_marabi_redfarn.mid .
   ln -s /usr/share/openttd/gm/busy_schedule.mid .
   ln -s /usr/share/openttd/gm/careless_perc_redfarn.mid .
   ln -s /usr/share/openttd/gm/chemistry_lab.mid .
   ln -s /usr/share/openttd/gm/chuggachugga.mid .
   ln -s /usr/share/openttd/gm/city_blues_redfarn.mid .
   ln -s /usr/share/openttd/gm/coconut_run2.mid .
   ln -s /usr/share/openttd/gm/flying_scotsman.mid .
   ln -s /usr/share/openttd/gm/harp_harmony.mid .
   ln -s /usr/share/openttd/gm/linns_basket.mid .
   ln -s /usr/share/openttd/gm/midnight_snow_run.mid .
   ln -s /usr/share/openttd/gm/mighty_giant_run.mid .
   ln -s /usr/share/openttd/gm/modern_motion.mid .
   ln -s /usr/share/openttd/gm/moo_redfarn.mid .
   ln -s /usr/share/openttd/gm/mosey_along_redfarn.mid .
   ln -s /usr/share/openttd/gm/no_work_song_redfarn.mid .
   ln -s /usr/share/openttd/gm/openmsx.obm .
   ln -s /usr/share/openttd/gm/relax_song.mid .
   ln -s /usr/share/openttd/gm/run_for_your_life.mid .
   ln -s /usr/share/openttd/gm/say_what_redfarn.mid .
   ln -s /usr/share/openttd/gm/slow_neasy_redfarn.mid .
   ln -s /usr/share/openttd/gm/the_fast_route.mid .
   ln -s /usr/share/openttd/gm/the_hobo_redfarn.mid .
   ln -s /usr/share/openttd/gm/train_filled_with_cash.mid .
   ln -s /usr/share/openttd/gm/ttsong_iii_imuh3.mid .
   ln -s /usr/share/openttd/gm/ttsong_iv_imuh3.mid .
   ln -s /usr/share/openttd/gm/tttheme2.mid .
   ln -s /usr/share/openttd/gm/ultimate_run.mid .
   ln -s /usr/share/openttd/gm/wood_whistles.mid .

}
