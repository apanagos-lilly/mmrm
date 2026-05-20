# Compute G-computation Correction for emmeans Integration

Computes the corrected L matrix (global covariate weighting) and the p x
p variance correction matrix. Together these produce the G-computation
estimator with correct standard errors.

## Usage

``` r
h_gcomp_emm_correction(object, model_mat, grid)
```

## Arguments

- object:

  (`mmrm`)\
  the fitted MMRM with `emmeans_gcomp_vars` set.

- model_mat:

  (`matrix`)\
  the L matrix from the emmeans reference grid.

- grid:

  (`data.frame`)\
  the reference grid from emmeans.

## Value

A list with:

- `delta`: `matrix` p x p positive semi-definite correction.

- `L_global`: `matrix` n_grid x p globally-weighted L matrix.
