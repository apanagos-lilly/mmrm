# Get Subject-Level Covariate Data

Returns one row per subject with covariate data. Uses the stored
`emmeans_gcomp_subject_data` from the original dataset when available
(includes subjects with missing outcomes), otherwise falls back to the
fitted model's complete-case frame.

## Usage

``` r
h_get_subject_data(object)
```

## Arguments

- object:

  (`mmrm`)\
  the fitted MMRM.

## Value

A `data.frame` with one row per subject.
