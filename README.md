# diffnc

## Description
Small script to compare two netcdf files, including metadata. The script uses ncdump to extract the content of the file and then diff to perform the comparison

## Installation
Make sure you have `diff`, `awk` and `ncdump` commands available.
In CentOS, you can install them via
```shell
yum install -y diff gawk netcdf diffutils
```

Just download the [diffnc](https://github.com/spinto/diffnc/raw/master/diffnc) script, and run it.
```shell
curl https://github.com/spinto/diffnc/raw/master/diffnc -o diffnc
chmod +x diffnc
./diffnc
```

## Usage
```shell
[~]# ./diffnc -h
diffnc version 1.0
Usage:
diffnc [options] <file1> <file2>

Options:
      -h               Displays this help page
      -x <metadata>    Exclude <metadata> from the comparison (comma-separated for multiple
                       metadata names)
      -q               Do not print differences
      -e | --ed        Output an ed script.
      -n | --rcs       Output an RCS format diff.
      -l | --paginate  Pass the output through 'pr' to paginate it.
      -s               Report when two files are the same.

Exit codes:
      0                files matches
      1                files do not match
```
