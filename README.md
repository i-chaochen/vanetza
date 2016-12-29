# Vanetza

Vanetza is an open-source implementation of the ETSI ITS-G5 protocol stack.
It covers GeoNetworking (GN) and Basic Transport (BTP) protocols as well as Decentralized Congestion Control (DCC) and aspects of the Facilities layer.

# How to build

Building Vanetza is accomplished by the CMake build system. Hence, CMake needs to be available on the build host.

## Prerequisites

You need following tools and libraries on your system for compiling Vanetza:

* C++11 compatible compiler, e.g. GNU GCC or Clang
* CMake 3.1 or higher
* Boost 1.58 or higher
* GeographicLib 1.37 or higher
* Crypto++ 5.6.1 or higher

If openSSL 1.1.0 is available on your system, an alternative security backend implementation is compiled along with the Crypto++ based backend.
You can switch the employed backend per `geonet::Router` instance through the `vanetzaCryptoBackend` option located in the Management Information Base (MIB).

## Compilation

Following command line snippet demonstrates the build process using a generated Makefile.
Other CMake generators and build directory setups can be used as well.

    cd vanetza
    mkdir build && cd build
    cmake ..
    make

## Continuous Integration

We strive for quality in our code base. Latest commits are built using [Travis CI](https://travis-ci.org) as part of this effort.
[![Build Status](https://travis-ci.org/riebl/vanetza.svg?branch=master)](https://travis-ci.org/riebl/vanetza)

## Demo

Vanetza ships with a simple demo application called *socktap*.
You can enable the build process for this application by the *BUILD_SOCKTAP* CMake option.
See [tools/socktap](tools/socktap/README.md) for details.

# Authors

Development of Vanetza is part of ongoing research work at Technische Hochschule Ingolstadt.
Maintenance is coordinated by Raphael Riebl. Contributions are happily accepted.

# License

Vanetza is licensed under LGPLv3, see LICENSE.md for details.
