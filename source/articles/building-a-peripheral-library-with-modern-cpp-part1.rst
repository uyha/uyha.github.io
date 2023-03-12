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
  - `CMake`_
  - `Conan`_

- Use external libraries where needed
- Test the library as best as possible

This series will be about my journey of creating this library.

A new C++ library
=================
There are a few templates to start a new C++ project like `cmake-init
<https://github.com/friendlyanon/cmake-init>`_, or `cmake_conan_boilerplate_template
<https://github.com/cpp-best-practices/cmake_conan_boilerplate_template>`_. I also have
my own `template <https://github.com/uyha/cpp-template>`_ and
`cmake modules <https://github.com/uyha/cmake-modules>`_, and I start my project with
it.

This project uses `Conan`_ as a package manager, it is invoked automatically
whenever CMake is configured. This is achieved by using ``include(Conan)``, this cmake
module 

.. _CMake: https://cmake.org
.. _Conan: https://conan.io
