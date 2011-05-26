## Process this file with automake to produce Makefile.in

if DARWIN
AM_CPPFLAGS_DARWIN = -D_POSIX_C_SOURCE=200112L -D__DARWIN_64_BIT_INO_T=1 -O -gdwarf-2
else
AM_CPPFLAGS_DARWIN =
endif

AM_CPPFLAGS = -I$(top_srcdir)/include -D_FILE_OFFSET_BITS=64 -D_REENTRANT $(AM_CPPFLAGS_DARWIN)
noinst_HEADERS = fioc.h
noinst_PROGRAMS = fusexmp fusexmp_fh null hello hello_ll fioc fioclient \
		  fsel fselclient cusexmp

if DARWIN
LDADD = ../lib/libfuse_ino64.la
fusexmp_fh_LDADD = $(LDADD)
else
LDADD = ../lib/libfuse.la
fusexmp_fh_LDADD = ../lib/libfuse.la ../lib/libulockmgr.la
endif

fioclient_CPPFLAGS =
fioclient_LDFLAGS =
fioclient_LDADD =
fselclient_CPPFLAGS =
fselclient_LDFLAGS =
fselclient_LDADD =
