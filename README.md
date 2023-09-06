# AutomatedSiteOptimisation

This is a current working script for running an automated workflow for identifying site and sample combinations which capture over 90% allele proportion, followed by site optimisation.

1). Run alleleproportion using 1000 iterations to find the number of sites and samples per site which capture over 90% of common alleles for your specific 'analysis' dataset (i.e. previously genetic neighbourhood)

2). Run OgmSFS analysis (a modified OptGenMix analysis using the site frequency spectrum to optimise site combination given site and individual parameters identified by the alleleproportion script)


Things you can customise using the RRSpeciesParameters.csv spreadsheet (example attached)

A). Do you want to optimise the site combination which gives you the minimum  number of sites required to capture over 90% alleles? - add "yes" to the "Run_OptSiteMix_minimum_Sites" column
B). Do you want to optimise the site combination which gives you the minimum  number of total individuals required to capture over 90% alleles? - add "yes" to the "Run_OptSiteMix_minimum_samples" column
C). Do you want to just run the alleleproportion analysis and not optimise any site combination? - add "no" to the "Run_OptSiteMix_minimum_samples" and "Run_OptSiteMix_minimum_Sites" columns
D). Do you want to force any sites into the optimisation analyses? add "yes" to the "Run_forced_OptSiteMix" column and list the exact name of the sites under the "List_of_ForcedSites" column (if you have multiple forced site, separate with "," and no spaces!
E). Do you want to change the allele proportion threshold to identify all site combinations which capture over X% of common alleles? - change the value of the "threshold_allele_prop" column to the desired proportion (default is 0.9)
