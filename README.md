MSYS2-osm
=========

To compile OSRM for Windows (MinGW) with MSYS2 environment, the following steps are needed:

1. Download and install MSYS2: http://msys2.github.io/
2. It contains very good packaging system. Enter its shell ``C:\msys64\mingw64_shell.bat``.
3. Update the packages database
   ```bash
   pacman -Sy
   ```
   
   and install the lates mingw-w64 compiler:
   ```bash
   pacman -S mingw-w64-x86_64-gcc
   ```
   
3. Install the developer tools:
   ```bash
   pacman -S git patch subversion make automake autoconf mingw-w64-x86_64-cmake libtool
   ```
   
4. Install the developer libraries:
   ```bash
   pacman -S mingw-w64-x86_64-gdal mingw-w64-x86_64-spatialite-tools mingw-w64-x86_64-geos mingw-w64-x86_64-libosmpbf-git mingw-w64-x86_64-lua mingw-w64-x86_64-luabind-git mingw-w64-x86_64-stxxl-git mingw-w64-x86_64-intel-tbb mingw-w64-x86_64-boost
   ```

5. Clone this repository
   ```bash
   git clone https://github.com/alex85k/MSYS2-osm osm
   ```
   
   
6. Compile OSRM:
   ```bash
   cd ../mingw-w64-osrm-git
   makepkg-mingw
   
   ```
