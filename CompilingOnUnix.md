# Introduction #

We provide a simple Makefile for compiling.

# Details #

  1. CD to "build/unix"
  1. Enter: make all

This is a complete build. It will create an executable image and associated "pforth.dic" file in the "fth/" folder. You may need to remove the -C89 option from the Makefile if there are too many warnings.

It will also create a standalone executable image that includes the dictionary compiled inside. To run it enter:

> ./pforth\_standalone

# Testing #

> Enter: make test

Return to [PForthHome](PForthHome.md)