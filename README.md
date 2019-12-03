# Schottky Data Analysis Framework
This repo's codes efficiently implement a wide spectrum of algorithms useful for Schottky data analyses within the context of Schottky spectroscopy experiments.
A selected examples include, but are not limited to, numerical calculation of **discrete prolate spheroidal sequence** (**DPSS**), **spectral density estimation** of Schottky signal, **periodogram** with different windows, **multitaper**, and so on.

Presently, it is compatible with **`wv`** files (e.g. generated by _Rohde & Schwarz_ [`FSVR`](https://www.rohde-schwarz.com/product/fsvr-productstartpage_63493-11047.html)), as well as **`tiq`** files (e.g. generated by _Tektronix_ [`RSA5000B`](https://www.tek.com/spectrum-analyzer/rsa5000)).

## Prerequisites
 - `Python 3`
 - `Scipy`, `Numpy`
 - [`BLAS`](http://www.netlib.org/blas/) and [`LAPACK`](http://www.netlib.org/lapack/) libraries (_essential for matrix computation_)
 - [`pyFFTW`](https://hgomersall.github.io/pyFFTW/) (_essential for FFT_)
 - [`true-random-number`](https://github.com/nerdull/true-random-number) (_essential for provoding true random numbers of normal distribution_)
 - `Matplotlib` (_optional, only if visualization is needed_)

## Usage
All the codes are supposed to be imported as modules into a _main_ `Python` script, or a `Jupyter` notebook.
 1. `dpss.py`: generate a list of DPSSs with given length and bandwidth
 2. `preprocessing.py`: read meta-info from header, and load IQ data into memory
 3. `processing.py`: spectral density estimation using periodogram or multitaper in 1D and 2D

See [Wiki](https://github.com/SchottkySpectroscopyIMP/data-analysis/wiki) for more explanations about the class methods and arguments.

In addition, this repo is shipped with an extra script `synthetic.py` for test.
By using that, one can produce synthetic `wv` files with customized artificial signals inside.
Common waveforms include **sinusoids**, **rectangular** and **triangular pulses**, etc., as well as stochastic processes, such as **autoregressive processes** and **noise-corrupted sinusoids**. 

## License
This repository is licensed under the **GNU GPLv3**.
