# iDEC 2026 Challenge

*Engineering Inducible Control of Bacterial Conjugation*

A common engineering objective, a standardized comparison framework and a transparent map of the public methods and materials underlying the Challenge.

## Challenge objective

The iDEC 2026 Challenge asks teams to engineer an inducible regulatory system that controls the conjugation efficiency of **pRK24**, or an approved pRK24-derived variant. The aim is to preserve strong transfer when the system is induced and suppress transfer when it is uninduced.

- **ON state:** conjugation efficiency should approach that of the original pRK24 control.
- **OFF state:** conjugation efficiency should approach the experimental detection limit.

The standardized regulatory input is L-arabinose acting through the P_BAD-controlled expression cassette of **pAJM.677**. Teams replace the defined reporter region with a protein-coding or RNA-coding regulator capable of controlling the conjugation machinery. The Challenge is evaluated separately from the main iDEC project track.

pRK24 is publicly catalogued through Addgene as bacterial strain #51950 and is documented in the Conjugative Assembly Genome Engineering protocol. pAJM.677 is an arabinose sensor from the Voigt laboratory's Marionette system, catalogued as Addgene plasmid #108530; its sensor includes an engineered AraC (AraCAM), AraE and a P_BAD-YFP reporter. [3][4][5][6]

### Scientific concept and public-source basis

The general principle of linking a gene product's activity to cell-to-cell nucleic-acid transfer is described in public continuous-evolution patent literature. The Esvelt–Liu disclosure includes conjugal transfer among possible transfer mechanisms. [1]

A later Thuronyi–Wilson–Liu disclosure describes conjugation-dependent transfer linked to gene activity, including an embodiment involving TraA or TraQ and an F plasmid lacking the corresponding gene or genes. [2]

The experimental procedures and evaluation criteria below provide a common framework for comparing team designs using publicly documented biological materials and methods.

## Public materials and method provenance

The biological materials and experimental methods described below are based on previously published research, public protocols and repository records. References accompany the relevant materials and procedures. Public availability does not remove applicable repository terms, material-transfer agreements or intellectual-property requirements.

Teams must obtain biological materials independently through their institutions or recognized repositories and comply with the relevant access terms and institutional procedures. **iDEC does not provide, privately distribute or broker biological materials for the Challenge.**

| Material or method | Public source | Application |
|---|---|---|
| Function-dependent transfer | Public patent disclosures [1][2] | Conceptual basis for linking biological activity to DNA transfer. |
| pRK24 | CAGE protocol; Addgene #51950 [3][4] | Conjugative plasmid used as the transfer system. |
| pAJM.677 | Marionette publication; Addgene #108530 [5][6] | Arabinose-responsive expression system and YFP control. |
| P_BAD/AraC regulation | Arabinose expression-vector study [7] | Established basis of arabinose-inducible expression. |
| RiboJ insulation | Ribozyme insulator study [8] | Ribozyme-mediated insulation of the expression cassette. |
| Sequence verification and RCA | Repository sequence records; Phi29 RCA study [4][6][9] | Sequence checks; optional amplification of circular plasmid DNA. |
| Six-hour culture and fluorescence readout | CRISPRa methods; Marionette reporter [13][5][6] | 100-fold dilution, 6-hour culture, 1 mL deep-well format; fluorescence/absorbance measurement and correction. |
| Filter mating | Conjugation on filters; Xu et al. [10][14] | Public filter-conjugation format, including 0.2 µm cellulose acetate membranes on non-selective LB agar. |
| Selective CFU enumeration | Published conjugation assays [11] | Example of enumerating transconjugants relative to donors. |
| Plasmid maintenance | Published stability-measurement background [12] | Assessing plasmid stability during culture. |

**Handling the deposited strain:** the Addgene pRK24 deposit is listed at 30°C, with depositor advice to culture the deposited strain at 32°C or below. Follow these handling instructions when propagating the received strain. [4]

## Standardized experimental framework

Use the procedures below for construct preparation, induction, conjugation measurements and plasmid maintenance assays. Perform the required controls and report the results as specified.

### Required plasmids and sequence boundaries

| Plasmid | Required configuration | Use |
|---|---|---|
| Original pAJM.677 | Original YFP expression cassette | Arabinose-induction fluorescence control |
| Engineered pAJM.677-X/Y | Kanamycin-resistant; replace the permitted RBS/YFP region with gene X encoding one or more regulatory proteins, or gene Y encoding one or more regulatory RNAs | Donor, together with original pRK24 or an approved variant |
| Recipient pAJM.677 derivative | The same engineered construct, with its original kanamycin-resistance gene replaced by a chloramphenicol-resistance gene | Recipient identification and selection after conjugation |

The public parent construct is **pAJM.677, Addgene #108530**, associated with the Marionette publication. Its arabinose-responsive cassette and RiboJ context are documented by the parent-plasmid record and the relevant original studies. [5][6][7][8]

For the primary regulator construct, **replace only the specified region between RiboJ and the terminator**. The permitted 769-nt replacement interval is shown below, 5′ to 3′. The parent plasmid is pAJM.677 (Addgene #108530). [6]

```
cctctacaaataattttgtttaatactagagaaagaggggaaatactagatggtgagcaagggcgaggag
ctgttcaccggggtggtgcccatcctggtcgagctggacggcgacgtaaacggccacaagttcagcgtgt
ccggcgagggcgagggcgatgccacctacggcaagctgaccctgaagttcatctgcaccacaggcaagct
gcccgtgccctggcccaccctcgtgaccaccttcggctacggcctgcaatgcttcgcccgctaccccgac
cacatgaagctgcacgacttcttcaagtccgccatgcccgaaggctacgtccaggagcgcaccatcttct
tcaaggacgacggcaactacaagacccgcgccgaggtgaagttcgagggcgacaccctggtgaaccgcat
cgagctgaagggcatcgacttcaaggaggacggcaacatcctggggcacaagctggagtacaactacaac
agccacaacgtctatatcatggccgacaagcagaagaacggcatcaaggtgaacttcaagatccgccaca
acatcgaggacggcagcgtgcagctcgccgaccactaccagcagaacaccccaatcggcgacggccccgt
gctgctgcccgacaaccactaccttagctaccagtccgccctgagcaaagaccccaacgagaagcgcgat
cacatggtcctgctggagttcgtgaccgccgccgggatcactctcggcatggacgagctgtacaagtaa
```

This interval includes the original RBS and YFP coding sequence. Protein-coding designs may use a team-selected or designed RBS. RNA-coding designs should express the intended RNA regulator within the P_BAD-controlled context. Apart from the required recipient resistance-marker replacement described above, no other pAJM.677 region may be changed for the primary Challenge construct without explicit iDEC HQ approval.

Report the inserted DNA sequence; the RBS, coding sequence and predicted protein sequence where applicable; the RNA design and predicted function where applicable; the proposed mechanism for regulating pRK24 conjugation; and sequence-confirmation evidence. For sequences obtained from existing work, give the publication, repository identifier or accession and version. For designed or modified sequences, identify the starting sequence and describe the changes.

### pRK24 verification and permitted engineering

Use original pRK24 or an approved pRK24 variant. The public material and associated CAGE protocol are available through Addgene #51950 and Ma et al. [3][4] The received plasmid may differ from the website sequence. Teams are strongly encouraged to sequence the actual working material. Report the final sequence used for design, its source record and all confirmed differences. NGS is recommended; if direct cell-lysate DNA is insufficient, rolling-circle amplification followed by sequencing is an option. Phi29 RCA is an established method for amplifying circular plasmid DNA. [9]

Transfer of pRK24 by conjugation into a stable standard laboratory *E. coli* host, such as TOP10, DH10B or NEB 10-beta / NEB10B, is recommended as soon as possible because the original Addgene host may show instability. Preserve the resulting strain as the working source. Follow the depositor's handling instructions when culturing the received Addgene strain. [4]

- Carried *E. coli* genomic DNA fragments may be removed.
- If pRK24-encoded genes are supplied in trans from engineered pAJM.677 to regulate conjugation, the corresponding native genes may be removed from pRK24.
- Minimal variants may be explored provided they remain maintainable, transferable and measurable.
- **Retain the tetracycline-resistance marker** and all markers required for donor maintenance, transconjugant selection, CE calculation and comparison with original pRK24.

### Strains, selection and biological replication

| Strain | pRK24 | pAJM.677 | Main purpose |
|---|---|---|---|
| Donor 1 | Original | Original YFP | Original-pRK24 reference and fluorescence induction control |
| Donor 2 | Engineered variant | Original YFP | Control for the pRK24 engineering effect and quantitative induction characterization |
| Donor 3 | Engineered variant | Kan-resistant engineered X/Y | Main engineered system and non-fluorescent control |
| Recipient | Absent before mating | Chl-resistant engineered derivative | Recipient-derived transconjugant selection |

Maintain donors in LB with **tetracycline (Tet) 10 µg/mL + kanamycin (Kan) 50 µg/mL**. Maintain recipients in LB with **chloramphenicol (Chl) 25 µg/mL**.

Use **at least three independent biological replicates** for OD_600, YFP fluorescence, donor and transconjugant counts, maintenance assays, all required controls, figures and scoring metrics. Each biological replicate starts from an independent colony or independently grown overnight culture and undergoes independent induction, mating, recovery, dilution, plating and counting. Technical replicates may supplement but cannot replace biological replicates.

### Day 1 — Overnight cultures

For each strain and biological replicate, pick a single colony into **200 µL LB** in a 96-well plate. Add Tet 10 µg/mL + Kan 50 µg/mL for each of the three donor groups, or Chl 25 µg/mL for the recipient. Incubate at **37°C, 800–1000 rpm, for 16–20 hours**.

### Day 2 — Six-hour induction and recipient preparation

The culture and induction procedure is adapted from Liu, Wan and Wang, *Engineered CRISPRa enables programmable eukaryote-like gene activation in bacteria*. Prepare donor and recipient cultures in sterile deep-well 96-well plates using the conditions below. [13]

| Parameter | Donors: each strain, replicate and induction condition | Recipients: each strain and replicate |
|---|---|---|
| Plate | Sterile deep-well 96-well plate | Sterile deep-well 96-well plate |
| Fresh medium | 990 µL LB with Tet 10 µg/mL, Kan 50 µg/mL and the required arabinose concentration | 990 µL LB with Chl 25 µg/mL |
| Inoculum | 10 µL donor overnight culture | 10 µL recipient overnight culture |
| Final culture volume | 1 mL | 1 mL |
| Dilution | 1:100 | 1:100 |
| Final arabinose concentrations | 0, 0.1, 1, 10, 100 and 1000 µM | No arabinose induction required |
| Incubation | 37°C, 800–1000 rpm, 6 hours | 37°C, 800–1000 rpm, 6 hours, in parallel with donors |
| Fluorescence measurement | YFP control donors as described below | Not required |

**Recipients require neither arabinose induction nor fluorescence measurement.**

### Day 2 — PBS resuspension and plate-reader measurement

1. After the 6-hour culture, centrifuge the donor and recipient plates to pellet the cells, then carefully remove the supernatant.
2. Resuspend each donor pellet and each recipient pellet in **1 mL sterile PBS**. Mix thoroughly but gently.
3. For donors carrying **engineered pRK24 + original pAJM.677-YFP**, transfer **200 µL** of each PBS-resuspended sample into a black-wall, transparent-bottom 96-well plate. Include **three blank wells containing 200 µL PBS each**.
4. Measure OD_600 and YFP fluorescence, retaining the original-pRK24 + original-pAJM.677 fluorescence control and the appropriate non-fluorescent control.
5. Retain the remaining donor suspension for mating. Calculate the actual mating input using the 1 cm pathlength OD normalization below.

Report raw OD_600, raw fluorescence, background-subtracted fluorescence, OD-normalized fluorescence, arabinose concentration, biological replicate number, plate-reader model, excitation and emission wavelengths, and gain. Fluorescence and absorbance measurements, blank correction and use of a non-fluorescent control are based on published gene-expression assays. [13]

### Day 2 — Conjugation on a cellulose acetate membrane surface

Filter mating is adapted from Brown's *Conjugation on filters* protocol and the cellulose acetate membrane-surface method described by Xu et al. [10][14]

#### Prepare the mating surface

Use non-selective LB agar. With lids open in a sterile environment, dry the plates for approximately **2 hours**, adjusting for ambient humidity. Place a **sterile 0.2 µm cellulose acetate membrane** directly on the dried agar. Report membrane material, pore size, diameter, supplier, catalogue number and the agar medium beneath the membrane.

#### Normalize and combine the cells

Measure the PBS-resuspended donor and recipient OD_600 with a standard spectrophotometer using a **1 cm pathlength**, or an equivalent setting calibrated to 1 cm. Plate-reader OD values must not be used directly for cell-input normalization unless calibrated against that standard.

For every arabinose condition and biological replicate, combine the equivalent of **0.5 mL donor cells at OD_600 = 1** and **0.5 mL recipient cells at OD_600 = 1**, giving a 1:1 OD-normalized input ratio. Calculate the volume for each suspension separately:

!!! formula ""
    Volume used (mL) = 0.5 / OD_600

| Measured OD_600 (1 cm) | Volume of that suspension |
|---|---|
| 1.0 | 0.5 mL |
| 2.0 | 0.25 mL |
| 0.5 | 1.0 mL |

Centrifuge the mixed cells, carefully remove the supernatant and resuspend the combined pellet in **10–15 µL sterile PBS**.

#### Spot and incubate

Spot the entire **10–15 µL** suspension onto the centre of the cellulose acetate membrane. Allow the droplet to absorb until the surface is no longer visibly wet, then close the lid. Incubate at **37°C for 1 hour**. Report the actual temperature and exact mating duration.

### Recovery, five-fold dilution and Day 3 colony counting

1. After the 1-hour mating, transfer the membrane to a sterile tube, add **1 mL sterile PBS** and recover the cells by strong vortexing.
2. Prepare a **five-fold serial dilution series** of each recovered mixture.
3. Spot the dilution series onto the two selective plate types below.
4. After overnight incubation, count colonies from countable dilution spots. Record raw Tet + Kan and Tet + Chl counts, dilution factors, the spot volume used, and the calculated donor and transconjugant CFU.

| Readout | Selective LB agar | Interpretation |
|---|---|---|
| Donor CFU | Tet 10 µg/mL + Kan 50 µg/mL | Donor cells carrying pRK24 and the Kan-resistant pAJM.677 construct |
| Transconjugant CFU | Tet 10 µg/mL + Chl 25 µg/mL | Recipient-derived cells: Chl identifies the recipient construct, and Tet indicates pRK24 acquisition |

!!! formula ""
    CE = CFU on Tet + Chl / CFU on Tet + Kan

Selective enumeration provides the donor and transconjugant CFU used to calculate conjugation efficiency. [11] Calculate one CE value per arabinose concentration per biological replicate.

### Matched original-pRK24 reference and required controls

Measure the original pRK24 + original pAJM.677-YFP reference with the same host background, recipient strain, filter protocol, mating time, recovery volume, dilution scheme and selective plating conditions as the engineered system. Its mean CE supplies the reference denominator for ON-state retention and OFF-state leakage.

1. Original pRK24 + original pAJM.677 fluorescence induction control.
2. Original pRK24 conjugation control.
3. Donor-only control on Tet + Chl, using the equivalent of 0.5 mL at OD_600 = 1.
4. Recipient-only control on Tet + Chl, using the equivalent of 0.5 mL at OD_600 = 1.
5. Selection control confirming donor growth on Tet + Kan.
6. Selection control confirming recipient growth on Chl.
7. Selection control confirming that recipient-only cells do not grow on Tet + Chl.

These controls address toxicity, growth defects, contamination, altered antibiotic resistance, plasmid loss and selection artefacts as alternative explanations for changes in measured CE. Include at least three independent biological replicates.

### Mandatory 48-hour pRK24 maintenance assay

Compare original and engineered pRK24 in **LB with tetracycline** and **LB without tetracycline**. Start from a **1:100 dilution of an overnight culture** and culture for **48 hours at 37°C, 800–1000 rpm**, with a passage every **12 hours**. The schedule is **0, 12, 24, 36 and 48 hours**.

Report host strain, culture volume, passage dilution ratio, tetracycline concentration, incubation temperature, shaking speed and biological replicate number. After 48 hours, serially dilute and spot plate on LB + tetracycline for all four groups:

- Original pRK24, passaged with tetracycline.
- Original pRK24, passaged without tetracycline.
- Engineered pRK24, passaged with tetracycline.
- Engineered pRK24, passaged without tetracycline.

Use at least three independent biological replicates per group. Report tetracycline-resistant CFU. Additional non-selective LB plating is encouraged: a normalized retention fraction requires total viable CFU as well as tetracycline-resistant CFU. For further reading on plasmid stability measurement, see Chen et al. [12]

## Quantitative evaluation

Conjugation efficiency (CE) is the ratio of recipient-derived transconjugant CFU to donor CFU in the recovered mating mixture. Enumerate transconjugants on Tet + Chl plates and donors on Tet + Kan plates.

!!! formula ""
    CE = CFU_transconjugant / CFU_donor = CFU_Tet + Chl / CFU_Tet + Kan

Let CE_ref be the mean CE of the matched original pRK24 control. CE_ON and CE_OFF are the engineered-system CE values at 1000 µM and 0 µM L-arabinose, respectively. Report CE as mean ± standard deviation across at least three biological replicates.

| Metric | Definition | Interpretation |
|---|---|---|
| ON-state retention | R_ON = CE_ON / CE_ref | Retention of reference transfer efficiency under full induction. |
| OFF-state leakage | L_OFF = CE_OFF / CE_ref | Background transfer relative to the original pRK24 control. |
| Induction fold change | F = (CE_ON − CE_OFF) / CE_OFF | Increase above the uninduced baseline. |
| Robustness | Q_robust = 1 / (1 + CV_avg) | Reproducibility across biological replicates; CV_avg is the mean coefficient of variation across the six induction conditions. |

### Rules applied for scoring

- Cap R_ON at 1.0 when calculating the score.
- If L_OFF exceeds 1, treat the leakage term (1 − L_OFF) as zero.
- When no OFF-state transconjugant colonies are detected, report the result as below the detection limit and use the experimentally determined detection limit as the denominator in the fold-change calculation. A non-detection must not be reported as measured zero.
- Use F_scoring = min(F, 10,000). Report the observed or detection-limit-based F as well as the capped value used for scoring.

!!! formula "emphasis"
    S = min(R_ON, 1)² × log₁₀(F_scoring + 1) × max(1 − L_OFF, 0)² × Q_robust

The score combines ON-state transfer, OFF-state leakage, inducible range and reproducibility, with the retention cap and leakage rule included explicitly.

The summary table must include CE_ref, CE_OFF, CE_ON, R_ON, L_OFF, F, CV_avg, Q_robust and S. Detection limits and any quantity that cannot be calculated must be stated transparently rather than assigned an arbitrary value.

## Reproducibility, reporting and timeline

Team documentation must enable independent assessment of construct design, experimental performance and score calculation. Include construct designs, plasmid maps and sequences with source references, sequence-confirmation evidence, experimental protocols, raw and processed data, biological replicate information, the required figures and scoring table, and all deviations from the standard procedure.

### Required figures

Each figure must show error bars from **at least three independent biological replicates**. Use standard deviation unless otherwise stated.

| Figure | Required comparison | Axes and display |
|---|---|---|
| 1. Induction and conjugation response | Original-pAJM.677 YFP fluorescence and engineered-system CE under matched 0, 0.1, 1, 10, 100 and 1000 µM arabinose conditions | Line plot; x-axis: arabinose concentration; y-axes: normalized YFP fluorescence and CE. Use two y-axes, or scale each series to its own maximum. |
| 2. Full-induction conjugation | Original-pRK24 control versus engineered system at 1000 µM arabinose | Bar chart; y-axis: CE = Tet + Chl CFU / Tet + Kan CFU. |
| 3. Plasmid maintenance | 48-hour results for original and engineered pRK24, each passaged with and without tetracycline | Bar chart with all four groups; y-axis: tetracycline-resistant CFU, or normalized retention if total viable CFU was also measured. Non-selective LB plating is encouraged. |

### Required scoring summary table

Include all nine items: CE_original pRK24; engineered CE at 0 µM; engineered CE at 1000 µM; ON-state retention; OFF-state leakage; induction fold change; CV_avg; Q_robust; and final score S. Report CE as mean ± standard deviation from at least three independent biological replicates. Apply the definitions, detection-limit handling and scoring caps in Quantitative evaluation.

### Additional comparisons and deviations

Additional figures are encouraged where useful. If multiple engineering strategies are tested, present separate comparisons of their performance under the standardized metrics.

For every deviation, state what changed, why it changed, which samples or replicates were affected and whether comparisons with other teams are affected. Record failed experiments, negative results and troubleshooting on the team Wiki. Data completeness, transparency and reproducibility may be considered by the judging panel.

### Current Challenge timeline

**Challenge report deadline: 1 November 2026.** Challenge results are evaluated in the separate Challenge process, including the results presented at the November iDEC Festival. Teams submitting an independent non-Challenge project must also meet the separate main-track requirements.

**Challenge-team Wiki pages will temporarily be withheld from public display.** Teams must nevertheless maintain complete Wiki documentation for judging and subsequent release.

## Responsible research and intellectual contributions

### Responsible research and scope

The Challenge is intended for contained research with established non-pathogenic laboratory bacterial strains. Participation does not authorize environmental release, work with pathogenic organisms, clinical or environmental isolates, or experiments intended to expand the host range of conjugative elements or facilitate uncontrolled dissemination of antimicrobial-resistance determinants.

Each institution is responsible for biological-risk assessment, laboratory authorization, applicable regulations, material-transfer agreements, gene-synthesis requirements and responsible-research procedures. Teams must comply with iDEC's Responsible Research policy and their institutional requirements.

iDEC provides a common scientific question, a standardized comparison framework and transparent evaluation criteria. The underlying materials and methodological building blocks are identified through public sources.

### Authorship, data and intellectual contributions

Challenge outcomes may lead to follow-up research, collaborative publication or intellectual-property development involving iDEC HQ, the Challenge commissioner or organizer, and teams generating validated results. Teams should record who designed each construct, performed each experiment, generated and analyzed each dataset, and contributed to interpretation and reporting.

Any subsequent authorship or ownership arrangements should reflect actual scholarly contributions and the applicable policies of the participating institutions.

## References

Public-source links were checked on 6 October 2026.

1.  Esvelt KM, Liu DR. Continuous directed evolution of proteins and nucleic acids. Published US patent application US20110177495A1 (2011); granted as US9023594B2 (2015). See Summary of the Invention and claim 24. <https://patents.google.com/patent/US20110177495A1/en>
2.  Thuronyi B, Wilson CG, Liu DR. Methods and compositions for evolving base editors using phage-assisted continuous evolution (PACE). Published patent application WO2019023680A1 (2019). See paragraph [0221] for the conjugative-plasmid embodiment. <https://patents.google.com/patent/WO2019023680A1/en>
3.  Ma NJ, Moonan DW, Isaacs FJ. Precise manipulation of bacterial chromosomes by conjugative assembly genome engineering. Nature Protocols 9, 2285–2300 (2014). DOI: 10.1038/nprot.2014.081. <https://doi.org/10.1038/nprot.2014.081>
4.  Addgene. pRK24, bacterial strain #51950. Deposited by the Farren Isaacs laboratory. Material record, sequence information and depositor handling instructions. <https://www.addgene.org/51950/>
5.  Meyer AJ, Segall-Shapiro TH, Glassey E, Zhang J, Voigt CA. Escherichia coli "Marionette" strains with 12 highly optimized small-molecule sensors. Nature Chemical Biology 15, 196–204 (2019). DOI: 10.1038/s41589-018-0168-3. <https://doi.org/10.1038/s41589-018-0168-3>
6.  Addgene. pAJM.677, plasmid #108530. Deposited by the Christopher Voigt laboratory. AraCAM + AraE + PBAD-YFP reporter for use in non-Marionette strains. RRID: Addgene_108530. <https://www.addgene.org/108530/>
7.  Guzman LM, Belin D, Carson MJ, Beckwith J. Tight regulation, modulation, and high-level expression by vectors containing the arabinose PBAD promoter. Journal of Bacteriology 177, 4121–4130 (1995). DOI: 10.1128/JB.177.14.4121-4130.1995. <https://doi.org/10.1128/JB.177.14.4121-4130.1995>
8.  Lou C, Stanton B, Chen YJ, Munsky B, Voigt CA. Ribozyme-based insulator parts buffer synthetic circuits from genetic context. Nature Biotechnology 30, 1137–1142 (2012). DOI: 10.1038/nbt.2401. <https://doi.org/10.1038/nbt.2401>
9.  Dean FB, Nelson JR, Giesler TL, Lasken RS. Rapid amplification of plasmid and phage DNA using Phi29 DNA polymerase and multiply-primed rolling circle amplification. Genome Research 11, 1095–1099 (2001). DOI: 10.1101/gr.180501. <https://doi.org/10.1101/gr.180501>
10. Brown NF. Conjugation on filters. protocols.io, version 1 (2016). <https://www.protocols.io/view/Conjugation-on-filters-5jyl89bdv2wp/v1>
11. Bean EL, Herman C, Anderson ME, Grossman AD. Biology and engineering of integrative and conjugative elements: Construction and analyses of hybrid ICEs reveal element functions that affect species-specific efficiencies. PLOS Genetics 18, e1009998 (2022). DOI: 10.1371/journal.pgen.1009998. <https://doi.org/10.1371/journal.pgen.1009998>
12. Chen S, Larsson M, Robinson RC, Chen SL. Direct and convenient measurement of plasmid stability in lab and clinical isolates of E. coli. Scientific Reports 7, 4788 (2017). DOI: 10.1038/s41598-017-05219-x. <https://doi.org/10.1038/s41598-017-05219-x>
13. Liu Y, Wan X, Wang B. Engineered CRISPRa enables programmable eukaryote-like gene activation in bacteria. Nature Communications 10, 3693 (2019). DOI: 10.1038/s41467-019-11479-0. See Methods: "Strains and growth conditions", "Quantitative RT-PCR", "Gene expression assays" and "Calculation of fluorescence intensities". <https://doi.org/10.1038/s41467-019-11479-0> <https://pmc.ncbi.nlm.nih.gov/articles/PMC6710252/>
14. Xu J, Kim J, Koestler BJ, Choi JH, Waters CM, Fuqua C. Genetic analysis of Agrobacterium tumefaciens unipolar polysaccharide production reveals complex integrated control of the motile-to-sessile switch. Molecular Microbiology 89, 929–948 (2013). DOI: 10.1111/mmi.12321. See "Transposon mutagenesis" for mating on 0.2 µm cellulose acetate filters on non-selective LB agar. <https://doi.org/10.1111/mmi.12321> <https://onlinelibrary.wiley.com/doi/full/10.1111/mmi.12321>
