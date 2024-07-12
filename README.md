# Assembling-Genome

1. <b><u>kmer_comp</u></b>: Finds the kmers in a <b>Text</b> based on the length <b>k</b> of the k-mer

2. <b><u>PathtoGenome</u></b>: Given the <b>path</b> that the kmers follow, the genome has to be constructed. Path is defined by: A sequence of k-mers Pattern(1),...,Pattern(n) such that the last k - 1 symbols of Pattern(i) are equal to the first k - 1 symbols of Pattern(i+1) for
 1 <= n - 1.