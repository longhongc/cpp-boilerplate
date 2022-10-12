# Valgrind Exercise
There are two bugs in the original source code.
The output of valgrind before and after debugging is in the folder valgrind_output.

The first bugs is forgot to deallocate memory allocating from the heap.
The second bugs is forgot to initialize value for variables.

## Build
```
mkdir build
cd build
cmake ..
make -j
```

## Run
Run valgrind
```
cd build/app
valgrind --tool=memcheck --leak-check=yes --show-reachable=yes --num-callers=20 --track-fds=yes ./shell-app
```


