AC_INIT([TBB-Community-Game], [1.0], [])


AC_CANONICAL_TARGET

AC_PROG_CC
AC_PROG_CXX
AC_PROG_INSTALL

AC_ARG_WITH([build-type],[--with-build-type=<build type>. Allows you to configure the type of build. Defaults to release. Acceptable values are debug, debug-sanitize, and release],
	[
		build_type=$withval
	],
	[
		build_type=release
	])
AC_SUBST([build_type])



shell=/bin/bash
AC_SUBST([shell])

os=${target_os}
AC_SUBST([os])

AC_CONFIG_FILES([Makefile])

AC_OUTPUT
