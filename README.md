# Gibbs Motif Finder

This repository contains a basic Python implementation of the Gibbs Sampling algorithm for motif discovery in DNA sequences. This technique is commonly used in bioinformatics to identify conserved patterns, such as transcription factor binding sites, across multiple sequences.

## Description

The Gibbs Sampling algorithm applies a stochastic approach to explore the space of possible motifs. At each iteration, one sequence is randomly excluded, a profile is built from the remaining motifs, and a new motif is sampled from the excluded sequence based on the profile. This strategy helps avoid local optima and improves convergence.

Pseudocounts are used in the profile matrix to prevent zero probabilities.

## Input

- `dna`: A list of `t` DNA sequences (strings).
- `k`: Length of the motif to be searched.
- `t`: Number of sequences.
- `N`: Number of iterations of the sampler.

## Main Functions

- `gibbs_sampler(dna, k, t, N)`: Executes the Gibbs Sampling algorithm.
- `random_motifs(dna, k, t)`: Generates an initial set of random motifs.
- `profile_from_motifs(motifs)`: Constructs a profile matrix with pseudocounts.
- `profile_most_probable(text, k, profile)`: Returns the most probable k-mer in a sequence according to the profile.

## Example Usage

```python
k, t, N = 15, 20, 2000
motifs = gibbs_sampler(dna, k, t, N)
print(motifs)
