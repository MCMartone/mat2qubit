
## Overview

`mat2qubit` is a Python package for converting matrix operators into a Pauli operator representation. Single particles/subsystems as well as interacting particles (e.g. many-body Hamiltonians) may be processed. More formally, the code takes sums of tensor products of arbitrarily sized matrices, and maps them to sums of Pauli products with a chosen encoding. The code assumes trivial (i.e. bosonic etc) commutation, meaning that it cannot be used for fermionic particles.

<!--
```math
\sum \cdots \otimes M \otimes N \otimes \cdots \rightarrow \sum \bigotimes \{I,\sigma_x,\sigma_y,\sigma_z\}
```
-->

The package can be used to implement different encodings for which there are often depth-space tradeoffs or other resource tradeoffs (see references below). The built-in encodings include <b>standard binary</b>, <b>Gray code</b>, <b>unary (one-hot)</b>, and <b>block unary</b>. User-defined embeddings may be added by modifying `integer2bit.py`.

Mathematical and theoretical details can be found in these references:
* Sawaya, NPD, Menke, T, Kyaw, TH, Johri, S, Aspuru-Guzik, A and Guerreschi, GG. [npj Quantum Information, 6(49)](https://www.nature.com/articles/s41534-020-0278-0) (2020).
* Sawaya, NPD, Schmitz, AT, and Hadfield, S. arXiv preprint [arXiv:2203.14432](https://arxiv.org/abs/2203.14432) (2022).

Please see the two files in the `examples/` directory for worked examples of Bose-Hubbard model, chemical vibrations, classical linear algebra, spin-<i>s</i> models, graph coloring, traveling salesperson problem, and machine scheduling.

Intel Labs 2020 - 2022.
Contact: nicolas.sawaya@intel.com


## Installation

We recommend one of two installation options:

#### Option 1
`python setup.py bdist_wheel`  
`pip install dist/*.whl`

#### Option 2
In your `.bash_profile` include the path to the `mat2qubit` directory in `PATH` and `PYTHONPATH`.a

