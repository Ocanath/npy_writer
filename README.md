# NPY Writer

Extremely lightweight C++ utility for writing .npy files.

**Usage:**
Simply open the file with name and data type, log data of that type, and close:

```C++
NpyWriter nw;
nw.open("time_sec.npy", NpyWriter::FLOAT32);

/*
.
.
.
*/

nw.add_float32(1.0);
nw.add_float32(2.0);
nw.add_float32(3.0);

nw.close();

```

The same writer can be re-used for multiple files, or multiple instances can be spawned for simultaneous data streams.

Started as a utility for [dartt-dashboard](https://github.com/ocanath/dartt-dashboard), but I moved it to it's own repo for easier linking. 

## Building

Simply use `add_subdirectory()` in cmake to link this to your project.

The typical pattern:

```
cmake -B build
cmake --build build
```

Will statically compile this library.
