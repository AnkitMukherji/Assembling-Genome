# Assembling-Genome
<b><i>Definitions of functions used:</i></b>

1. <b><i>kmer_comp</i></b>: Finds the kmers in a <b>Text</b> based on the length <b>k</b> of the k-mer

2. <b><i>PathtoGenome</i></b>: Given the <b>path</b> that the kmers follow, the genome has to be constructed. Path is defined by: A sequence of k-mers Pattern(1),...,Pattern(n) such that the last k - 1 symbols of Pattern(i) are equal to the first k - 1 symbols of Pattern(i+1) for
 1 <= n - 1.

3. <b><i>OverlapGraph</i></b>: An adjacency list to find connection between nodes i.e. the kmers represented by <b>nodes</b>.

4. <b><i>DeBruijnGraph</i></b>: Constructing a DeBruijn Graph using the kmers(obtained from the given genome) as the edges and not nodes representing the path. Gluing the identically labeled nodes together reducing the number of nodes from <b>OverlapGraph</b> but keeping the number of edges the same. The output is an adjacency list.

5. <b><i>DeBruijnGraph_from_kmers</i></b>: As the sequence of the genome is not known, only reads from a sequencer or here unordered kmers <b>kmers</b> are known from which the DeBruijn Graph is constructed. The output is an adjacency list.

6. <b><i>eulerian_cycle</i></b>: Constructing an eulerian cycle (basis of de_bruijn graph) from an adjacency list.

7. <b><i>eulerian_path</i></b>: An eulerian path is an eulerian cycle if the graph is balanced and the last node meets the first node i.e. it forms a cycle. Eulerian Path is a more realistic situation as constructing genome from reads cannot be balanced until we are working with a circular genome.

8. <b><i>String_Reconstruction</i></b>: From a set of unordered kmers, the DeBruijn Graph is formed with which the Eulerian Path is derived. This gives us the directed graph of nodes connected by directed edges. Using the nodes of the directed graph, the Genome is reconstructed.

9. <b><i>k-Universal Circular String</i></b>: Generating a circular string from all binary kmers of a specific length. We can construct a k-universal circular binary string by finding an Eulerian cycle in the de Bruijn graph constructed from the collection of all binary k-mers.
This was the problem solved by De Bruijn which is now applied to solved Genome Assembly Problem.

10. <b><i>paired_composition</i></b>: Generating read pairs rather than reads to simplify Genome Reconstruction from De Bruijn Graphs.