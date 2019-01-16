Project thermochron

May 26, 2011
"Boris Avdeev, borisaqua@gmail.com"
"Mike Turzewski, mturzewski@gmail.com"
http://code.google.com/p/thermochron/source/

This python package contains thermochron-ralated codes. 

Installation instructions are in INSTALL.txt

thermochron.detrital_ui is a module for estimation erosion models from detrital and bedrock thermochronometric data (Avdeev et al., 2011)

To use the thermochron.detrital_ui module, copy the provided model_summary.py settings file into a folder in which model output will be stored. Open this file in a text editor, and modify following instructions found in the model_summary.py file.

From within the model folder run thermochron/detrital_ui/run.py. This will read the model_summary.py and all the data, and run the MCMC sampler to estimate the parameters. Every additional call to run.py will produce additional Markov chains.

The output of the MCMC sampler is stored in subfolder XXX, as plain text files.

The program will also generate several output figures based on the number of detrital/bedrock samples that are provided in 'model_setup.py'. These include:
	
	'Summary' -- A figure that provides empirical CDF's for each detrital sample as well as a visual plot of the traces for the parameters.
	'Chains' -- A figure containing plots and histograms of the thinned chains for each parameter in the model.
	'Statistics' -- A file which provides the mean, standard deviation, and confidence intervals for each parameter estimate. 
	'KS_test' -- A Kolmogorov-Smirnov goodness of fit plot for each detrital sample that plots KS statistics for the model and a p-value describing the model fit.
	'Discrepancy_Plot' -- A plot for each sample displaying the discrepancy statistics for the model and a p-value. 
		(Learn more about the discrepancy statistic in PyMC User Guide: http://code.google.com/p/pymc/downloads/list)
	Histograms -- Histograms for both ages and elevations for all detrital samples. 
	

