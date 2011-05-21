## Process this file with automake to produce Makefile.in

fuseincludedir=$(includedir)/fuse

if DARWIN
darwin_headers = fuse_darwin.h
darwin_headers_private = fuse_darwin_private.h
ulockmgr_headers =
else
darwin_headers =
darwin_headers_private =
ulockmgr_headers = ulockmgr.h
endif

fuseinclude_HEADERS = 		\
	$(darwin_headers)		\
	fuse.h					\
	fuse_compat.h			\
	fuse_common.h			\
	fuse_common_compat.h    \
	fuse_lowlevel.h			\
	fuse_lowlevel_compat.h	\
	fuse_opt.h				\
	cuse_lowlevel.h

include_HEADERS = old/fuse.h $(ulockmgr_headers)

noinst_HEADERS = fuse_kernel.h $(darwin_headers_private)
