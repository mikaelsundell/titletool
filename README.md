Readme for titletool
==================

[![License](https://img.shields.io/badge/license-BSD%203--Clause-blue.svg?style=flat-square)](https://github.com/mikaelsundell/logctool/blob/master/README.md)

Introduction
------------

titletool is a utility for creating title images.

![Sample image or figure.](images/image.png 'it8tool')

Building
--------

The titletool app can be built both from commandline or using optional Xcode `-GXcode`.

```shell
mkdir build
cd build
cmake .. -DCMAKE_MODULE_PATH=<path>/titletool/modules -DCMAKE_PREFIX_PATH=<path> -GXcode
cmake --build . --config Release -j 8
```

Usage
-----

Print titletool help message with flag ```--help```.

```shell
titletool -- a utility for creating titletool images

Usage: overlaytool [options] ...

General flags:
    --help                     Print help message
    -v                         Verbose status messages
    -d                         Debug status messages
Input flags:
    --title                    Set title
    --subtitle                 Set subtitle
    --size SIZE                Set size (default: 1024, 1024)
Output flags:
    --outputfile OUTPUTFILE    Set output file
```

Example title image
--------

```shell
./titletool
--title "Hello, world!"
--subtitle "An image about Hello, world!"
--outputfile title.png 
--size "2350,1000" 
```

Packaging
---------

The `macdeploy.sh` script will deploy mac bundle to dmg including dependencies.

```shell
./macdeploy.sh -e <path>/overlaytool -d <path> -p <path>
```

Dependencies
-------------

| Project     | Description |
| ----------- | ----------- |
| Imath       | [Imath project @ Github](https://github.com/AcademySoftwareFoundation/Imath)
| OpenImageIO | [OpenImageIO project @ Github](https://github.com/OpenImageIO/oiio)
| 3rdparty    | [3rdparty project containing all dependencies @ Github](https://github.com/mikaelsundell/3rdparty)

Project
-------------

* GitHub page   
https://github.com/mikaelsundell/overlaytool
* Issues   
https://github.com/mikaelsundell/overlaytool/issues


Resources
---------

* Dynamic Symmetry: The Foundation of Masterful Art   
Author: Tavis Leaf Glover

Copyright
---------

* Roboto font   
https://fonts.google.com/specimen/Roboto   
Designed by Christian Robertson
