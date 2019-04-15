# REMI 

Relative Expression and Metabolite Integration
Paper :

    Pandey, Vikash, Noushin Hadadi, and Vassily Hatzimanikatis. "Enhanced flux prediction by integrating relative expression and relative metabolite abundance into thermodynamically consistent metabolic models." bioRxiv (2018): 481499.

URL : https://www.biorxiv.org/content/10.1101/481499

## Folder organisation

REMI folder contains folders:  core, data, models, scripts, and simData.

1. core : The folder contains the functions which are required for generating models, computing alternatives solutions etc.
2. data: The folder contains data which are required to execute REMI walkthrough script. It comprises some random transciptomics(RelExpData.mat) and metabolomics(relMetdata.mat) as well as gene expression (test\_expr.mat)and metabolomics(fmodel.mat, fmodel.Ishii) data from Ishii et al 2007. The Expression data data was also used in the Eflux2 and SPOT method.
3. models: For a quick analysis and run we put the ecoli core model. Additionally, for reproducing results from the paper we also put the GEM with and without thermodynamic constraints.
4. scripts: We provide two walkthrough files for 1) ecoli model and 2) for a GEM.  With the ecoli walkthrough script one can build model from scratch and then perform alternative enumeration of maximum consistency score (MCS ; for detail see in Paper). Scripts folder contains three subfolders.

	- ModelGenRun:  We provides scripts which one we used to generate models, compute alternative solutions, and compute flux variability analysis.  We saved all results in simData. If one want use and execute these codes they need to set appropriate path for models and and path for saving the results. We already saved all results in simData.
	- Result\_script: This folder contains scripts which can be used generate figures and tables which are in the manuscript.  This script uses simData which we generated during the study using REMI method.
	- runGXFBA: This folder contains scripts for GX-FBA method (which is already published Navid et al 2012) and the scripts which one we used to generate results using data sets.

5. simData: This folder contains all simulation data which can be used to generate results of the paper.

	- Expression\_data: This folder contains Transcriptomics data form both studies: Ishii et al (see test\_expr.mat) and holm et al.
	- Fluxdata: Fluxomics data can be found form the studies Ishii et al and holm et al.
	- Metabolomics: This contains metabolomics data of aforementioned both studies.
	- ModelsSolutions: We generated different models using with thermodynamics (TGex, TGexM, TM) and without thermodynamics models (Gex, GexM, M). Gex indicates integration with only gene expression, GexM indicates gene expression and metabolite, and M indicates only metabolites. &#39;T&#39; is used for thermodynamic models.  Models for different mutants and conditions (e.g. pgm, pgi) can be found in the corresponding folders (TGex, TGexM, TM, Gex, GexM, and M).  Variables with the &#39;store&#39; tag comprises flux solutions, correlation values and percentage error between simulation and experiment fluxes.
	- AlternativeMCS: We generated alternative states for MCS and saved results.
	- FVAMM: This is the result flux variability analysis can be found in this folder.
	- Scatter\_plot: Scatter plots indicates correlation between measured and model predicted fluxes.


