### Gibbs Sampler for Motif Finding
This repository contains an implementation of the Gibbs Sampler algorithm for motif finding in DNA sequences. The algorithm uses random sampling and nucleotide frequency profile construction to identify the most probable motifs in a set of input sequences.

### Code Structure

The code is structured as follows:

### 1. gibbs_sampler function: The main function that executes the Gibbs Sampler algorithm.

### 2. random_motifs function: Generates an initial set of random motifs from the provided DNA sequences.

### 3. profile_most_probable function: Finds the most probable motif based on a probability profile.

### 4. profile_from_motifs function: Calculates the probability profile from a set of motifs.

### Functions
gibbs_sampler(dna, k, t, N)

Runs the Gibbs Sampler algorithm to find the best motifs from the provided DNA sequences.

### Parameters:
dna: List of DNA sequences.
k: Length of the motif to be found.
t: Number of DNA sequences.
N: Number of iterations to be performed.

### Returns:

A list of found motifs.

random_motifs(dna, k, t)
Generates random motifs from the provided DNA sequences.

### Parameters:

dna: List of DNA sequences.

k: Length of the motif.

t: Number of sequences.

### Returns:

A list of random motifs.
profile_most_probable(text, k, profile)
Finds the most probable motif in a DNA sequence based on the provided probability profile.

### Parameters:
text: The DNA sequence.
k: Length of the motif.
profile: The nucleotide probability profile.

### Returns:

The most probable motif.
profile_from_motifs(motifs)
Calculates the nucleotide probability profile from a set of motifs.

### Parameters:

motifs: List of motifs.

### Returns:

A probability profile for nucleotides.

### Example Usage
```
# Example DNA sequences
dna = ["AGCTTAGG", "CGTACGGA", "AGTTCGGA", "GCTTAGGA"]

# Set motif length, number of sequences, and iterations
k = 3
t = len(dna)
N = 1000

# Run the Gibbs Sampler
motifs = gibbs_sampler(dna, k, t, N)

print(motifs)
```
### Dependencies
This implementation relies on basic Python libraries. Ensure you have the following installed:

Python 3.x
random
collections

### License
This project is licensed under the MIT License - see the LICENSE file for details.




