# Route Planning Project

This repo contains the starter code for the Route Planning project.
<img src="map.png" width="600" height="450" />

## building the `IO2D`library
The `IO2D's` library's `CMake` script expects `cairo` and `graphicsmagick` to be installed. So before cloning the `IO2D` library we run
```
sudo apt update
sudo apt install build-essential
sudo apt install cmake
sudo apt install libcairo2-dev
sudo apt install libgraphicsmagick1-dev
sudo apt install libpng-dev
```
we then go ahead to clone and build the `IO2D` library
```
$ git clone --recurse-submodules https://github.com/cpp-io2d/P0267_RefImpl
$ cd P0267_RefImpl
$ mkdir Debug
$ cd Debug
$ cmake --config Debug "-DCMAKE_BUILD_TYPE=Debug" ..
$ cmake --build .
```
## updating `cmake`
The Ubuntu package for `Cmake` is usually an earlier version and won't be able to run our project. So we remove it
```
$ sudo apt-get purge cmake
```
And install a more current version from https://cmake.org/download/ such as cmake-3.14.3.tar.gz
```
$ tar -xzvf cmake-3.14.3.tar.gz
$ cd cmake-3.14.3
$ ./bootstrap
$ make
$ sudo make install 
```
Now you can clone this project
## Cloning


When cloning this project, be sure to use the `--recurse-submodules` flag. Using HTTPS:
```
git clone https://github.com/singhsduos/Route-Planning-Project.git --recurse-submodules 
```


## Dependencies for Running Locally
* cmake >= 3.11.3
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* gcc/g++ >= 7.4.0
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same instructions as make - [install Xcode command line tools](https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)
* IO2D
  * Installation instructions for all operating systems can be found [here](https://github.com/cpp-io2d/P0267_RefImpl/blob/master/BUILDING.md)
  * This library must be built in a place where CMake `find_package` will be able to find it

## Compiling and Running

### Compiling
To compile the project, first, create a `build` directory and change to that directory:
```
mkdir build && cd build
```
From within the `build` directory, then run `cmake` and `make` as follows:
```
cmake ..
make
```
### Running
The executable will be placed in the `build` directory. From within `build`, you can run the project as follows:
```
./OSM_A_star_search
```
Or to specify a map file:
```
./OSM_A_star_search -f ../<your_osm_file.osm>
```

## Testing

The testing executable is also placed in the `build` directory. From within `build`, you can run the unit tests as follows:
```
./test
```

