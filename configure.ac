# -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([docker-centos], [0.1], [zeroc0d3.team@gmail.com])
AM_INIT_AUTOMAKE([foreign])
AM_MAINTAINER_MODE
AM_EXTRA_RECURSIVE_TARGETS([build pull])

# Checks for programs.
AC_PROG_INSTALL
AC_PROG_MAKE_SET

AC_CHECK_PROG(DOCKER, docker, yes, no)
if test x"$DOCKER" != x"yes" ; then
    AC_MSG_ERROR([required program 'docker' not found])
fi

# Checks for libraries.

# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.

AC_ARG_VAR(TAG, tag of docker images)
AC_MSG_CHECKING([tag of docker images])
if test "x${TAG}" = "x"; then
    AC_SUBST(TAG, latest)
fi
AC_MSG_RESULT([${TAG}])

AC_ARG_VAR(CLEAN_OPTIONS, clean options)
AC_ARG_VAR(BUILD_OPTIONS, build options)
AC_ARG_VAR(PULL_OPTIONS, pull options)

AC_CONFIG_FILES([
    Makefile
    centos-base/Makefile
    centos-base-workspace/Makefile
    centos-application/Makefile
])

AC_OUTPUT
