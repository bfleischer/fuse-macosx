## Process this file with automake to produce Makefile.in

ACLOCAL_AMFLAGS = -I m4

SUBDIRS = @subdirs2@

if DARWIN
extra_pkgconfig = fuse.pc.in fuse_ino64.pc.in
else
extra_pkgconfig = fuse.pc.in
endif

EXTRA_DIST =			\
	$(extra_pkgconfig)	\
	README*			\
	Filesystems		\
	FAQ			\
	doc/how-fuse-works	\
	doc/kernel.txt		\
	doc/Doxyfile

pkgconfigdir = @pkgconfigdir@
if DARWIN
pkgconfig_DATA = fuse.pc fuse_ino64.pc
else
pkgconfig_DATA = fuse.pc
endif

$(pkgconfig_DATA): config.status
