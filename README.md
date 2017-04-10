## massmappy - a code to generate mass maps from galaxy shear measurements

###### Code Authors: 
Main Author: Christopher G R Wallis (christophergrwallis@gmail.com)

###### Useful and necessary contributions:
* Jason McEwen (jason.mcewen@ucl.ac.uk)
* Thomas Kitching (t.kitching@ucl.ac.uk)
* Boris Leistedt (boris.leistedt@gmail.com)
* Antoine Plouviez (antoine.plouviez@ens-cachan.fr)

###### Code used for the papers:  

* "Mapping dark matter on the celestial sphere with weak gravitational lensing", Christopher G. R. Wallis, Jason D. McEwen, Thomas D. Kitching, Boris Leistedt and Antoine Plouviez arXiv:1703.09233 https://arxiv.org/abs/1703.09233

###### Installation:

From the command line, move into the directory and execute: `python setup.py build_ext --inplace`

###### Dependances:
* numpy
* matplotlib
* libc
* pyssht www.spinsht.org
* healpy (only needed for certain functions)


###### Directories:

* src/ 	  	: Contains all the code
* python/ 	: Contains all the python code
	* DES_mass_map.py 	: Analyses the DES data and generates plots in Figures 5-7 and B3
	* cy_mass_mapping.pyx	: General code base for sherical mass mapping using ssht and planar mass mapping
	* low_res_examples.py 	: Code to generate Figures 2 and 3 and Table 1
	* mass_mapping.py 	: Example code that is fast to run showing mass mapping on the sphere
	* cy_DES_utils.pyx 	: Code to generate shear maps from the measured galaxy shapes
	* cy_healpy_mass_mapping.pyx : Code for making spherical mass maps using healpix
	* cy_mass_mapping.pxd	: Supporting functions
	* high_res_error.py 	: Code to generate Figure 4
	* plot_high_res.py 	: Code to generate Figure 4
* mask_plots/	: Contains plots of the servey areas of some past present and future weak lensing experiments
* fig/ 		: Contains figures generated by the code
* data/ 	: Contains data used/made by the code
	* DES.mat          					All the necessary parts of the DES SV public cataloge used in the code           
	* cell_icosmo.txt             		An example cosmic sheer power spectrum generated by cosmosis
	* cls_ap.txt                  		Interpelated power spectrum used by the code
	* high_res_results/            		Example results from high_res_error.py
	* reduced_shear_iteration.txt			Reduced shear results from low_res_examples.py
