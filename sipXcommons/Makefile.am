include config/project.am

@PACKAGE@_EXTRA_DIST = \
   @PACKAGE@-rpmlintrc \
   config.properties.in \
   lib \
   src

SUBDIRS = \
   . \
   src

# BUILT_SOURCES is special autoconf variable to be checked on every make
BUILT_SOURCES = config.properties

config.properties : config.properties.in Makefile
	@echo "Localize $< -> $@"
	@$(LocalizeSipXconfig) $(srcdir)/config.properties.in > $(top_builddir)/config.properties
