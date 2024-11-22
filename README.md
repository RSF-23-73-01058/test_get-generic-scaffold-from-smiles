# test_get-generic-scaffold-from-smiles
This is a test of basic implementation of generic Bemis-Murcko scaffolds’ calculation (Bemis GW, Murcko MA. The properties of known drugs. 1. Molecular frameworks. J Med Chem. 1996 Jul 19;39(15):2887-93. doi: 10.1021/jm9602928. PMID: 8709122).
-	Input is the valid SMILES. Validity is ensured by the RDKit.js library (RDKit.js - JavaScript Example).
-	SMILES is pre-processed as string to make it ‘generic’.
-	Generic string is annotated to highlight the important positions.
-	For each important position links to the other important positions are listed.
-	Important positions having only one link are being deleted iteratively (except for rings).
-	Some post-processing takes place.
-	Here is the SMILES string of the generic Bemis-Murcko scaffold, which is visualized using RDKit.js, - an Output.
The code was tested using generic scaffolds of the 1155 drugs obtained using RDKit from Python (Malakhov G, Pogodin P. Dataset of drugs, their molecular scaffolds and medical indications with interactive visualization. Data Brief. 2024 Apr 14;54:110417. doi: 10.1016/j.dib.2024.110417. PMID: 38698799; PMCID: PMC11063979). The results of the test are good, ~98% SMILES strings of the generic scaffolds obtained using this tool and RDKit are literally the same strings. The remaining 2% probably describe the same structures.
However, more extensive validation and overall testing is needed before the practical usage.
