Built using the instructions originally from (https://github.com/mannau/h5/blob/master/INSTALL#L49-L69)

- Download current source of HDF5 (used 1.8.14) from 
https://www.hdfgroup.org/ftp/HDF5/releases/hdf5-1.8.14/src/hdf5-1.8.14.tar.gz
unpack the current version to e.g. C:\hdf5
- Install CMake using standard parameters and open.
- Set CMake Source dir to HDF5 Source, e.g. C:\hdf5; Set build dir to new 
directory.
- For each architecture do the following
- The following parameters need to be set manually in the CMake tool (check Advanced Box):
  * CMAKE_INSTALL_PREFIX: a directory
  * BUILD_STATIC_EXECS: check
  * HDF5_BUILD_CPP_LIB: check
  * HDF5_BUILD_HL_LIB: check
  * HDF5_ENABLE_ZLIB_SUPPORT: check
  * ZLIB_INCLUDE_DIR: C:/local320/include
  For 32Bit Platforms:
  * ZLIB_LIBRARY: C:/local320/lib/i386/libz.a
  For 64Bit Platforms:
  * ZLIB_LIBRARY: C:/local320/lib/x64/libz.a
- After Configuration is finished change to build-dir and compile using
$ mingw32-make install
