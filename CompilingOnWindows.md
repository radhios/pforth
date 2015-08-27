# Introduction #

We provide a project for Visual Studio 2005

# Details #

  1. Double click the VS2005 solution "build/win32/vs2005/pforth.sln".
  1. Build the "pforth\_main" project.
  1. Continue with the instructions for "Building the Dictionary" on the page HowToCompile.

Note that there were a few modifications made to the default projects.

The warnings for 64-bit code compatibility were turned to prevent annoying warnings. The property "C/C++"/General/"Detect 64-bit Portability Issues" was set to "No".

The following were added to "C/C++"/PreProcessor/"Preprocessor Definitions":

  * PF\_SUPPORT\_FP - to turn on floating point support
  * 