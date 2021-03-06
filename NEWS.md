# dict 0.10.0

- add option to initialize `dict` with keys and values

# dict 0.9.0

- initial benchmarking showed that `dict` was a lot slower than `hash`, but most of this was function lookups in R. Caching the function improved the lookup speed.

# dict 0.8.0

- New unified functions for NumVecDict: `each_mean`, `each_median`, `each_max`, `each_min` and the same for `inplace_...`

- Note that this changes the names of the functions `means` and `inplace_means`, as the plural form is awkward for max and min.

# dict 0.7.0

- Improve vignette.

- Add function `inplace_means` for NumVecDict.

# dict 0.6.0 "Don't run with scissors"

- While starting a vignette, it became apparent that storing pointers
in the C++ class works during testing, but not when creating the vignette
via knitr. As this hints towards some deeper problem, R objects are now
stored in a list on the R side, and the C++ side only retains a map of indexes
in the list.

- Add function `length`.

# dict 0.5.0

- Add function `append_items` for NumVecDict.

# dict 0.4.0

- Add function `means` for NumVecDict.

# dict 0.3.0

- Add functions `keys`, `values`, and `items`.

# dict 0.2

- Add `[[ ]]` syntax.

# dict 0.1

- Initial release with `get` and `set` syntax.