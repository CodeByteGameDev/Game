# Game (Name TDB)
Platformer Game.

## Building
This game uses autoconf to build. On windows you will need to use cygwin to build it and its dependencies
The game requires both c and c++ compiler and GNU make (other flavors of make may not work), as well as a C library with posix functions, and pthread.
To build, change to a different directory (a `build` directory created under the source tree is recommended), and execute the configure script located in this file (from `build`, run as `../configure`). 
When that is finished, type `make`.
There are a number of options available for configuration.
Run the configure script with `--help`
