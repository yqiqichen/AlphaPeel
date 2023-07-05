# AlphaPeel

AlphaPeel is a software package for calling, phasing, and imputing genotype and sequence data in pedigree populations. This program implements single-locus peeling, multi-locus peeling, and hybrid peeling. A complete description of these methods is given in the suggested citation:

Whalen, A, Ros-Freixedes, R, Wilson, DL, Gorjanc, G, Hickey, JM. (2018). Hybrid peeling for fast and accurate calling, phasing, and imputation with sequence data of any coverage in pedigrees. Genetics Selection Evolution; doi: <a href="https://doi.org/10.1186/s12711-018-0438-2">https://doi.org/10.1186/s12711-018-0438-2</a>

## User guide

See https://alphapeel.readthedocs.io/en/latest

## Conditions of use

AlphaPeel is fully and freely available for all use under the MIT License.

## Requirements

* Python 3
* NumPy
* Numba

## Installation

AlphaPeel is available on [PyPi](https://pypi.org/project/AlphaPeel): 

    pip install AlphaPeel

## Build instructions

Run the following to build the Python wheel and user guide. You will need an installation of [Sphinx](https://www.sphinx-doc.org) and [LaTex](https://www.latex-project.org/get) to build the user guide.

    git clone --recurse-submodules https://github.com/AlphaGenes/AlphaPeel.git
    cd AlphaPeel
    
    mamba create -n AlphaPeel
    mamba activate AlphaPeel
    mamba install python=3.9
    pip install sphinx
    ./build_pipeline.sh
    pip install --force-reinstall dist/AlphaPeel*.whl
    
    cd example; ./runScript.sh

The wheel can be found in `dist/` and PDF of the user guide at `docs/build/latex/alphaplantimpute2.pdf`
