# additional include paths necessary to compile the C++ library
SUBDIRS = Grid
if ENABLE_HMC
SUBDIRS += HMC
endif
if ENABLE_TESTS
SUBDIRS += benchmarks tests
endif

include $(top_srcdir)/doxygen.inc

bin_SCRIPTS=grid-config

.PHONY: bench check tests doxygen-run doxygen-doc $(DX_PS_GOAL) $(DX_PDF_GOAL)

tests-local: all
bench-local: all
check-local: all

AM_CXXFLAGS += -I$(top_builddir)

ACLOCAL_AMFLAGS = -I m4
