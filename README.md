# PDB_domain_extractor

Author: Murat Buyukyoruk

Associated lab: Wiedenheft lab

        PDB_domain_extractor help:

This script is developed to fetch domain from PDB files. 

IMPORTANT! The input PDB file should be located in the same directory as the workdir directory (type "pwd" to terminal first to get the current workdir.)  

UCSF-Chimera and Pychimera packages are required to fetch domains. Additionally, tqdm is required to provide a progress bar since some multifasta files can contain long and many sequences.

Syntax:

        pychimera PDB_domain_extractor.py -i demo_list.txt

Example Dataframe (tab separated file is required with .txt extension):

        PDB         Domain      Start       Stop
        4ncb.pdb    PIWI        461         685    
        
flank_grabber dependencies:
    
	UCSF-Chimera                                            refer to https://www.cgl.ucsf.edu/chimera/data/downloads/1.17.1/linux_x86_64.html
	Pychimera                                               refer to https://pypi.org/project/pychimera/0.1.1/
	tqdm                                                    refer to https://pypi.org/project/tqdm/

Input Paramaters (REQUIRED):
----------------------------
	-i/--input		FASTA			Specify a list of positions of domain of interest from pdbs.

Basic Options:
--------------
	-h/--help		HELP			Shows this help text and exits the run.

Output header will contain protein accession/array no, original accession number, positions and fullname (if included in original fasta), observed stand and the information about flank in terms of which side of the gene is fetched.

