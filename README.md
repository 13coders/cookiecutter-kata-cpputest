# Template for TDD Code Katas in C++

Hey there. This is a cookiecutter template for a simple TDD code kata
using CppUTest.  It's intended to give you a repeatable way of very
quickly getting started for a "deliberate practice" session with C++.

## Features of this template

This generates a project for doing a test-driven code kata in C++.

- Includes CppUTest library
- Generates a header, "production" source file and an empty test
- Generates a CMake build which will work on most platforms
- Has some convenience targets for generating etags and running unit
  tests

## Pre-requisites

You'll need to have [cookiecutter
installed](https://github.com/audreyr/cookiecutter). This is a Python
tool - on most platforms, install using:

```
$ pip install cookiecutter
```

After the kata project is created, you'll need to generate a build
using [CMake](https://cmake.org/), and then of course compile, link
and execute the kata. This is all going to take a fairly complete C++
development toolchain, and you'll need to figure out how to get this
configured for your platform, if you don't already have one.

The minimum requirements for building this are really those from
[CppUTest](http://cpputest.github.io/), which is highly portable
across C++ versions and compilers.

## Generating your project

Start by invoking cookiecutter. This can be done locally - handy if
you're working disconnected:

```
$ cookiecutter <path-to-this-template>
```

or directly from the GitHub URL where the template lives:

```
$ cookiecutter https://github.com/13coders/cookiecutter-kata-cpputest
```

This template is intended to be very simple, so cookiecutter will
prompt you for only three parameters when you are creating your project:

```
kata [CodeKata]: 
```

This is name/title of the Code Kata. Whatever name you provide will be
capitalised exactly as you enter it:

- If you use camel case, the name of the test file, source file and
  header will be, for example "GameOfLife.cpp", "GameOfLifeTest.cpp"
  etc

- The name will be lowercased for the CMake file, the name of the
  repository, the value in the #include guard and the dummy namespace
  that's generated in the header

So, if you prefer CamelCase file names, use something like
"GameOfLife" as the kata name, or if you prefer snake_case file names,
then use "game_of_life".

```
Select etags:
1 - y
2 - n
Choose from 1, 2 [1]: 1
```

This lets you decide whether or not to include the build file magic
for generating an [etags
file](https://www.emacswiki.org/emacs/BuildTags) when recompiling-,
which defaults to "y". If you choose no, there will be no dependency
on etags in the build.

If you want to, you can always add any extra tools you need (static
analyzers, sanitizers etc) into the CMake file yourself - it's a
minimal starting point.

```
Select license:
1 - GNU General Public License v3
2 - MIT license
3 - Apache Software License 2.0
Choose from 1, 2, 3 [1]: 1
```

Lets you select the free/open source license for your kata sources. If
you don't want a license, just delete the contents of the LICENSE file
after generating the project. Defaults to GPL v3.

## Next steps

Your newly generated project has its own README.md, which has the next
steps for compiling, linking and running the tests. There are also
some useful resources linked in there on TDD, software craftsmanship
and code katas to try out.

Happy coding !
