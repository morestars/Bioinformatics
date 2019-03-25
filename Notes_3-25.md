* Common ancestral sequence
  * Homology
    * Orthologs - linear descendants
      * diverge directly from common ancestor
      * similar function
    * Paralogs
      * human proteom, 4-5 versions for same protein
      * pp1, pp2, etc
      * branching process in divergence
      * paralogs are free to do different functions
      * found often in human genome
      * easy to misplace paralog reads

* Large-scale genome events
* Simplified model of evolution
  * Substitutions
  * Deletions
  * Insertions
  
* Similarity due to common ancestral line

* Tabular representation

* Pairwise sequence alignment
  * Match shared equivalent positions
  * Best way is not clearly defined
  
* Tabular
  * Index i and j with each of the nucleotide sequences
  * M(i,j) starts at M(0,0)
  * Coordinate system defination may change
  * This class will use top left of M(0,0)
  
* Insertion/deltions
  * Given by vertical movement in table
  
* Scoring system to quantify which alignment path is the best
  * matches
  * gaps

* Kimura scoring matrix
  * match --> 6
  * extra penalty for purine <--> pyrimidine changes
  
* Linear gap penalties favor shorter gaps
  * Penalty for many short gaps the same as one long gap
  
* Eqpsilon should be smaller than delta because opening the gap should be the biggest consideration for penalty vs the length of the gap

* Dynamic programming
  * 2 sequences, can extend each and then check
  
* top left zero is the empty string base case for programming

* Best global alignment is not necessarily biologically accurate
  * There is biological overlap for different areas
  * Need local alignment measures
  
* Local pairwise sequence alignment
  * allow 0 to be a choice
  * can't do worse than zero
  * while aligning subsequences, when getting negative scores, essentially reset with the zero value
  * start again for 
  * proteins have regular secondary structures
    * beta sheets in equivalent position, there will be high similarity
    * repetetive regions in DNA are difficult to align
    * focus on highly conserved  nucleotides
  * Do we set a pointer (i,j) = (0,0)?
    * No, we haven't aligned it yet
    * This is a region of no alignemnt
  * What about at (0,2)?
    * Yes
    
  * Backtrack over winning path
    * Might jsut be a short region of subsequence
    * Largest value in the matrix --> start here
    * Best local alignemnt is suboptimal because another alignment has the same score
    * Expected value of a random match must be negative
      * Allows us to stop aligning and reset
      
* Heiristic alignments
  * Quadratic time not optimal for large-scale problems
  * BLAST
    * First heuristic algorithm
    
* BLAST was too slow for high-throughput sequencing
* Speed over optimal solution
* High-throughput, efficient algorithms are under current study and development
  





