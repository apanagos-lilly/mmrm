# Compute Subject-Level Potential Outcomes

For a given visit, computes each subject's fitted potential outcome
under each combination of fixed variable levels by constructing the
counterfactual design matrix. Each subject's own covariate values are
used for all non-fixed variables.

## Usage

``` r
h_compute_potential_outcomes(
  object,
  subj_data,
  visit_value,
  visit_var,
  counterfactual_grid
)
```

## Arguments

- object:

  (`mmrm`)\
  the fitted MMRM.

- subj_data:

  (`data.frame`)\
  one row per subject with covariates.

- visit_value:

  (`string`)\
  the visit level to evaluate at.

- visit_var:

  (`string`)\
  name of the visit variable.

- counterfactual_grid:

  (`data.frame`)\
  unique combinations of fixed variables (excluding visit) to loop over.

## Value

A list with:

- `vhat`: `matrix` of fitted potential outcomes (n x K).

- `L_global`: `matrix` of globally-weighted contrast rows (K x p).
