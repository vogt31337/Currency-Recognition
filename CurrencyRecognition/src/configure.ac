#                    -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([CurrencyRecognition], [1.1], [carloscosta.cmcc@gmail.com])
AM_INIT_AUTOMAKE
AC_CONFIG_MACRO_DIR(m4)

# AC_CONFIG_SRCDIR([Configs.h])
# AC_CONFIG_HEADERS([config.h])

# Checks for programs.
AC_PROG_CXX
AC_PROG_CC

# Checks for libraries.
#AC_CHECK_LIB(opencv)
PKG_CHECK_MODULES(OPENCV, [opencv >= 2.0], [], [AC_MSG_ERROR("opencv not found")])

# Checks for header files.
AC_CHECK_HEADERS([stdlib.h sys/time.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_CHECK_HEADER_STDBOOL
AC_TYPE_SIZE_T

# Checks for library functions.
AC_CHECK_FUNCS([gettimeofday pow sqrt])

AC_CONFIG_FILES([Makefile CLI/Makefile GUI/Makefile ImageAnalysis/Makefile libs/Makefile libs/Transformations/Makefile])

AC_OUTPUT
