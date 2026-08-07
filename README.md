INTRODUCTION

The following is the workflow and documentation of a genomic epidemiology investigation I conducted in collaboration with the North Dakota Veterinary Diagnostics Lab and the North Dakota Department of Agriculture. In 2022, these departments were tasked with investigating a Salmonella outbreak among exotic cats in a North Dakota zoo— two snow leopards and a Pallas’ cat. They found that all three were carrying a multidrug-resistant strain of Salmonella serovar Newport, REPJJP01, that had also infected animals in two unrelated zoos. This strain is associated with imported beef products from Mexico, though no additional evidence has yet come forth about potential food-source contamination for these animals.

This event alerted the departments to the need for additional AMR surveillance among exotic and domestic animals as a potential risk factor of zoonotic spillover to humans. These kinds of animals receive considerably less attention than commercial food animals such as poultry, swine, and cattle, which are well-established reservoirs of antimicrobial-resistant bacteria and are subject to extensive antimicrobial use in agricultural settings.

The VDL asked me to analyze genomic data from a set of roughly 2600 Salmonella isolates from the FDA’s Veterinary Laboratory Investigation and Response Network (Vet-LIRN), a federal program that monitors animals for AMR pathogens. This dataset had previously been unanalyzed by the department due to constraints on time, staff, and bioinformatics capacity, and the department was interested in documenting unusual AMR genes found in animal reservoirs and in serovars besides Newport.

This analysis was conducted primarily on GalaxyTrakr, a graphical user interface dedicated to public health bioinformatics and pathogen genomics. Below, you'll find my Galaxy pipelines, results, and associated metadata.

1) EXPLORATORY ANALYSIS

I first filtered the Vet-LIRN dataset for isolates taken from exotic animals, domestic animals, and wildlife. After organizing these isolates by serovar, I discovered a population of serovar Typhimurium isolates spread among different bird and mammalian species (Table 1- "Vet-LIRN"). 
