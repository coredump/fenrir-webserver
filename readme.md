# Webserver for fenrir

## How to compile?
This project need [CMake](https://cmake.org/).

If you're on a Linux(or wsl) system, it can be compiled like this:

```
mkdir build
cd build
cmake ..
make
```

## Usage

You can serve a cd image like this

```
FenrirServer <image filename>
```

For example:

```bash
FenrirServer "MyGame.chd"
```

## Compatible image formats

It supports .cue/.nrg/.iso/.chd 


## Licence
[Mongoose](https://cesanta.com/) as http server.

Toc parsing based on [MAME](https://docs.mamedev.org/).

[libchdr](https://github.com/rtissera/libchdr) for CHD supports.

are each distrubted under their own terms.


## Docker

You can use Docker to launch the server.

For example:

```ps
docker run --rm -it  -p 3000:3000 -v ${pwd}:/work ghcr.io/fenrir-ode/webserver:main FenrirServer Sfa2.cue
```