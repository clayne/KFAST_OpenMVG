CMAKE_MINIMUM_REQUIRED(VERSION 2.6)
PROJECT(KFAST)
SET(KFAST_VERSION_MAJOR 1)
SET(KFAST_VERSION_MINOR 0)

ADD_DEFINITIONS("-pedantic -Ofast -fomit-frame-pointer -std=c++11 -mavx2 -msse4 -march=native -mfma -flto")

ADD_LIBRARY(fast STATIC
	KFAST.cpp
)

INSTALL(TARGETS fast DESTINATION lib EXPORT openMVG-targets)
