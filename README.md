# Quantum Phylogenetic Trees

In this repository, two methods are studied for the reconstruction of phylogenetic trees with a quantum-inspired technology: Fujitsu's Digital Annealer (DA).

The first method, called NMCutDA, is a reproduction of the paper 'Phylogenetic tree reconstruction via graph cut presented using a quantum-inspired computer' by Onodera et al. (2023). The method consists on breaking down the all-to-all graph of species with their similatiry matrix in order to reconstruct their phylogenetic tree. It is a divisive method that uses a MinCut QUBO with a penalization term and then a post-processing formula to choose the best cut.

The second method, called NJDA, is an original method consisting on adapting the classical Neighbor Joining to quantum technologies, allowing for paralelization and thus exploiting the capabilities of the Digital Annealer. It is a grouping method, or bottom-up, inspired by its classical counterpart. Several modifications have been implemented to better the efficiecy of the algorithm and reduce the resources needed to execute it.  

Other methods have also been compiled here, such as \verb|func_QUBOmod| (divisive method with a QUBO formulation based on modularity), \verb|func_Modularity| (same as NMCutDA but with modulatiry instead of Ncut post-processing) and \verb|func_back_mod| (the first attempt at a bottom-up method with modularity before NJDA). These have all been discared due to poor results and therefore are not updated.

Finally, helper functions are also listed: \verb|func_cleanfasta| (cleans FASTA files that are not properly formatted), \verb|func_filter_nodes| (lists trees and the number of nodes they have), \verb|Representaciones_graficas| (a compilation of all the drafts and code to print the figures present in the deliverable).

