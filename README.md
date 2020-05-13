# MATLAB Interface to COVID-19 Data Hub

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
