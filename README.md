# breed
An experimental approach to meta-program benchmark and resource sections in a snakemake workflow

This program will allow you to breed snakefiles containing benchmarks and/or resource sections from an initial snakefile without altering the original snakefile/rule file.

```
usage: breed [-h] -s SNAKEFILE [-o OUTPUT] [-t] [-tr [TARGET_RULE]] [-w] [-ew EXCLUDE_WILDCARDS [EXCLUDE_WILDCARDS ...]] [-b [1,2,3, or ...]] [-rb] [-r] [-rr] [-v]

breed will create any number of children snakefiles from a parent snakefile that exists. The offspring may contain new benchmark or resource sections as well as shed them.

options:
  -h, --help            show this help message and exit
  -s SNAKEFILE, --snakefile SNAKEFILE
                        The snakefile to bless with benchmark/resource sections
  -o OUTPUT, --output OUTPUT
                        New snakefile with benchmark or resources sections
  -t, --top-level       Print the snakefile top-level/psuedo-rules rules (e.g. rule all)
  -tr [TARGET_RULE], --target-rule [TARGET_RULE]
                        Return only the target rule text. Default will return all target rule text.
  -w, --wildcards       Print the wildcards in benchmark file name for each target rule
  -ew EXCLUDE_WILDCARDS [EXCLUDE_WILDCARDS ...], --exclude-wildcards EXCLUDE_WILDCARDS [EXCLUDE_WILDCARDS ...]
                        Include any wildcards that should be excluded from the benchmark filename (e.g. {outdir} or {{indir}})
  -b [1,2,3, or ...], --benchmarks [1,2,3, or ...]
                        Add benchmark sections to each target rule in the snakefile. Set any number of repeats for all benchmarks with a positive integer
  -rb, --remove-benchmarks
                        Remove all benchmark sections from the input file!
  -r, --resources       Add resources section to each target rule in snakefile from benchmark tsv output
  -rr, --remove-resources
                        Remove all resource sections from the input file!
  -v, --verbose         Print current state of benchmarks and resources section in file.
```
