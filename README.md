# PPNM
Repo for the course: PPNM

## How the notebooks use C++

The notebooks in this repository are used as the main interface for documenting, running, and presenting the solutions. Each notebook contains explanations, code cells, plots, and numerical results. The actual numerical algorithms are implemented in C++ rather than directly in Python.

The general workflow is:

1. The notebook explains the problem and the numerical method.
2. C++ source files are written or used from the project folder.
3. The C++ code is compiled from inside the notebook, often using shell commands such as:

```bash
g++ -std=c++23 -O2 main.cpp -o main
```

or by using a `Makefile`:

```bash
make
```

4. The compiled C++ program is executed from the notebook.
5. The C++ program prints numerical results or writes data files, such as `.txt` or `.data` files.
6. The notebook then reads these results and uses Python, NumPy, Pandas, and Matplotlib to analyze and visualize them.

So the notebooks act both as a report and as a reproducible workflow. The numerical method is implemented in C++, while Python is mainly used for plotting, data handling, and presenting the results.

For example, a notebook may compile and run a C++ program with commands like:

```bash
g++ -std=c++23 -O2 program.cpp -o program
./program > output.txt
```

The output can then be loaded in Python:

```python
import numpy as np
data = np.loadtxt("output.txt")
```

and plotted using Matplotlib.


## Requirements

The notebooks require both a Python environment and a C++ compiler.

The Python packages used for analysis and plotting can be installed with:

```bash
python -m pip install numpy matplotlib pandas scipy
```

The C++ parts require a compiler such as `g++`. On Ubuntu or WSL this can be installed with:

```bash
sudo apt update
sudo apt install build-essential
```

Some folders may also use `make`, which is included with `build-essential`.

## Repository structure

The repository is organized into exercises, homeworks, and exam project:

```text
Exercises/
Homework/
Exam/
```


