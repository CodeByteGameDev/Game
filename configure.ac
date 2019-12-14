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

AC_CONFIG_COMMANDS([lclib-c++],[
	mkdir -p lclib-c++
	pushd lclib-c++
	../$ac_top_srcdir/lclib-c++/configure --with-build-type=$build_type
	popd
])

AC_CONFIG_COMMANDS([SDL],[
	mkdir -p SDL
	pushd SDL
	../$ac_top_srcdir/SDL/configure
	popd
])

AC_CONFIG_COMMANDS([pipeworks],[
	mkdir -p pipeworks
	pushd pipeworks
	CPPFLAGS="$CPPFLAGS -I$abs_top_srcdir/SDL/include" LDFLAGS="$LDFLAGS -L$abs_top_builddir/SDL/.libs" ../$ac_top_srcdir/pipeworks/configure --with-build-type=$build_type
	popd
])



AC_OUTPUT
