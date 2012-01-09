AC_PREREQ(2.54)
AC_INIT([nss], [3.12])

AC_CONFIG_SRCDIR([mozilla/security/nss/Makefile])

NSPR_PREFIX=$(pkg-config nspr --variable=prefix)
AC_SUBST(NSPR_PREFIX)
NSPR_LIBDIR=$(pkg-config nspr --variable=libdir)
AC_SUBST(NSPR_LIBDIR)

AC_CHECK_SIZEOF(long)
if test x$ac_cv_sizeof_long = x8; then
  USE_64=1
else
  USE_64=
fi
AC_SUBST(USE_64)

AC_CONFIG_FILES([
Makefile
nss.pc
])

AC_OUTPUT
