# stats

NaN-aware statistical helpers for MATLAB.

Part of the Prerau Lab [`utils`](https://github.com/preraulab/utils) meta-repository. Can also be used standalone.

## Functions

### `nanzscore`

Z-score a vector or matrix, ignoring NaN values.

```matlab
z = nanzscore(x)
z = nanzscore(x, flag, dim)
```

Mirrors the built-in `zscore` API but uses `mean(..., 'omitnan')` and `std(..., 'omitnan')` internally.

### `nanpow2db`

Convert power to dB with NaN pass-through. Equivalent to `10*log10(x)` but preserves NaN values instead of producing `-Inf`.

```matlab
y_dB = nanpow2db(y_power)
```

See `help <function>` at the MATLAB prompt for the full docstring of each.

## Install

```matlab
addpath('/path/to/stats');
```

## Dependencies

MATLAB R2020a+. No required toolboxes.

## License

BSD 3-Clause. See [`LICENSE`](LICENSE).
