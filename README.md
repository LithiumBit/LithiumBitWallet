# LithiumBitWallet

#### Trasladar archivos de Repositorio "LithiumBit" a carpeta "cryptonote"
#### On * nix / OS X

Dependencies: CMake 2.8.6 or later, Boost 1.59 or later and QT 5.1 or later.

You may download them from:

* http://www.cmake.org/
* http://www.boost.org/
* https://www.qt.io/

```
cd lithiumbitwallet/
sudo cmake CMakeLists.txt
sudo make install -j2

```

#### To create a portable build

##### On * nix

```
cp src/lithiumbitwallet.desktop build/
cp src/images/lithiumbit.png build/
cd build
linuxdeployqt.AppImage lithiumbitwallet.desktop -appimage -verbose=2 -always-overwrite -no-translations
```

##### On OS X

```
./macdeployqt lithiumbit.app -dmg
```

