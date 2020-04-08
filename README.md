# patient_matcher

## Usage
```python
from jake_match import PatientMatcher


matcher = PatientMatcher(
    excel_file='PATH_TO_MY_DATA.xls' # the excel doc must contain a column named BIPOLAR
)

# Calculates the best match for each bipolar patient,
# given no bipolar patient can be matched to the same control patient.
matches = matcher.get_best_matches()

# A "sanity checker" to visualize how well the matching algorithm performed.
# May only be called after calling get_best_matches.
viz_algo = matcher.decomp_viz(
    matches=matches,
    decomp_method='PCA'
)
```
