# Makefile used by configure to create real Makefile

LIBS = -ldl -lc -lresolv
libdir = @prefix@/lib/torsocks

# Install helper programs
#bin_PROGRAMS = validateconf inspectsocks saveme
#validateconf_SOURCES = validateconf.c common.c parser.c
#validateconf_CFLAGS = $(AM_CFLAGS)

#inspectsocks_SOURCES = inspectsocks.c common.c
#inspectsocks_CFLAGS = $(AM_CFLAGS)

#saveme_SOURCES = saveme.c
#saveme_CFLAGS = $(AM_CFLAGS)

# Install configuration file
usewithtorconfdir = $(CONFDIR)/
usewithtorconf_DATA = torsocks.conf

# Install invocation scripts
bin_SCRIPTS = torsocks usewithtor
INSTALL_SCRIPT = $(install_sh) -c -m 755

# Install man pages
torsocksmanpagedir = $(mandir)/man1
torsocksmanpage_DATA = torsocks.1

torsocks8manpagedir = $(mandir)/man8
torsocks8manpage_DATA = torsocks.8

usewithtormanpagedir = $(mandir)/man1
usewithtormanpage_DATA = usewithtor.1

torsocksconfmanpagedir = $(mandir)/man5
torsocksconfmanpage_DATA = torsocks.conf.5

# Install main library to $(prefix)/lib/tor (must match torsocks.in)
lib_LTLIBRARIES = libtorsocks.la
libtorsocks_la_SOURCES = tsocks.c common.c parser.c dead_pool.c
libtorsocks_la_LDFLAGS = -version-info 1:0:0
#libtorsocks_la_CFLAGS = -nostartfiles

DISTCLEANFILES=parser.lo dead_pool.lo common.lo libtorsocks.lo tsocks.lo \
			   config.cache config.log config.h Makefile \
			   aclocal.m4 config.status usewithtor torsocks \
			   autom4te.cache .libs .deps 
