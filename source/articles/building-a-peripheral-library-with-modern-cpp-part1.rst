.. post:: 2023-03-11
   :tags: modern c++, i2c, spi, linux

======================================================
Building a Peripheral Library with Modern C++ - Part 1
======================================================

Introduction
============
I want to create a library in modern C++ that provides an abstraction for interacting
with I2C and SPI buses on the Linux kernel. My goals for this library are:

- Easy to use interface using C++20
- Easy to build library, requiring only the following:

  - A C++ compiler that supports C++20
  - `CMake <https://cmake.org/>`_
  - `Conan <https://conan.io>`_

- Use external libraries where needed
- Test the library as best as possible

This series will be about my journey of creating this library.

A new C++ library
=================
