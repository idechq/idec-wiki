# Phage-assisted continuous evolution (PACE) and Phage-assisted noncontinuous evolution (PANCE)

## Introduction
Phage-assisted continuous evolution (PACE) and its noncontinuous variant (PANCE), developed by Esvelt et al. 2011[^1]. This method offers the possibility to continuously mutate and select proteins with the help of M13 bacteriophages. Effectively, within the PACE process M13 is allowed to propagate whenever the gene of interest (GOI), which is incorporated into the phage genome, is active.
PACE is one of a few directed evolution methods which are continuous. Non-continuous evolution methods usually start with the diversification of the target, then functional mutants from the library are selected. These functional mutants can then be used as a basis for the next round of diversification to improve their properties. Continuous evolution methods enable an uninterrupted diversification and selection of the target and thus promise faster results. For PACE more than 100 rounds of selection can be performed within 2 weeks (Miller et al. 2020).
So why don’t we use continuous evolution methods all the time? Continuous evolution methods are usually very complex to set-up. The crucial condition to make continuous evolution work is to apply selection pressure onto the GOI and not to the host organism. Some methods do so by introducing targeted mutagenesis methods (e.g. EvolvR (Halperin et al. 2018) or error-prone DNA-polymerases (Camps et al. 2013) or T7 RNA-polymerase systems (https://www.nature.com/articles/s41587-019-0331-8)). In PACE, the target gene is encoded by an M13 phage and the selection pressure is applied to Escherichia coli cells (Badran et al. 2015).
So how does PACE work?
For PACE M13 bacteriophages are used, the same are used in Phage Display(link). M13 phages infect E. coli and establish a ‘chronic infection’ with an average generation time around 15 min (Barbas et al. 2001). The phage consists of a single-strand DNA genome encapsulated by five coat proteins. The coat protein relevant for PACE is pIII, which is essential for phage infectivity. 
The basic principle of PACE is to replace the CDS of the pIII coat proteins by the CDS of the target gene which shall be evolved. The pIII gene is located on an accessory plasmid and its expression is activated in response to the activity of the protein of interest. Thus the only phage that bears a functioning protein of interest is allowed to propagate in the culture. Furthermore, the E. coli cells carry a mutagenesis plasmid which enables ongoing mutation of the selection phage. Through this set-up, two possible scenarios can happen when the selection phage infects a cell:
The selection phage already carries a functional target gene or the mutation plasmid causes mutations which are beneficial for target functionality resulting in the target gene enabling pIII expression and infectious phages are produced and assembled, which can then infect other cells
The selection phage carries a non-functional target gene or the mutation plasmid introduces mutations which inhibit the target functionality resulting in the target gene not enabling pIII expression and no infectious phages are produced
In theory, PACE does not represent a method for targeted mutation since usually whole-genome mutators are used. However, due to the fast replication rate of the phages, the phages have a higher mutation rate and even if a selection plasmid is mutated and “wrong” phages are produced, these will be selected in the cells they infect next.
PACE is usually performed in a continuous cultivation set-up. In this set-up, the E. coli host cells are cultivated as a fed-batch cultivation and these host cells are used as feed for the actual cultivation where the evolution happens – the lagoon. In the lagoon, the phages are able to replicate under a continuous feed of the host cells and a continuous outflow of waste (phages and cells). 

To better understand the basic principle, we will take a look at an example project using PACE: The evolution of a T7-RNA polymerase to recognize another promoter described by Esvelt et al. 2011.
To evolve the polymerase, the CDS of pIII was replaced by the CDS of the T7-polymerase. The plasmid responsible for the selection pressure carried the CDS of pIII downstream of a T3/T7 hybrid promoter. 
The selection phages are replicated using a strain that can express pIII, producing functional phages with genomes encoding the T7-RNA polymerase CDS.
These phages can then infect the cells carrying the plasmid with pIII under the control of the T3/T7 hybrid promoter. If the mutation plasmid introduces mutations that enable the polymerase to recognize the new promoter, pIII is expressed and functional phages are assembled. These phages can then infect new host cells and will be mutated and selected again. 
Next to the T7-RNA polymerase, directed evolution using PACE has been used to evolve for example TALE array proteins (Hubbard et al. 2015), Cas9 variants (Hu et al. 2018; Miller et al. 2020), protein-protein interactions using a two-hybrid system (Badran et al. 2016), tRNA/aminoacyl-synthetases (Bryson et al. 2017), and base-editors (Thuronyi et al. 2019).

So what are the requirements and challenges using PACE to evolve your protein of choice?
A very detailed protocol about requirements, how to set-up, and troubleshoot PACE (and PANCE) experiments is published by Miller et al. 2020. 
In short: The crucial condition to use PACE is that the functionality of the target protein needs to be linkable to pIII expression. 
Furthermore, the start of the directed evolution process can pose a challenge. When the target protein has little or no activity, even after mutation by the selection plasmid, the phages can be washed out of the continuous system. In this case, an adaption of the selection pressure or a switch to phage-assisted non-continuous evolution (PANCE) are possible choices. PANCE, in general, is probably the easier method when getting started with phage-assisted evolution, since it avoids the set-up of the continuous cultivation set-up.


## References

[^1]: Esvelt, K. M., Carlson, J. C. & Liu, D. R. A system for the continuous directed evolution of biomolecules. Nature 472, 499–503 (2011)



Badran, A. H. & Liu, D. R. In vivo continuous directed evolution. Curr. Opin. Chem. Biol. 24, 1–10 (2015)
Badran, A. H. et al. Continuous evolution of Bacillus thuringiensis toxins overcomes insect resistance. Nature 533, 58–63 (2016)
Barbas, C. F. Phage Display: A Laboratory Manual. Cold Spring Harbor Laboratory Press (2001)
Bryson, D. I. et al. Continuous directed evolution of aminoacyl-tRNA synthetases. Nat. Chem. Biol. 13, 1253–1260 (2017)
Camps, M., Naukkarinen, J., Johnson, B. P & Loeb, L. A. Targeted gene evolution in Escherichia coli using a highly error-prone DNA polymerase I. PNAS 100 (17), 9727-9732 (2003)

Halperin, S. O., Tou, C. J., Modavi, C., Schaffer, D. V. &Dueber, J. E. CRISPR-guided DNA polymerases enable diversification of all nucleotides in a tunable window. Nature 560, 248-525 (2018)
Hu, J. H. et al. Evolved Cas9 variants with broad PAM compatibility and high DNA specificity. Nature 556, 57–63 (2018)
Hubbard, B. P. et al. Continuous directed evolution of DNA-binding proteins to improve TALEN specificity. Nat. Methods 12, 939–942 (2015)
Miller, S. M., Wang, T. & Liu, D. R. Phage-assisted continuous and non-continuous evolution. Nature Protocols 15, 4101-4127 (2020)
Miller, S. M. et al. Continuous evolution of SpCas9 variants compatible with non-G PAMs. Nat. Biotechnol. 38, 471–481 (2020)
Thuronyi, B. W. et al. Continuous evolution of base editors with expanded target compatibility and improved activity. Nat. Biotechnol. 37, 1070–1079 (2019)





