# Molecular networking applied to toxicology

## Overview

This project consists of 5 modules to facilitate the analysis of mass spectrometry data by molecular networking :
- **Metabolites**: annotation of molecules in a .clustersummary file from the GNPS site from a reference file.
- **Biotransformation**: annotates the links in a .selfloop file from the GNPS site with the biotransformations corresponding to the mass difference between the molecules.
- ***InSilico***: *in silico* prediction of a list of molecules whose SMILES code is provided by 3 software packages (BioTransformer3, SyGMa, MetaTrans).
- **MetGem**: allows export to Cytoscape of molecular network link information generated by the MetGem software.
- **ProteoWizard**: converts mass spectrometry data from proprietary to open formats. Uses the docker version to run on a Linux system.

Linux and Windows (WSL) compatible. Not tested on Mac

## Quick start

### Required packages:
- **Zenity** `sudo apt install zenity` (As this project was designed for non-bioinformaticians, a graphical interface via zenity was included. However, modules can be used separately)
- **bc command** `sudo apt install bc`
- **gawk** `sudo apt install gawk`
- **Java** `sudo apt install default-jre`
- **Docker** (https://docs.docker.com/desktop/install/linux-install/)
- **Conda** (https://github.com/conda/conda).
- Necessary for metatrans conda environment installation : `conda config --set channel_priority flexible`

### Download: 
- `git clone https://github.com/alexisbourdais/MolecularNetworking`
- `cd Tools/`
- `git clone https://bitbucket.org/wishartlab/biotransformer3.0jar.git` **Biotranformer3.0** 
- `git clone https://github.com/KavrakiLab/MetaTrans` **MetaTrans**
- download the models in https://rice.app.box.com/s/5jeb5pp0a3jjr3jvkakfmck4gi71opo0 and place them in **MetaTrans/models/**

### Run
- `cd ..`
- `chmod +x Main.sh`
- `./Main.sh`

To use the ***in silico*** mode, create a text file with each line = namemolecule,smilecode

## Sources & Documentations

GNPS : https://gnps.ucsd.edu/ProteoSAFe/static/gnps-splash.jsp

BioTransformer3 : https://bitbucket.org/wishartlab/biotransformer3.0jar/src/master/

SyGMa : https://github.com/3D-e-Chem/sygma

MetaTrans : https://github.com/KavrakiLab/MetaTrans

ProteoWizard : https://proteowizard.sourceforge.io/

Cytoscape : https://cytoscape.org/

MetGem : https://github.com/metgem/metgem

SdftoSmi & SmitoStr scripts : https://github.com/MunibaFaiza/cheminformatics/tree/main

## References

Wang, M. et al. Sharing and community curation of mass spectrometry data with Global Natural Products Social Molecular Networking. Nat Biotechnol 34, 828–837 (2016).

Djoumbou-Feunang, Y. et al. BioTransformer: a comprehensive computational tool for small molecule metabolism prediction and metabolite identification. J Cheminform 11, 2 (2019)

Ridder, L. & Wagener, M. SyGMa: Combining Expert Knowledge and Empirical Scoring in the Prediction of Metabolites. ChemMedChem 3, 821–832 (2008).

Litsa, E. E., Das, P. & Kavraki, L. E. Prediction of drug metabolites using neural machine translation. Chem. Sci. 11, 12777–12788 (2020).

Chambers, M. C. et al. A cross-platform toolkit for mass spectrometry and proteomics. Nat Biotechnol 30, 918–920 (2012).

Shannon, P. et al. Cytoscape: A Software Environment for Integrated Models of Biomolecular Interaction Networks. Genome Res. 13, 2498–2504 (2003).

Olivon, F. et al. MetGem Software for the Generation of Molecular Networks Based on the t-SNE Algorithm. Anal. Chem. 90, 13900–13908 (2018).
