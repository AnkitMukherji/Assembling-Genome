# Assembling-Genome
<b><i>Definitions of functions used:</i></b>

1. <b><i>kmer_comp</i></b>: Finds the kmers in a <b>Text</b> based on the length <b>k</b> of the k-mer

2. <b><i>PathtoGenome</i></b>: Given the <b>path</b> that the kmers follow, the genome has to be constructed. Path is defined by: A sequence of k-mers Pattern(1),...,Pattern(n) such that the last k - 1 symbols of Pattern(i) are equal to the first k - 1 symbols of Pattern(i+1) for
 1 <= n - 1.

3. <b><i>OverlapGraph</i></b>: An adjacency list to find connection between nodes i.e. the kmers represented by <b>nodes</b>.

4. <b><i>DeBruijnGraph</i></b>: Constructing a DeBruijn Graph using the kmers(obtained from the given genome) as the edges and not nodes representing the path. Gluing the identically labeled nodes together reducing the number of nodes from <b>OverlapGraph</b> but keeping the number of edges the same. The output is an adjacency list.

5. <b><i>DeBruijnGraph_from_kmers</i></b>: As the sequence of the genome is not known, only reads from a sequencer or here unordered kmers <b>kmers</b> are known from which the DeBruijn Graph is constructed. The output is an adjacency list.