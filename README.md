# **HPV16: From Viral Genomics to Proteomics and Drug Discovery**

## **An Integrated In Silico Analysis of Human Papillomavirus Type 16**

# Project Overview

This project presents a complete bioinformatics workflow for the computational analysis of the Human Papillomavirus type 16 (HPV16) genome and the identification of potential inhibitors targeting the HPV16 viral oncoprotein.

The study combines genome annotation, comparative sequence analysis, protein characterization, homology modelling, ADMET prediction, binding pocket identification, and molecular docking to identify promising compounds against the viral protein.

The workflow also demonstrates how genome-scale analysis can guide target selection before structure-based drug discovery.

# Objectives

1. Retrieve and analyse the complete HPV16 genome
2. Predict coding regions and viral genes
3. Compare HPV16 with homologous viral sequences
4. Identify conserved nucleotide and protein regions
5. Characterize physicochemical properties of HPV proteins
6. Generate reliable 3D protein structures through homology modelling
7. Select the most suitable therapeutic target
8. Predict ligand binding pockets
9. Compare natural and synthetic compounds using docking and ADMET analysis
10. Identify potential HPV16 viral protein inhibitors

# Workflow

[HPV16 Genome Retrieval]
            →
[ORF Prediction]
            →
[Gene Prediction]
            →
[Genome Mapping]
            →
[Genome Annotation]
            →
[Genome Similarity Analysis]
            →
[Protein Similarity Analysis]
            →
[Multiple Sequence Alignment]
            →
[Conserved Region Analysis]
            →
[ProtParam Analysis]
            →
[Homology Modelling]
            →
[Target Selection]
            →
[Ligand Selection]
            →
[ADMET Prediction]
            →
[Binding Pocket Prediction]
            →
[Protein Preparation]
            →
[Ligand Preparation]
            →
[SwissDock Molecular Docking]
            →
[Interaction Visualization]
            →
[Comparative Analysis]
            →
[Potential HPV16 Protein Inhibitor Identification]

  # Bioinformatics Tools Used     

| Step | Tool / Server | Purpose |
|--------|---------------|----------|
| Genome Retrieval | [NCBI Database](https://www.ncbi.nlm.nih.gov/) | HPV16 genome retrieval |
| ORF Prediction | [NCBI ORF Finder](https://www.ncbi.nlm.nih.gov/orffinder/) | Detect coding regions |
| Gene Prediction | [GeneMark](http://exon.gatech.edu/GeneMark/) | Predict viral genes |
| Genome Mapping | [PlasMapper 3.0](https://plasmapper.wishartlab.com/) | Circular genome map |
| Genome Annotation | [Proksee](https://proksee.ca/) | Genome visualization and annotation |
| HPV Reference Database | [PaVE Database](https://pave.niaid.nih.gov/) | Papillomavirus reference sequences |
| Similarity Search | [NCBI BLASTn](https://blast.ncbi.nlm.nih.gov/Blast.cgi) | Genome comparison |
| Protein Similarity | [NCBI BLASTp](https://blast.ncbi.nlm.nih.gov/Blast.cgi) | Protein comparison |
| Sequence Alignment | [Clustal Omega](https://www.ebi.ac.uk/Tools/msa/clustalo/) | Conserved region analysis |
| Protein Properties | [ProtParam](https://web.expasy.org/protparam/) | Physicochemical characterization |
| Homology Modelling | [SWISS-MODEL](https://swissmodel.expasy.org/) | 3D protein modelling |
| Ligand Retrieval | [PubChem](https://pubchem.ncbi.nlm.nih.gov/) | Ligand structures |
| ADMET Prediction | [ADMET-AI](https://admet.ai.greenstonebio.com/) | Drug-likeness and toxicity |
| Binding Pocket Prediction | [CASTpFold 3.0](https://cfold.bme.uic.edu/castpfold/compute) | Active site identification |
| Protein Preparation | ChimeraX | Remove HETATM and water molecules |
| Molecular Docking | [SwissDock](https://www.swissdock.ch/) | Protein-ligand docking |
| Interaction Visualization | PyMOL / Discovery Studio | Binding interaction analysis |

# Genome Analysis

The complete HPV16 genome was retrieved and analysed to identify coding regions and gene organization.

The analysis included:
1. ORF prediction
2. Gene prediction
3. Genome annotation
4. Circular genome visualization
5. Sequence similarity analysis
6. Conserved region identification

These analyses confirmed the organization of the major HPV proteins:
1. E1
2. E2
3. E4
4. E5
5. E6
6. E7
7. L1
8. L2

# Comparative Sequence Analysis

Genome and protein similarity analyses were performed using BLAST followed by multiple sequence alignment.
The analyses showed:
1. High sequence similarity with HPV16 isolates
2. Conserved nucleotide regions
3. Conserved amino acid residues
4. Variable mutation regions
5. Strong protein homology

These findings indicate that most functional regions of HPV16 remain highly conserved.

# Protein Physicochemical Analysis

ProtParam was used to evaluate:

1. Molecular weight
2. Theoretical pI
3. Instability index
4. Aliphatic index
5. GRAVY score
6. Amino acid composition

This provided insight into protein stability and biochemical characteristics before structural modelling.

# Homology Modelling

Initially, homology modelling was performed for all eight HPV16 proteins. 
1. E1
2. E2
3. E4
4. E5
5. E6
6. E7
7. L1
8. L2

Model quality was evaluated using:

1. Template identity
2. Sequence coverage
3. GMQE
4. QSQE
5. Structural quality

Among all proteins, E2, E6, and L1 exhibited template identities and sequence coverage greater than 95%, indicating highly reliable structural models.

**Why E6 was selected**

Although E2, E6, and L1 all produced high-quality models:

1. L1 is primarily a vaccine target because it is the major capsid protein with important antigenic determinants.
2. E2 showed excellent structural quality; however, sufficient literature describing small-molecule inhibition was not available.
3. E6 is a well-established oncogenic protein with several reported inhibitory compounds, making it the most suitable target for docking studies.

Therefore, HPV16 E6 was selected for downstream molecular docking.

# Ligand Selection

Four compounds were selected through literature review.

| Category  | Compound                         | Reported Role                                    |
| --------- | -------------------------------- | ------------------------------------------------ |
| Synthetic | Sulindac                         | Growth inhibition and apoptosis induction        |
| Synthetic | Imiquimod                        | Immune modulation                                |
| Natural   | Indole-3-Carbinol (I3C)          | Induces apoptosis in cervical cancer cells       |
| Natural   | Nordihydroguaiaretic Acid (NDGA) | Suppresses E6 gene expression and stabilizes p53 |

# ADMET Analysis

ADMET prediction was performed before docking to evaluate pharmacokinetic and toxicity profiles.

**Why ADMET is important**

A compound with excellent docking affinity may still fail as a drug if it has poor absorption, unfavorable metabolism, or high toxicity. Therefore, ADMET screening helps prioritize compounds with a better balance between efficacy and safety.

**Toxicity ranking**

Sulindac > Imiquimod > NDGA > Indole-3-Carbinol

Toxicity ranking (Highest → Lowest)

# Binding Pocket Prediction

CASTpFold 3.0 was used to identify the binding pocket of the HPV16 E6 protein before docking.

**Why is binding pocket prediction important?**

Blind docking searches the entire protein surface, which can identify unrealistic binding locations. Predicting the active binding pocket first allows docking to focus on biologically relevant regions, improving the reliability of predicted interactions.

Conversely, even a highly effective ligand can produce a poor docking score if docking is performed in an incorrect grid or binding region instead of the true active pocket.

Pocket prediction therefore helps:
1. Identify active site residues
2. Estimate pocket area and volume
3. Guide docking towards functional regions
4. Improve interpretation of docking results

# Molecular Docking Results

| Compound          | Category  | Binding Affinity (kcal/mol) |
| ----------------- | --------- | --------------------------: |
| NDGA              | Natural   |                  **−8.318** |
| Sulindac          | Synthetic |                  **−8.082** |
| Imiquimod         | Synthetic |                  **−7.691** |
| Indole-3-Carbinol | Natural   |                  **−6.143** |

**Binding affinity ranking (Highest → Lowest)**

NDGA
    >
Sulindac
    >
Imiquimod
    >
Indole-3-Carbinol

# Key Findings

1. Homology modelling identified E2, E6, and L1 as the highest-quality structural models.
2. E6 was selected as the drug target based on both structural quality and available literature.
3. NDGA exhibited the strongest binding affinity.
4. Sulindac showed strong binding but the highest predicted toxicity.
5. Indole-3-Carbinol displayed the weakest docking score but the lowest predicted toxicity.
6. Drug selection should consider docking affinity together with toxicity and pharmacokinetic properties rather than binding energy alone.

# Discussion

This study demonstrates a complete computational workflow from viral genome analysis to structure-based drug discovery. Comparative genomics confirmed the conservation of major HPV16 proteins, while homology modelling identified E2, E6, and L1 as structurally reliable proteins for downstream applications.

Among these, E6 was selected because of its central role in HPV-associated carcinogenesis and the availability of reported inhibitory compounds. ADMET prediction complemented molecular docking by highlighting that binding affinity alone does not determine therapeutic potential. Although Sulindac showed strong binding, its higher predicted toxicity reduced its overall suitability. NDGA achieved the best balance between docking performance and predicted safety, whereas Indole-3-Carbinol demonstrated the most favorable toxicity profile despite lower binding affinity.

Overall, the integrated workflow suggests that NDGA represents the most promising computational lead against the HPV16 E6 protein and emphasizes the importance of combining structural modelling, binding pocket prediction, docking, and ADMET evaluation during early-stage drug discovery.

# Future Scope

1. Molecular dynamics simulation
2. MM-PBSA free energy calculation
3. Experimental validation
4. Structure optimization of lead compounds
5. Design of improved E6 inhibitors

# Acknowledgement

I sincerely express my heartfelt gratitude to **Dr. Diptendu Sarkar Sir**, Assistant Professor and Head, Department of Microbiology, Ramakrishna Mission Vidyamandira, Belur, and State President (West Bengal), Microbiology Society, India (MBSI), for his valuable guidance and mentorship throughout this internship.

Dr. Sarkar Sir demonstrated the complete bioinformatics workflow using relevant tools and web servers with an example viral dataset, providing a clear understanding of each analysis step. He then encouraged independent project-based learning by allowing us to choose a virus of our interest and perform the entire workflow ourselves. Based on this opportunity, I selected **Human Papillomavirus type 16 (HPV16)** and independently carried out the complete computational analysis, from genome characterization to molecular docking and result interpretation.

I am sincerely thankful to Dr. Sarkar Sir for his continuous support, encouragement, and for providing an excellent learning environment that strengthened my practical skills in bioinformatics and computational biology.

# References

1.	Jensen, J. E., Becker, G. L., Jackson, J. B., & Rysavy, M. B. (2024). Human Papillomavirus and Associated Cancers: A Review. Viruses, 16(5), 680. https://doi.org/10.3390/v16050680
2.	Han, F., Guo, X. Y., Jiang, M. X., Xia, N. S., Gu, Y., & Li, S. W. (2024). Structural biology of the human papillomavirus. Structure (London, England : 1993), 32(11), 1877–1892. https://doi.org/10.1016/j.str.2024.09.011
3.	Nelson, C. W., & Mirabello, L. (2023). Human papillomavirus genomics: Understanding carcinogenicity. Tumour virus research, 15, 200258. https://doi.org/10.1016/j.tvr.2023.200258
4.	Oyouni A. A. A. (2023). Human papillomavirus in cancer: Infection, disease transmission, and progress in vaccines. Journal of infection and public health, 16(4), 626–631. https://doi.org/10.1016/j.jiph.2023.02.014
5.	Khamjan, N. A., Beigh, S., Algaissi, A., Megha, K., Lohani, M., Darraj, M., Kamli, N., Madkhali, F., & Dar, S. A. (2023). Natural and synthetic drugs and formulations for intravaginal HPV clearance. Journal of infection and public health, 16(9), 1471–1480. https://doi.org/10.1016/j.jiph.2023.06.016

