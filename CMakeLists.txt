CMAKE_MINIMUM_REQUIRED (VERSION 3.0.0 FATAL_ERROR)
IF (NOT MYPACKAGEBOOTSTRAP_DONE)
  INCLUDE ("3rdparty/github/cmake-utils/cmake/MyPackageBootstrap.cmake")
ENDIF ()
MYPACKAGESTART (coo 1 0 1)

###############
# Executables #
###############
MYPACKAGETESTEXECUTABLE (ooTester                    test/ooTester.c)

#########
# Tests #
#########
MYPACKAGECHECK(ooTester)

#############
# Packaging #
#############
MYPACKAGEPACK("" "Generic OO with plain C")

#########
# Setup #
#########
MYPACKAGEPRINTSETUP()
