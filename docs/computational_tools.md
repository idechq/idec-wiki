# Computational tools (for library creation, design and analysis)

Combining computational algorithms with directed evolution allows experimental methods such as Combinatorial Saturation Mutagenesis, DNA recombination and epPCR to be performed in a more effective way, leading to biocatalysts with strong biotechnological potential while reducing the demands on screening. In recent years, different computational methods have emerged that take advantage of the thousands of sequences and structures deposited in gene and protein databases. Comprehensive reviews of these computational tools have been recently published (Damborsky and Brezovsky, 2014; Sebestova et al., 2014, Sequeiros-Borja et al., 2020), so here we will simply mention a few representative examples of the most common computational algorithms used to date.
https://academic.oup.com/bib/advance-article/doi/10.1093/bib/bbaa150/5879227?login=true

SCHEMA: This computational method allows libraries to be designed by recombination of several homologous sequences (with as little as 55 % identity) while maximizing the number of folded proteins (Voigt et al., 2002). SCHEMA predicts the fragments that must be inherited in the same parent, thereby allowing the computational selection of blocks from which novel proteins (chimeras) can be assembled. The selection of crossover locations is based on a metric for disruption, defined as the number of interactions of a hybrid protein that are broken when a given pattern of fragments is inherited from each of the parents (ie, the pairs of residues within 4.5 Å of each other that are not present as the same pair in any of the parents—defined as SCHEMA energy). This method requires a multiple sequence alignment of the parental sequences, a PDB file, and a UNIX-based computer.
Link:http://www.cheme.caltech.edu/groups/fha/old_website_2010.6.25/schema-tools/schema-overview.html
Application example: https://www.pnas.org/content/114/13/E2624#ref-10

MAP (Mutagenesis Assistant Program): MAP compares the different random mutagenesis methods available and their consequences in terms of mutational bias at the level of amino acid substitution (Wong et al., 2006b). MAP is used to predict the quality of the mutant library based on the epPCR method chosen and the nucleotide composition of the target gene. It works at three levels of information using three distinct indicators: (1) the protein structure indicator provides data about the likelihood of introducing stop codons and residues that destabilize the helical structure (Pro, Gly), (2) the amino acid diversity indicator shows the proportion of variants with preserved amino acids (ie, amino acids that do not change with a single nucleotide substitution—silent mutations—) and the average number of amino acid substitutions after a single nucleotide change, and (3) the chemical diversity indicator provides the chemical diversity generated in terms of amino acid substitution (aliphatic, aromatic, neutral, charged). The new version of the server (MAP2.0 3D) permits further mapping of the sequence indicators onto the target protein’s 3D structure, correlating the pattern of amino acid substitution with structural information regarding local interactions solvent accessibility, residual motility, and secondary elements. To work, MAP2.0 3D requires only the target gene sequence and a PDB file (or a homology model) of the protein.

Link: http://smap.win.biotec.rwth-aachen.de/

Application example/tutorial: 
https://daniloroccatano.blog/2018/03/23/bioinformatics-tools-for-protein-bioengineering-the-map-server/


3. HOT-SPOT WIZARD: This algorithm predicts hot-spot residues for CSM to modify activities and stability, precluding catalytic determinants from mutagenesis (Pavelka et al., 2009). For each individual amino acid, the tool gives information about the degree of mutability (and possible amino acid substitution at that position), functional and structural significance, and similar residues in related enzymes. The server integrates data from several bioinformatics databases allowing structural and evolutionary previews to be performed. The requirements to run HotSpot Wizard are minimal, only the PDB file of the target protein.
    
    Link: https://loschmidt.chemi.muni.cz/hotspotwizard/

  Application example/tutorial: 
  https://loschmidt.chemi.muni.cz/hotspotwizard/?action=usecases&



4. 3DM: The 3DM protein superfamily platform is a commercial database that is useful to explore sequence-function relationships (Kuipers et al., 2010). By superimposing protein family structures from different sources (including mutations reported in the literature), a structure sequence alignment provides valuable information about conserved residues and more mutable amino acids to create CSM libraries.

 Link: https://www.bio-prodict.com/

5. ProSAR (Protein Sequence Activity Relationship): This computational platform unmasks beneficial mutations from experimental mutant libraries (even from mutants with reduced function) to be incorporated into new iterative rounds of directed evolution. ProSAR follows the same principles that rule QSAR (an algorithm used for drug design) but applied to protein engineering to sort out beneficial, neutral, and detrimental mutations from a given mutant library in order to find new epistatic effects within a given protein scaffold (Fox et al., 2007).

6. ROSETTA: The Rosetta software suite for macromolecular modeling, docking, and design is widely used in pharmaceutical, industrial, academic, non-profit, and government laboratories. Considering its broad modeling capabilities, Rosetta consistently ranks highly when compared to other leading methods created for highly specialized protein modeling and design tasks. Developed for over two decades by a global community of scientists at more than 60 institutions, Rosetta has undergone multiple refactorings, and now comprises over three million lines of code. Among its many uses, the most common applications are: Predicting protein structures; modeling protein–protein and DNA/RNA-protein complexes; design/modeling antibodies and other immune system proteins;  designing new proteins and functions. A limitation of Rosetta is the need for a local installation and compilation in a Unix-like environment. Webservers provide a user-friendly alternative and a number of independent servers have emerged in our community. However, implementing and maintaining such servers comes at a substantial cost. To make it easier to provide protocols webservers, ROSIE (Rosetta Online Server that Includes Everyone) (http://rosie.rosettacommons.org/) implements a simple framework for “serverification” of protocols. ROSIE currently contains 21 webservers, with additional protocols continually being added.
Link: https://www.rosettacommons.org/
Application example/tutorial: 
https://www.rosettacommons.org/docs/latest/Home

More Rosetta Resources:
Macromolecular Modeling and Design in Rosetta: New Methods and Frameworks
https://www.preprints.org/manuscript/201904.0263/v3
Protocols for Molecular Modeling with Rosetta3 and RosettaScripts
https://pubs.acs.org/doi/abs/10.1021/acs.biochem.6b00444
Practically Useful: What the ROSETTA Protein Modeling Suite Can Do for You
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2850155/pdf/bi902153g.pdf
Rosetta comparative modeling for library design: Engineering alternative inducer specificity in a transcription factor
https://onlinelibrary.wiley.com/doi/full/10.1002/prot.24828?casa_token=5i7yAN1li_kAAAAA%3AXZ9Wi-G-H1f1QMrPV2z2-sdFTLatqt4r9T_pStOhHSUSRkhqGSj1mySkYhsmdiVqEQZbXEPHTj6IAw0
Rosetta Tutorials, Demos, and Protocol Captures
https://www.rosettacommons.org/demos/latest/Home

7. Machine-learning based approaches: An emerging alternative for screening protein function in silico is machine learning, which comprises a set of algorithms that make decisions based on data (10). By building models directly from data, machine learning has proven to be a powerful, efficient, and versatile tool for a variety of applications, such as extracting abstract concepts from text and images or beating humans at our most complex games (11, 12). Previous applications of machine learning in protein engineering have identified beneficial mutations (13) and optimal combinations of protein fragments (14) for increased enzyme activity and protein stability, as reviewed recently (15). 
Example/Application: Here we use machine learning to enhance directed evolution by using combinatorial libraries of mutations to explore sequence space more efficiently than conventional directed evolution with single mutation walks. The size of a mutant library grows exponentially with the number of residues considered for mutation and quickly becomes intractable for experimental screening. However, by leveraging in silico models built based on sampling of a combinatorial library, machine learning assists directed evolution to make multiple mutations simultaneously and traverse fitness landscapes more efficiently. In the machine learning-assisted directed evolution strategy presented here, multiple amino acid residues are randomized in each generation. Sequence–function information sampled from the large combinatorial library is then used to predict a restricted library with an increased probability of containing variants with high fitness. The best-performing variants from the predicted libraries are chosen as the starting points for the next round of evolution, from which further improved variants are identified. 
https://www.pnas.org/content/pnas/116/18/8852.full.pdf
 
A good and concise example of combining computational and experimental approaches:
In our last example, a good combination of dry and wetlab was employed. The IPTG responsive Transcription Factor LacI has been computationally redesigned and mutated to recognize four new non-native inducers (Taylor et al., 2016). This study is a good example of how the combination of computation-guided mutagenesis based on the Rosetta algorithm and different diversification techniques (such as epPCR and saturation mutagenesis) can accelerate the discovery/generation of new molecular functions. In a counter-selection round, the mutant libraries were pre-screened for retained ability to repress a TolC reporter (a porin that allows entry of toxic colicin E1) by growth enrichment in the absence of inducers but in the presence of colicin E1. The enriched LacI libraries were then positively screened by FACS for their ability to activate production of GFP upon induction with different sugars, resulting in variants of LacI that were responsive to fucose, gentiobiose, lactitol and sucralose (Taylor et al., 2016). In this instance, no active counter-screening was performed against activation by IPTG, so nearly all mutants retained their ability to respond to IPTG, a phenotype that was reduced for some designs upon shuffling of mutations for activity screening. https://academic.oup.com/nar/article/48/1/e3/5645005?login=true

Reviews
Computational tools for enzyme improvement: why everyone can – and should – use them
https://www.sciencedirect.com/science/article/pii/S1367593117300248
Computational Tools for Designing Smart Libraries
https://link.springer.com/protocol/10.1007%2F978-1-4939-1053-3_20
Protein computational design - recent review
https://www.sciencedirect.com/science/article/pii/S0734975021000021
From directed evolution to computational enzyme engineering—A review
https://aiche.onlinelibrary.wiley.com/doi/10.1002/aic.16847
Other examples:
CADEE: Computer-Aided Directed Evolution of Enzymes
https://journals.iucr.org/m/issues/2017/01/00/be5274/index.html
Machine learning-assisted directed protein evolution with combinatorial libraries
https://www.pnas.org/content/pnas/116/18/8852.full.pdf
Principles of Machine Learning Guided Protein Engineering https://dash.harvard.edu/handle/1/37365914
Discovery of Novel Gain-of-Function Mutations Guided by Structure-Based Deep Learning
https://pubs.acs.org/doi/pdf/10.1021/acssynbio.0c00345
Deep Dive into Machine Learning Models for Protein Engineering
https://pubs.acs.org/doi/10.1021/acs.jcim.0c00073
Underrated Machine Learning Papers for Protein Design
https://medium.com/proteinqure/underrated-machine-learning-papers-for-protein-design-applications-a846e294330
Deep Learning in Protein Structural Modeling and Design
https://www.cell.com/patterns/pdf/S2666-3899(20)30190-2.pdf

