Built with msys + Rtools gcc + cmake from msys2.

```
MSYS2_ARG_CONV_EXCL="-DCMAKE_INSTALL_PREFIX=" \
  /c/msys2-x64/mingw64/bin/cmake.exe \
    -Wno-dev \
    -G"MSYS Makefiles" \
    -DCMAKE_INSTALL_PREFIX="/c/msys2-x64/mingw64/bin/" \
    -DBUILD_SHARED_LIBS=ON \
    -DCMAKE_BUILD_TYPE=Release \
    -DCMAKE_SKIP_RPATH=ON \
    -DHDF5_BUILD_HL_LIB=ON \
    -DHDF5_BUILD_CPP_LIB=ON \
    -DHDF5_BUILD_FORTRAN=ON \
    -DHDF5_BUILD_TOOLS=ON \
    -DHDF5_ENABLE_DEPRECATED_SYMBOLS=ON \
    -DHDF5_ENABLE_SZIP_SUPPORT=OFF \
    -DHDF5_ENABLE_Z_LIB_SUPPORT=ON \
    ../hdf5-1.8.16

  make
```

For building with gcc-4.6.3 pass `-m64` or `-m32` flags to compiler.


```
export CFLAGS="-m64"
export CXXFLAGS="-m64"
export FFLAGS="-m64"
MSYS2_ARG_CONV_EXCL="-DCMAKE_INSTALL_PREFIX=" \
  /c/msys2-x64/mingw64/bin/cmake.exe \
    -Wno-dev \
    -G"MSYS Makefiles" \
    -DCMAKE_INSTALL_PREFIX="/c/msys2-x64/mingw64/bin/" \
    -DBUILD_SHARED_LIBS=ON \
    -DCMAKE_BUILD_TYPE=Release \
    -DCMAKE_SKIP_RPATH=ON \
    -DHDF5_BUILD_HL_LIB=ON \
    -DHDF5_BUILD_CPP_LIB=ON \
    -DHDF5_BUILD_FORTRAN=ON \
    -DHDF5_BUILD_TOOLS=ON \
    -DHDF5_ENABLE_DEPRECATED_SYMBOLS=ON \
    -DHDF5_ENABLE_SZIP_SUPPORT=OFF \
    -DHDF5_ENABLE_Z_LIB_SUPPORT=ON \
    ../hdf5-1.8.16

  make
```