# IPD-uncertainty
Uncertainty calculation for the matrix inversion of the isotope pattern deconvolution technique, using a Monte Carlo approach. Questions can be directed to alkuin.koenig@gmx.de

Important notes:
- For convenience, data input and output is managed through excel files (.xlsx).
  - Input files should be deposited in the folder ./data_input
  - Output files will be deposited in the folder ./data_output by the main program
- The main program/script/notebook is called "IPD_uncertainty_Monte_Carlo.rmd", found in ./scripts

For computation of uncertainties, follow these steps: 
1) duplicate the file "isotope_keys_testfile.xlsx" in ./data_input (copy the duplicate into the same folder), and adapt it to your setup (i.e. populate it with the values corresponding to your setup. This file should contain information about the definition of your isotopes, their molar mass, their relative abundancies, and related uncertainties. It is needed for the matrix deconvolution.). **More info is given in the README that is given for each sheet of the testfile!**
2) duplicate the file "sample_data_testfile.xlsx" in ./data_input (copy the duplicate into the same folder), and adapt it to your data (i.e. fill in your data values, such as the peak area and it's uncertainty for each sample, as well as information about sample volume, etc.). More info is given in the individual README that is given for each sheet of the testfile! **For both input files, do NOT change the general structure of the file, do NOT erase the README cells, and do NOT rename the sheets!**
3) modify the fist cell of the R notebook "IPD_uncertainty_Monte_Carlo.rmd" in ./scripts to take the correct input files! (should be self-explanatory)
4) Define the desired output by modifying the first cell of "IPD_uncertainty_Monte_Carlo.rmd" (check out the comments in the notebook for more information)
5) Run "IPD_uncertainty_Monte_Carlo.rmd". Once through, make sure that a new output was created in ./data_output. Note that in the name of each output file a timestamp is included corresponding to the time of computation (new output will not overwrite old output). It's your job to keep track of the output files! (you can rename them afterwards with more fitting names. Note that each output file contains a sheet named "Metadata" with more information about how the file was created)
