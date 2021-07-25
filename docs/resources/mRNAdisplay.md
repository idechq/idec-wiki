# Introduction

Both mRNA and cDNA display are based on in vitro transcription-translation systems. The rationale behind developing these two types of displays was to (1) eliminate the reliance on the formation of stalled ribosome complex which is unstable and prone to dissociation and (2), mRNA has known stability issues itself, hence the goal was to reverse transcribe it before performing the subsequent selection, respectively. These methods are typically used for finding protein-, peptide- or peptidomimetic binders. The main advantage of this method is library size that can theoretically reach 1015 mutants. This roughly corresponds to 12 randomised positions in a peptide. Additionally, performing selection in vitro gives control over a wide range of experimental conditions including the use of exotic chemistries (for the search of enzymes) and non-proteogenic modified amino acids in case of peptidomimetic selection.

# Principle of the mRNA and cDNA displays 

As opposed to the Ribosome display, where mRNA and the nascent chain (= protein or peptide) are physically connected via a stalled ribosome, in the mRNA display, a nascent chain gets attached covalently to its mRNA via the antibiotic puromycin, that is coupled to it.

Puromycin resembles 3’-end of tyrosyl-tRNA. Specifically, it contains para-methyl-tyrosine linked via a stable amide bond to 3’-amino group of the modified adenosine. Normally, its incorporation into the growing protein chain leads to the termination of protein synthesis. In the late 90s, the group of [Jack Szostak](https://www.pnas.org/content/94/23/12297.long) realised that puromycin can be linked to an oligonucleotide which, in turn, can also be ligated to mRNA. Thus translation of such mRNA-oligo-puromycin will eventually lead to the formation of a linkage between a newly translated protein and its encoding mRNA on the ribosome.

In the [cDNA display](https://academic.oup.com/nar/article-lookup/doi/10.1093/nar/gkp514), puromycin is attached to a branched DNA oligo which has two other functionalities: (1) biotin for quick removal of mRNA-DNA-protein from the in vitro translation system to avoid mRNA degradation (2) primer for reverse-transcription reaction and (3) restriction site for the release of the cDNA-protein complex from the beads for the subsequent selection.

Advantage of cDNA display include:
•	Effectively cancellation of mRNA instability.
•	In some instances mRNA can fold and thus also bind the bait which may bias the selection. cDNA typically does not have such property and thus selection is ‘cleaner’.
•	Puromycin-mRNA linkage is prepared cheaply and very effectively by the use of T4 DNA ligase
•	Translated protein/peptide which contains many disulphide bridges can be refolded after the cDNA synthesis and before selection.

# Challenges

Dealing with setting up an in vitro translation systems inherently requires optimisations depending on the type of protein to be selected or display techniques they are used in. Other potential problems may include:

•	mRNA display’s probably the main problem is that puromycin in the mRNA is inefficiently attached to the nascent chain. However, a plethora of optimisations have been done on this subject with regards to the sequence and length of the oligo [linkers between](https://www.sciencedirect.com/science/article/pii/S0168165615300997) puromycin and the [mRNA](https://link.springer.com/protocol/10.1007/978-1-4939-8648-4_14).
•	mRNA is very labile particularly in certain in vitro translation systems (Escherichia coli S30 extract)
•	The mRNA, cDNA and other homogeneous in vitro display methods are limited to the selection of binders. However, there are reports of [enzyme selection](https://www.nature.com/articles/nprot.2011.312). In all of them, only a single turnover reaction can be selected for. Ultimately, selection for the multiple turnover enzymatic reaction requires encapsulation of the mRNA(cDNA)-protein complex.
•	All of the homogeneous in vitro assays are poorly suitable for selection of membrane-associated proteins.

# Future directions

There is certainly a need to accommodate principles of mRNA or cDNA display for the use in a natural context - the cell. The main advantage of these methods is the coupling of every expressed protein to its corresponding cDNA/mRNA, the latter then can be efficiently detected as opposed to the low-sensitivity proteomics readouts. Starting from the report on high-throughput protein-protein interaction studied in vitro in [2014](https://www.nature.com/articles/s41467-020-16140-9) there was only one attempt so far to develop mRNA display [in vivo](https://doi.org/10.1073/pnas.2002650117) that was published in 2020.

Other potential avenues to further improve mRNA and cDNA display logically comes from their weak points described above. The issue of mRNA stability was largely addressed by utilising translation systems reconstituted from individual components ([PURE](https://www.authorea.com/doi/full/10.22541/au.159129081.14061266)). The same PURE-based system can also be used for the selection of enzymes due to the absence of the parasitic background activities in the translation mix.


