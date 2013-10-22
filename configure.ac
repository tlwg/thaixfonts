AC_PREREQ(2.59)

AC_INIT(thaixfonts, 1.2.6svn, thai-linux-foss-devel@googlegroups.com)
AC_CONFIG_SRCDIR([thai.alias])
AM_INIT_AUTOMAKE(dist-xz no-dist-gzip)

AC_PROG_INSTALL
AC_PROG_LN_S
AC_CHECK_PROGS(RMDIR,rmdir,no)

AC_CHECK_PROGS(BDFTOPCF,bdftopcf,no)
if test "x$BDFTOPCF" = "xno" ; then
  AC_MSG_ERROR([You need bdftopcf (from xfonts-utils)])
fi
AC_CHECK_PROGS(MKFONTDIR,mkfontdir,no)
if test "x$MKFONTDIR" = "xno" ; then
  AC_MSG_ERROR([You need mkfontdir (from xfonts-utils)])
fi
AC_CHECK_PROGS(GZIP,gzip,no)
if test "x$GZIP" = "xno" ; then
  AC_MSG_ERROR([You need gzip (from gzip distribution)])
fi

AC_ARG_WITH(fontdir,
  [AC_HELP_STRING([--with-fontdir=DIR],
                  [font directory in DIR [PREFIX/share/fonts/X11/misc]])],
  [fontdir="$withval"], [fontdir=\$\{datadir\}/fonts/X11/misc])
AC_MSG_CHECKING(--with-fontdir)
AC_MSG_RESULT("$fontdir")                                                                                                           
AC_SUBST(fontdir)

MRULE=$srcdir/Make.rule
AC_SUBST_FILE(MRULE)

AC_OUTPUT(
  Makefile
  etlthai/Makefile
  manop/Makefile
  nectec/Makefile
  poonlap/Makefile
  yenbut/Makefile
  thaixfonts.spec
)

