# __Fungal-Genome-Annotation__
This workflow provides a structured, user‑friendly approach to annotating fungal genomes using several established bioinformatic tools on the University of Brimingham's BlueBEAR HPC. Once a genome assembly is complete, you can use the pipeline to generate several kinds of informative annotations.

○ Gene structure and function annotations

○ Transposable element (TE) annotations

○ Translation of CDS predictions to Protein sequences

○ Signal peptide predictions

○ Starship mobile element detection

The final outputs include GFF files and summary tables that when put together offer greater insight into the fungal genome's content. 

The tools described within this workflow are all installed within BlueBEAR modules and can be loaded as described. In some cases, databases may be required which have been pre-downloaded onto the BlueBEAR project, but may need to moved elsewhere depending on project access. 

The script is split-up utilising BlueBEAR's slurm job system, with each tool and section within these suited for individual usage or as part of a larger step-by-step process. 

# __File Structure & Key Variables__
Before starting it is important to establish a structured file storage and naming system. This workflow was designed with this key structure in mind. Adapting a similar structure yourself will make adapting the script below easier, and make it less confusing when dealing with lots of different tools and output files.

Additionally, each job is given a specific name which represents the species sample used, eg. the specific isolate used or species grouping for the analysis. Examples such as 'Bsoro_Isolates' for analysis of several Bipolaris sorokinana isolates, or 'Bvictor_FI3' for analysis of the B. victoriae FI3 isolate. By creating a variable with this name, it can be easily attatched to output files while not needing to be manually re-named for each analysis. 
