# **HPV16: From Viral Genomics to Proteomics and Drug Discovery**

## **An Integrated In Silico Analysis of Human Papillomavirus Type 16**

# Project Overview

This project presents a complete bioinformatics workflow for the computational analysis of the Human Papillomavirus type 16 (HPV16) genome and the identification of potential inhibitors targeting the HPV16 E6 oncoprotein.

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

| Step                | Tool / Server            | Purpose                          |
| ------------------- | ------------------------ | -------------------------------- |
| Genome Retrieval    | NCBI                     | HPV16 genome                     |
| ORF Prediction      | ORF Finder               | Detect coding regions            |
| Gene Prediction     | GeneMark                 | Predict viral genes              |
| Genome Mapping      | PlasMapper               | Circular genome map              |
| Genome Annotation   | Proksee                  | Genome visualization             |
| Similarity Search   | BLASTn                   | Genome comparison                |
| Protein Similarity  | BLASTp                   | Protein comparison               |
| Sequence Alignment  | Clustal Omega            | Conserved region analysis        |
| Protein Properties  | ProtParam                | Physicochemical characterization |
| Homology Modelling  | SWISS-MODEL              | 3D protein modelling             |
| Ligand Retrieval    | PubChem                  | Ligand structures                |
| ADMET Prediction    | ADMET-AI                 | Drug-likeness and toxicity       |
| Pocket Prediction   | CASTpFold 3.0            | Active site identification       |
| Protein Preparation | ChimeraX                 | Remove HETATM and water          |
| Docking             | SwissDock                | Protein-ligand docking           |
| Visualization       | PyMOL / Discovery Studio | Interaction analysis             |

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
a. E1
b. E2
c. E4
d. E5
e. E6
f. E7
g. L1
h. L2

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
i.   Molecular weight
ii.  Theoretical pI
iii. Instability index
iv.  Aliphatic index
v.   GRAVY score
vi.  Amino acid composition

This provided insight into protein stability and biochemical characteristics before structural modelling.

# Homology Modelling

Initially, homology modelling was performed for all eight HPV16 proteins. E1
E2
E4
E5
E6
E7
L1
L2

Model quality was evaluated using:
1. Template identity
2. Sequence coverage
3. GMQE
4. QSQE
5. Structural quality

Among all proteins, E2, E6, and L1 exhibited template identities and sequence coverage greater than 95%, indicating highly reliable structural models.

**Why E6 was selected**

Although E2, E6, and L1 all produced high-quality models:
A. L1 is primarily a vaccine target because it is the major capsid protein with important antigenic determinants.
B. E2 showed excellent structural quality; however, sufficient literature describing small-molecule inhibition was not available.
C. E6 is a well-established oncogenic protein with several reported inhibitory compounds, making it the most suitable target for docking studies.

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

Sulindac
       <
Imiquimod
        <
NDGA
        <
Indole-3-Carbinol

Highest toxicity → Lowest toxicity
