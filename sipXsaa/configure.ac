AC_PREREQ(2.57)
AC_INIT(sipXsaa, 0.0.4.5.2, sipx-dev@list.sipfoundry.org)
AC_CONFIG_AUX_DIR(config)
m4_include([config/general.m4])
m4_include([config/sipXlib.m4])
SFAC_STRICT_COMPILE_NO_WARNINGS_ALLOWED
AM_INIT_AUTOMAKE(foreign tar-ustar)
SFAC_AUTOMAKE_VERSION([1.6])
AM_CONFIG_HEADER([src/config.h])
AC_PROG_LIBTOOL
AC_PATH_PROG([BASH], [bash])
AC_PATH_PROG([PERL], [perl])
AC_PROG_CXX
AX_COMPILER_VENDOR
AC_PROG_CC
CHECK_XARGS_REPLACE
CHECK_APACHE2
CHECK_SELINUX
CHECK_XARGS_REPLACE
SFAC_LIB_COMMSERVER
SFAC_LIB_CALL
SFAC_LIB_MEDIA
SFAC_LIB_STACK
CHECK_GIPSNEQ
CHECK_JDK
CHECK_ANT
AC_ARG_WITH([dailydir],
  AC_HELP_STRING([--with-dailydir=directory],
    [The directory containing scripts that are run every night]),
  [DAILYDIR=${withval}],[DAILYDIR='$(sysconfdir)/cron.daily'])
AC_SUBST([DAILYDIR])
CHECK_POSTGRES
CHECK_SERVICEDIR
AC_CONFIG_FILES([Makefile])
AC_CONFIG_FILES([src/Makefile])
AC_CONFIG_FILES([src/test/Makefile])
AC_CONFIG_FILES([etc/Makefile])
AC_CONFIG_FILES([bin/Makefile])
AC_CONFIG_FILES([meta/Makefile])
AC_OUTPUT
