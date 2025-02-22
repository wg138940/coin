# Copyright (C) 2006 International Business Machines.
# All Rights Reserved.
# This file is distributed under the Eclipse Public License.

## $Id: configure.ac 533 2020-01-31 10:19:07Z stefan $

# Author:  Andreas Waechter            IBM    2006-04-13

#############################################################################
#                       Names and other basic things                        #
#############################################################################

AC_PREREQ(2.59)

AC_INIT([DataMiplib3],[1.2.8],[https://projects.coin-or.org/BuildTools/])

AC_COPYRIGHT([
Copyright 2006 International Business Machines and others.
All Rights Reserved.
This file is part of the open source package Coin which is distributed
under the Eclipse Public License.])

# List one file in the package so that the configure script can test
# whether the package is actually there
AC_CONFIG_SRCDIR(configure.ac)

# Where should everything be installed by default?  Here, we want it
# to be installed directly in 'bin', 'lib', 'include' subdirectories
# of the directory where configure is run.  The default would be
# /usr/local.
AC_PREFIX_DEFAULT([`pwd`])

AC_COIN_PROJECTDIR_INIT(DataMiplib3,2:8:1)

#############################################################################
#     We only need automake to generate Makefiles for the distribution      #
#############################################################################

# Initialize automake
AC_COIN_INIT_AUTOMAKE

# check if ZLIB is available, in which case we do not decompress
AC_COIN_CHECK_GNU_ZLIB

#############################################################################
#Find out what the data files are and create links if this is a VPATH config#
#############################################################################

AC_COIN_EXAMPLE_FILES([*.gz miplib3.cat])

##############################################################################
#                   Finishing up by writing all the output                   #
##############################################################################

ABSBUILDDIR="`pwd`"
AC_SUBST(ABSBUILDDIR)

# Here list all the files that configure should create (except for the
# configuration header file)
AC_CONFIG_FILES([Makefile coindatamiplib3.pc coindatamiplib3-uninstalled.pc])

# Finally, we let configure write all the output...
AC_COIN_FINALIZE
