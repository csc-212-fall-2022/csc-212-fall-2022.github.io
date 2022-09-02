+++
title = "Tools"
+++

# Tools

## Mac

Make sure you have the command-line developer tools installed: `xcode-select --install`. 
You probably also want to install [Homebrew](https://brew.sh/).

Use Homebrew to install the following:
- `cmake`
- `clang-format`

### Valgrind

On **Intel Macs**, you can install Valgrind with `brew install valgrind`.

On **M1 Macs**, we can try installing Valgrind by building from source:
1) `brew install autotools`
2) Download [the latest release](https://valgrind.org/downloads/current.html) and expand the archive
3) run `./autogen.sh`
4) run `./configure`
5) run `make`
6) run `make install`
You may need to use sudo for some subset of the commands. (I haven't been able to try this on an M1 Mac.
I did build successfully on my linux machine, so there aren't any *extremely* obscure dependencies.)

### Setting up `clang-tidy`

I found the following gist showing how to set up `clang-tidy` on OS X. (You can skip the `clang-format` symlink.)
<center><script src="https://gist.github.com/sleepdefic1t/e9bdb1a66b05aa043ab9a2ab6c929509.js"></script></center>

## Windows

If you have a linux VM set up from a previous course, see the Linux section below.

While it requires more setup, Windows Subsystem for Linux is probably more convenient to use than a VM.
Instructions for setting up WSL are [here](https://docs.microsoft.com/en-us/windows/wsl/install). There's
also a [tutorial](https://docs.microsoft.com/en-us/windows/wsl/setup/environment) focused on setting up a development environment. There is also a VSCode tutorial for [C++ on WSL](https://code.visualstudio.com/docs/cpp/config-wsl).

Despite the name, the VSCode [CMake Tools on Linux](https://code.visualstudio.com/docs/cpp/cmake-linux) tutorial also applies to Windows once you [download CMake](https://cmake.org/download/).

## Linux

You'll want to install the following packages if you don't have them already (these are the Ubuntu package names):
- `build-essential` (g++, make, libc6-dev, etc)
- `cmake`
- `clang-format`
- `clang-tidy`
- `valgrind`
