if XPRINT
XPRINT_SUBDIRS = xprint
endif

SUBDIRS =			\
	$(XPRINT_SUBDIRS)

DIST_SUBDIRS = xprint

relink:
	for i in $(SUBDIRS) ; do $(MAKE) -C $$i relink ; done
