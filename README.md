# SMoD
SequenceMotifDecomposer (SMoD) is a motif finder algorithm.


## Help

```
SequenceMotifDecomposer (SMoD) is a motif finder algorithm.

Version: 1.0
Author: Fabrizio Costa [costa@informatik.uni-freiburg.de]

Usage:
  smod --pos FILE (--neg FILE | -t N)  [-o PATH] [-c N] [-n N]
       [--min_subarray_size N] [--max_subarray_size N] [--similarity_th N]
       [--min_score N] [--min_freq N] [--min_cluster_size N] [--regex_th N]
       [--sample_size N] [--freq_th N] [--std_th N]
       [--verbose]
  smod (-h | --help)
  smod --version

Options:
  --pos FILE              Specify input fasta file for positive seqs.
  --neg FILE              Specify input fasta file for negative seqs.
  -t N                    The num of permutations for each positive
                          sequence [default: 1].
  -c N                    Feature complexity [default: 5].
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
