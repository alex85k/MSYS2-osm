MSYS2-osm
=========

To compile OSRM for Windows (MinGW) with MSYS2 environment, the following steps are needed:

1. Download and install MSYS2: http://msys2.github.io/
2. It contain very good packaging system. Enter its shell ``C:\msys64\mingw64_shell.bat``.
3. Update the pacakages database
   ```bash
   pacman -Sy
   ```
and install the lates mingw-w64 compiler:
   ```bash
   pacman -S mingw-w64-x86_64-gcc
   ```
3. Install the developer tools:
   ```bash
   pacman -S git subversion make automake autoconf mingw-w64-x86_64-cmake libtool
   ```
4. Install the developer libraries:
   ```bash
   pacman -S mingw-w64-x86_64-zlib mingw-w64-x86_64-bzip2 mingw-w64-x86_64-protobuf mingw-w64-x86_64-lua mingw-w64-x86_64-libxml2 mingw-w64-x86_64-intel-tbb mingw-w64-x86_64-boost
   ```

5. Clone this repository
   ```bash
   git clone https://github.com/alex85k/MSYS2-osm osm
   ```
6. Compile libosmpbf, stxxl and luabind:
   ```bash
   cd osm/mingw-w64-luabind-git
   makepkg-mingw -i
   cd ../mingw-w64-stxxl-git
   makepkg-mingw -i
   cd ../mingw-w64-libosmpbf-git
   makepkg-mingw -i
   ```

