include config/project.am

SUBDIRS = \
	. \
	src \
	bin \
	meta \
	etc

editscripts_IN = \
    bin/sipxsaa.sh.in

editscripts :
	@for f in $(editscripts_IN); \
	do \
	  target=`basename $$f .in`; \
          $(LocalizeSipXconfig) $(srcdir)/$$f > $$target; \
	  $(INSTALL) -D -m 755 $$target $(DESTDIR)$(bindir)/$$target; \
	done
