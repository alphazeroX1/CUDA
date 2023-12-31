# R2C_C2R Sample without descriptors

This sample shows how to compute a distributed R2C-C2R transform without the use of descriptors.
It explains how data is distributed according to `CUFFT_XT_FORMAT_INPLACE` and `CUFFT_XT_FORMAT_INPLACE_SHUFFLED`.
Finally, it applies an element-wise transform making use of the `BoxIterator` iterator to easily iterate through and index the distributed data.

To build and run:
```
$ MPI_HOME=/usr/lib/x86_64-linux-gnu/openmpi/ make run
Hello from rank 1/2 using GPU 1
Hello from rank 0/2 using GPU 0
Shuffled (Y-Slabs) GPU data, global 3D index [0 1 0], local index 0, rank 1 is (3.289261,0.000000)
Shuffled (Y-Slabs) GPU data, global 3D index [0 1 1], local index 1, rank 1 is (-1.492967,2.346867)
Shuffled (Y-Slabs) GPU data, global 3D index [0 1 2], local index 2, rank 1 is (0.645631,0.000000)
Shuffled (Y-Slabs) GPU data, global 3D index [1 1 0], local index 3, rank 1 is (-2.242222,0.000000)
Shuffled (Y-Slabs) GPU data, global 3D index [1 1 1], local index 4, rank 1 is (0.342550,-0.446430)
Shuffled (Y-Slabs) GPU data, global 3D index [1 1 2], local index 5, rank 1 is (0.671049,0.000000)
Shuffled (Y-Slabs) GPU data, global 3D index [0 0 0], local index 0, rank 0 is (3.783546,0.000000)
Shuffled (Y-Slabs) GPU data, global 3D index [0 0 1], local index 1, rank 0 is (-0.385746,-1.599692)
Shuffled (Y-Slabs) GPU data, global 3D index [0 0 2], local index 2, rank 0 is (-4.507643,0.000000)
Shuffled (Y-Slabs) GPU data, global 3D index [1 0 0], local index 3, rank 0 is (0.778320,0.000000)
Shuffled (Y-Slabs) GPU data, global 3D index [1 0 1], local index 4, rank 0 is (0.205157,1.710624)
Shuffled (Y-Slabs) GPU data, global 3D index [1 0 2], local index 5, rank 0 is (1.806104,0.000000)
Relative Linf error on rank 0, 8.582340e-08
Relative Linf error on rank 1, 5.971924e-08
PASSED on rank 1
PASSED on rank 0
```
