# Game Math Library in C

Game Math Library written in C.

## How to build

```sh
git clone https://github.com/silentstranger5/glm
cd glm
cmake -B build -S .
cmake --build build
```

## About

This library implements two, three and four dimensional vectors and matrices with operations on them. 
There are also some basic affine and camera transformations implemented as well.
The library assumes column-major matrix order and left-handed coordinate system.
If you want to switch to row-major order, just transpose the matrix after all calculations are done. 
Note that operations on row-major matrices are not supported.
If you want to switch to right-handed coordinate system, it is often sufficient to negate the third column of the matrix (assuming column-major order). 
In some cases, more calculations are required.
There is at least one transformation that can not be transformed into right-handed coordinate space due to the way it is constructed: glm_lookat.
