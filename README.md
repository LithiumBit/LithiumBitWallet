# LithiumBitWallet
#### On * nix / OS X

Dependencies: CMake 2.8.6 or later, Boost 1.59 or later and QT 5.1 or later.

You may download them from:

* http://www.cmake.org/
* http://www.boost.org/
* https://www.qt.io/

```
mkdir build && cd build && cmake -DSTATIC=1 .. && make
```

You may find it helpful to explicitly include Boost and QT paths
```
cmake -DSTATIC=1 -DBOOST_ROOT=/boost_1_59_0 -DBOOST_LIBRARYDIR=/boost_1_59_0/libs/ -DCMAKE_PREFIX_PATH=/qt/5.10 ..
```

#### To create a portable build

##### On * nix

```
cp src/inbestcoinwallet.desktop build/
cp src/images/inbestcoin.png build/
cd build
linuxdeployqt.AppImage inbestcoinwallet.desktop -appimage -verbose=2 -always-overwrite -no-translations
```

##### On OS X

```
./macdeployqt inbestcoin.app -dmg
```

