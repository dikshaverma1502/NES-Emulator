NES Emulator - GameDev and Esports Club
=============

Implemented a tailored version of the 6502 microprocessor architecture for emulating the Nintendo Entertainment System in C++.
Note- Roughly 40-50% of games should work (ie. games that use either no mapper or mappers 1, 2, 3 and experimental support for 4, 7, 66 and 11).


Screenshots
------------------------

![image](https://user-images.githubusercontent.com/63869921/189893910-baa6938a-d460-4c5f-8616-89cd0d87feaf.png)
![image](https://user-images.githubusercontent.com/63869921/189893939-c2c32cbb-06e3-4f79-9710-abc3405f8b72.png)
![image](https://user-images.githubusercontent.com/63869921/189893976-a264c2e7-3666-44fa-a733-ddc72565aa1a.png)


Compiling
-----------

You need:
* SFML 2.0+ development headers and library
* C++11 compliant compiler
* CMake build system

Compiling is straight forward with cmake, just run cmake on the project directory with CMAKE_BUILD_TYPE=Release
and you'll get Makefile or equivalent for your platform, with which you can compile the emulator

For e.g., on Linux/OS X/FreeBSD:
```
$ git clone https://github.com/amhndu/SimpleNES
$ cd SimpleNES
$ mkdir build/ && cd build/
$ cmake -DCMAKE_BUILD_TYPE=Release ..
$ make -j4    #Replace 4 with however many cores you have to spare
```

Running
-----------------

Just pass the path to a .nes image like

```
$ ./SimpleNES ~/Games/SuperMarioBros.nes
```
To set size of the window,
```
$ ./SimpleNES -w 600 ~/Games/Contra.nes
```
For supported command line options, try
```
$ ./SimpleNES -h
```

Controller
-----------------

Keybindings can be configured with keybindings.conf


Default keybindings:

**Player 1**

 Button        | Mapped to
 --------------|-------------
 Start         | Return/Enter
 Select        | Right Shift
 A             | J
 B             | K
 Up            | W
 Down          | S
 Left          | A
 Right         | D


**Player 2**

 Button        | Mapped to
 --------------|-------------
 Start         | Numpad9
 Select        | Numpad8
 A             | Numpad5
 B             | Numpad6
 Up            | Up
 Down          | Down
 Left          | Left
 Right         | Right
