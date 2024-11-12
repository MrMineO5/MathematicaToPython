# MathematicaToPython

Mathematica package to convert [MATHEMATICA](https://www.wolfram.com/mathematica/) expressions to Python [Numpy](http://www.numpy.org/)

## Quick usage

The quickest way to use the package is to directly load it from the master branch of this
repository by running the following code in a Mathematica notebook:

```Mathematica
Import["https://raw.githubusercontent.com/MrMineO5/MathematicaToPython/master/ToPython.wl"]
```

## Installation

To install the package permanently, do the following

1. Download it from this repository
2. Click on `Mathematica`' `File menu-> Install->From file...`
3. Select the file on your disk

You should be ready to go.

## Usage

The package mainly provides the `ToPython` function, which takes a Mathematica expression
and tries to convert it to a python expression. It can handle a lot of expressions
already, but it is obviously limited.

Beside the actual expression the `ToPython` function also supports two options:

* `NumpyPrefix`, which determines the name under which numpy is imported. The default is
  to prefix all numpy call with `np.`, but you can also set `NumpyPrefix` to `"numpy"` to
  enforce `numpy.` as a prefix. If you supply an empty string, no prefix is added, which
  might be useful if you use the wildcard import `from numpy import *`
* `Copy`, which when enabled copies the formatted expression to the clipboard

Taken together, a simple example call is

```Mathematica
ToPython[Sin[x], NumpyPrefix->"numpy", Copy->True]
```

which should copy `numpy.sin(x)` to your clipboard.

## Disclaimer

This has not been tested for every possible combinations of all the things, use at your own risks.

## License

[MIT](LICENSE.md) © [Gustavo Wiederhecker](https://github.com/gwiederhecker) with modifications from our group
