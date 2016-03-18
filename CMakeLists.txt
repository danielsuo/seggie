cmake_minimum_required (VERSION 3.2)

project (seggie)

include (ExternalProject)

# Note: need to install FTDI D2XX1.1.12
# http://www.ftdichip.com/Drivers/D2XX/MacOSX/D2XX1.1.12.dmg

ExternalProject_Add(segwayrmp
  GIT_REPOSITORY https://github.com/danielsuo/libsegwayrmp
  SOURCE_DIR "${CMAKE_CURRENT_BINARY_DIR}/segwayrmp"
  CONFIGURE_COMMAND ""
  BUILD_COMMAND make
  INSTALL_COMMAND ""
  UPDATE_COMMAND ""
  BUILD_IN_SOURCE 1
  )
