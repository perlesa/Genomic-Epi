INTRODUCTION

The following is the workflow and documentation of a genomic epidemiology investigation I conducted in collaboration with the North Dakota Veterinary Diagnostics Lab and the North Dakota Department of Agriculture. In 2022, these departments were tasked with investigating a Salmonella outbreak among exotic cats in a North Dakota zoo— two snow leopards and a Pallas’ cat. They found that all three were carrying a multidrug-resistant strain of Salmonella serovar Newport, REPJJP01, that had also infected animals in two unrelated zoos. This strain is associated with imported beef products from Mexico, though no additional evidence has yet come forth about potential food-source contamination for these animals.

This event alerted the departments to the need for additional AMR surveillance among exotic and domestic animals as a potential risk factor of zoonotic spillover to humans. These kinds of animals receive considerably less attention than commercial food animals such as poultry, swine, and cattle, which are well-established reservoirs of antimicrobial-resistant bacteria and are subject to extensive antimicrobial use in agricultural settings.

The VDL asked me to analyze genomic data from a set of roughly 2600 Salmonella isolates from the FDA’s Veterinary Laboratory Investigation and Response Network (Vet-LIRN), a federal program that monitors animals for AMR pathogens. This dataset had previously been unanalyzed by the department due to constraints on time, staff, and bioinformatics capacity, and the department was interested in documenting unusual AMR genes found in animal reservoirs and in serovars besides Newport.

This analysis was conducted primarily on GalaxyTrakr, a graphical user interface dedicated to public health bioinformatics and pathogen genomics. Below, you'll find my Galaxy pipelines, results, and associated metadata.

1) EXPLORATORY ANALYSIS

I first filtered the Vet-LIRN dataset for isolates taken from exotic animals, domestic animals, and wildlife. After organizing these isolates by serovar, I discovered a population of serovar Typhimurium isolates spread among different bird and mammalian species (Table 1- Vet-LIRN, "Enterica serovars"). After  retrieving sample accession numbers profiling for AMR genes using metadata from NCBI Pathogen Detection, I discovered a cassette of multidrug-resistant genes (blaCMY-2, sul2, tet(A)) among two domestic cats and a wild turkey (Table 1- Vet-LIRN, "Typhimurium metadata"). 

The blaCMY-2 gene is an antibiotic resistance gene that encodes an AmpC-type beta-lactamase enzyme. It provides bacteria with resistance to penicillins, cephamycins, and third-generation cephalosporins such as ceftriaxone and ceftazidime (Call et al., 2009). It has been associated in the literature with Salmonella Typhimurium and E. coli in commerical poultry farming operations, typically carried by an IncI plasmid designated in MOB as plasmid cluster AA474 (Robertson et al., 2023; Sanderson et al., 2023; Habib et al., 2025). Indeed, IncI and IncX plasmid backbones were detected in the Vet-LIRN isolates, suggesting that a mobile genetic element may have been carrying this gene and others.

