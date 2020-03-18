# poly3d

This repository reproduces code for `poly3d`, a boundary element method program first released in the M.S. thesis Thomas, 1993. It is intended to make this legacy code easily available for use in structural geology, geomechanics, and active tectonics research.

## Documentation

The primary `poly3d` manual is [Thomas, 1993](http://searchworks.stanford.edu/view/2830996). It covers the details of the boundary value problems behind `poly3d` and explains the input and output file formats.

Prof. Michele Cooke (University of Massachussetts, Amherst) maintains [a `poly3d` tutorial page](http://www.geo.umass.edu/faculty/cooke/poly3d/) that previously included the thesis source code provided here. The original `poly3d` tutorial is available there, as are several examples and other software packages. 

Other examples are available on the Stanford Structural Geology and Geomechanics [website](https://pangea.stanford.edu/research/geomech/Software/Software.htm).

### Compiling `poly3d`

This version of `poly3d` has been tested and modified under Debian Linux and CentOS using `gcc` 4.8.

The makefile provided here assumes you are using a recent version of `gcc`, the GNU Compiler Collection. **Mac OS X 10.8 and above alias `gcc` to a `clang` front-end**; to compile `poly3d` in those environments, you must [install `gcc` using Homebrew or macports](http://apple.stackexchange.com/questions/38222/how-do-i-install-gcc-via-homebrew). 

Both versions of `poly3d` must be compiled with the `-O2` flag. Over-optimization (e.g. `-O3` or `-ffast-math`) can lead to unpredictable numerical errors and large singularities in the resulting displacement fields. Just say no!

### Using `poly3d`

`poly3d -i <input> -o <output>`

### Contributors 

`poly3d` and a related commercial software package were developed by researchers and students of Profs. David Pollard and Atilla Aydin associated with the Stanford Rock Fracture Project and the [Structural Geology and Geomechanics research group](https://structuralgeology.stanford.edu/). This repository is intended for academic use only, and is solely derived from the publicly available source code printed in Thomas, 1993 with modifications to fix the "shadow effect."

### References

Please cite this thesis and related publications if you use `poly3d` in published work.

Thomas, A. L., 1993, Poly3D: A three-dimensional, polygonal element, displacement discontinuity boundary element computer program with applications to fractures, faults, and cavities in the Earth's crust (Doctoral dissertation, Stanford University).

To see a recent example of `poly3d` in action, take a look at [this 2014 paper by Fattaruso, Cooke, and Dorsey](http://dx.doi.org/10.1130/GES01050.1) on uplift produced by tectonic activity in the Coachella area.

### Contact
Please [open an issue](https://github.com/stgl/poly3d/issues/new) if you have a question.
