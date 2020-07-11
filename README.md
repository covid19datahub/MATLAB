<a href="https://covid19datahub.io"><img src="https://storage.covid19datahub.io/logo.svg" align="right" height="128"/></a>

# MATLAB Interface to COVID-19 Data Hub
[![DOI](https://joss.theoj.org/papers/10.21105/joss.02376/status.svg)](https://doi.org/10.21105/joss.02376)

Fetch the data by

```matlab
% download
data = urlread("https://storage.covid19datahub.io/data-1.csv");
% save to tempfile
csv_file_name = tempname;
tmp_file = fopen(csv_file_name, 'w');
fwrite(tmp_file, data);
fclose(tmp_file);
% parse csv from file
data = readtable(csv_file_name);
```
