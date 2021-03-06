[![DOI](https://zenodo.org/badge/doi/10.5281/zenodo.59226.svg)](http://dx.doi.org/10.5281/zenodo.59226)

# SMoD
SequenceMotifDecomposer (SMoD) is a motif finder algorithm based on the [EDeN](https://github.com/fabriziocosta/EDeN) framework.


## Installation

SMoD can be installed via [conda](http://conda.pydata.org/miniconda.html):

```bash
conda install smod -c bioconda
```


## Usage

SMoD can be invoked as:

```bash
./smod --pos data.fa -t 1 --freq_th 0 --std_th 0
```

## Output
The program outputs a file called report.md in Markdown format.

One can then convert it to html or pdf with appropriate utilities (e.g. [markdown2pdf](https://github.com/kxxoling/markdown2pdf) )

<p align="center"><img src="fig.png"></p>


## Help

```
SequenceMotifDecomposer (SMoD) is a motif finder algorithm.

Version: 1.0
Author: Fabrizio Costa [costa@informatik.uni-freiburg.de]

Usage:
  smod -i FILE (--neg FILE | -t N) [-m FILE] [-o PATH] [-n N] [-p N]
       [-c N] [--min_subarray_size N] [--max_subarray_size N]
       [--similarity_th N] [--min_score N] [--min_freq N]
       [--min_cluster_size N] [--regex_th N] [--sample_size N]
       [--freq_th N] [--std_th N]
       [--verbose]
  smod (-h | --help)
  smod --version

Options:
  -i FILE                 Specify input fasta file for positive seqs.
  --neg FILE              Specify input fasta file for negative seqs.
  -m FILE                 Model file. If specified no fitting is performed
                          [default: None]
  -t N                    The num of permutations for each positive
                          sequence [default: 1].
  -c N                    Feature complexity [default: 5].
  -p N                    P-value [default: 0.05].
  -n N                    Specify the num of clusters [default: 20].
  -o PATH                 Dir name for output files [default: out].
  --min_subarray_size N   The min num of nt in a motif [default: 4].
  --max_subarray_size N   The max num of nt in a motif [default: 10].
  --similarity_th N       The min relative edit distance to merge two motives
                          [default: 0.5].
  --min_score N           The min num of nt in a motif that need to have a
                          freq > min_freq [default: 4].
  --min_freq N            Min freq in the alignment [default: 0.5].
  --min_cluster_size N    Min num of seqs selected for a motif [default: 10].
  --regex_th N            Min freq for a nt to be selected in the regex
                          expression [default: 0.3].
  --sample_size N         The num of sequences randomly sampled to
                          build the alignment for a motif [default: 200].
  --freq_th N             The min freq of a regex seq (use 0 to deactivate)
                          [default: 0.03].
  --std_th N              The max standard deviation for the localization of a
                          rgex seq (use 0 to deactivate) [default: 25].
  -h --help               Show this screen.
  --version               Show version.
  --verbose               Print more text.
```
