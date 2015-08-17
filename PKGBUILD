# Contributor: Magnus Woldrich <magnus@trapd00r.se>
# Generator  : CPANPLUS::Dist::Arch 1.10
pkgname='perl-file-lscolor'
pkgver='0.170'
pkgrel='1'
pkgdesc="Colorize input filenames just like ls does"
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl-term-extendedcolor')
makedepends=()
url='http://search.cpan.org/dist/File-LsColor'
source=('http://search.cpan.org/CPAN/authors/id/W/WO/WOLDRICH/File-LsColor-0.124.tar.gz')
md5sums=('56fdee73903c2ef431b1ea01d48d3bad')

build() {
  PERL=/usr/bin/perl
  DIST_DIR="${srcdir}/File-LsColor-0.124"
  export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
    PERL_AUTOINSTALL=--skipdeps                            \
    PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
    PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
    MODULEBUILDRC=/dev/null

  { cd "$DIST_DIR" &&
    $PERL Makefile.PL &&
    make &&
    make test &&
    make install;
  } || return 1;

  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}
