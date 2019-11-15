# DHSVocabulary
Framework for running and analyzing ENCODE DHS presence/absence data with non-negative matrix factorization (NMF). 
This `OONMF.py` library provides a wrapper to run the `scikit-learn` NMF routine, and several other functions that can analyze the resulting decomposed matrices. `OONMFhelpers.py` and `OONMFmetadata.py` are libraries that provide additional functions useful for analysis.

To run the code as we did in the DHS Vocabulary paper with `k=16`, download the repository, as well as the DHS presence/absence matrix (733 samples x 3.59e6 DHSs) `matrix_bin_all_733samples_WM20180608.txt` (available [here](https://drive.google.com/file/d/1H-JOLd0NKggPIQPVdpgUJZsfX1kER6M_/view?usp=sharing)) and run:

```
python OONMF_compute_presence_NNDSVD_O.py
```

the output of this code will be the `Basis` (733 samples x 16 components)  and `Mixture` (3.59e6 DHSs x 16 components) matrices, in numpy binary format. If tab-separated output format is desired, uncomment the last line of this script.

Note: requires Python 3 with `scikit-learn`, `numpy`, `scipy`, `matplotlib`, `pandas` installations.
