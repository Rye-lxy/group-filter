# group-filter
A tool to eliminate effect of existing insertions in [dnarrange](https://github.com/mcfrith/dnarrange) output MAF file.

## Method
![group-filter pic](group-filter.jpg)

`group-filter` uses the following 2 steps to filter the dnarrange groups:

1. Checking if the start position (if human genome segment follows insertion segment) or the end position (if insertion segment follows human genome segment) of read alignments to human genome is in target region (specified by RepeatMasker `.out` file).
2. Checking if the direction of insertion segment is identical to the target region.

The groups satisfy these 2 conditions will be removed.

`--gap N` can extend the target region N-base long in both directions.

## Options
`--seg`: Specify the target region file.

`--insert`: Specify the insertion region name in MAF file.

`--gap`: Set an N-base extension for each direction in each region.

`-i`, `--input`: Input file.

`-o`, `--out`: Output file prefix.
