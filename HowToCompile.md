[PForthHome](PForthHome.md)

# Introduction #

PForth is very easy to build on most platforms, including desktop or embedded. The main steps are:

  1. Build pForth kernel in 'C'.
  1. Run pForth and build Forth dictionary. It will save automatically.
  1. Run pForth with dictionary and test it.

For more information see: http://www.softsynth.com/pforth/pf_ref.html

# Building pForth #

We have provided projects and Makefiles for some platforms.

  * CompilingOnWindows
  * CompilingOnUnix
  * CompilingOnMac

If you want to compile pForth for a new platform, please follow these instructions.

## Custom Compile of Kernel ##

  1. Add all of the 'C' code in the "csrc/" folder to your project.
  1. If your system supports getchar() and putchar() then add all of the files in "csrc/stdio/".
  1. If you want floating support then define preprocessor variable PF\_SUPPORT\_FP
  1. Compile, link and place the executable called "pforth" in the "fth/" folder.

## Building The Dictionary ##

The _words_ (functions) in pForth are stored in a dictionary. They are mostly written in Forth and can be compiled by the pForth kernel. Enter:

```
cd fth
pforth -i system.fth
```

The dictionary will be compiled and saved in a file called "pforth.dic" . That file will get loaded automatically if you enter:

```
pforth
```

# Testing pForth #

You can now execute pForth using the compiled dictionary. Enter:

```
pforth
```

Now add a couple numbers together to test the interpreter. Enter:
```
5  2  +  .
bye
```
It should have added 5 and 2 then printed the result.

You can also run several unit tests. By entering:
```
pforth t_corex.fth
pforth t_strings.fth
pforth t_locals.fth
pforth t_alloc.fth
```

For more information see: http://www.softsynth.com/pforth/pf_ref.html

Here is a Forth tutorial: http://www.softsynth.com/pforth/pf_tut.html