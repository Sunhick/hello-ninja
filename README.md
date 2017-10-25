# helloworld-ninja-gyp

Helloworld using Ninja(build system) and GYP(meta-build system)

### Installing GYP

* Install the GYP from the chromium source code https://chromium.googlesource.com/external/.

```git clone https://chromium.googlesource.com/external/gyp.git```

* After cloning source, ```cd gyp``` and run the python executable to install.

```sudo python setup.py install```

* At this point GYP should be install in your system. To know where it's install simply type ```which gyp```.

### Installing Ninja

* To install ninja-build on mac

```brew install ninja```

* on Linux (debian)

```sudo apt install ninja-build```

### Compiling the sources

* To compile the sources, type -

```$ GYP_GENERATORS=ninja gyp build.gyp --toplevel-dir=`pwd` --depth=0```

the above command line will generate the ninja build files. And type the following command to build using ninja

```$ ninja -C out/Defaults all```

* Run the target as -

```$ out/Defaults/helloworld```