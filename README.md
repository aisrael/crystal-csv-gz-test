# crystal-csv-gz-test
Crystal port of https://github.com/mostlygeek/go-csv-gz-test

This is a micro-benchmark project to see how fast Crystal can filter
S3 inventory .csv.gz files

## Other implementations:

* [mostlygeek's Go implementation](https://github.com/mostlygeek/go-csv-gz-test)
* [mythmon's Rust implementation](https://github.com/mythmon/rust-gz-csv-test)
* [peterbe's Python implementation](https://gist.github.com/peterbe/f147fd093aef43304a5c7e0a89c1ea0a) + [blog](https://www.peterbe.com/plog/fastest-python-datetime-parser)

## Usage

```
# get some working data, downloads 1GB from S3 into testdata/ subdirectory
> ./download.sh

# Processing using a one file at a time
> crystal run ./filter.cr
```

## My results (on my late 2016 13" MBP)

```
Total: 31521045, Matched: 710093, Ratio: 2.25%
Time: 00:28:44.910567000
```
