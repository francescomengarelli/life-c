# Life-C: A High-Performance Simulation Engine

A zero-dependency, cross-platform implementation of Conway's Game of Life 
optimized for asynchronous execution and terminal-based rendering.

### Engineering Highlights:
* **Multithreaded Input**: Utilizes pthreads for asynchronous simulation control, 
  decoupling user interaction from the physics loop.
* **Optimized Neighbor Tracking**: Implements an incremental neighbor-counting 
  algorithm to minimize redundant lookups in sparse grids.
* **Low-Latency Rendering**: Features a double-buffered terminal update system 
  to minimize I/O syscalls and prevent screen flickering.

![example](example.gif)

## Usage

Build using `make`. You'll get an executable `life.exe`.

You can pass different arguments to customise the simulation:

 - `--rows <r>` specify the number of rows
 - `--cols <c>` specify the number of cols
 - `--fps <fps>` specify the FPS at which the simulation should run. (1 FPS == 1 Iteration)
 - `--ggg` generate a gosper glider gun
 - `--lwss` generate a lightweight spaceship
 - `--pacman` enable pacman effect on borders

 When the simulation is running:

 - `<q>` to quit the simulation
 - `<->` to decrease the simulation speed
 - `<+>` to increase the simulation speed

 ## Notes

 - Input handling does not work on Windows
