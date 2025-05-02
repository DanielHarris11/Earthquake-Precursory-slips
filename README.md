# Earthquake-Precursory-slips
# This process removes Common mode Error via an ICA or a PCA for a single earthquake using GTS_CME.
# All data files from Bletery and Nocquet's paper "The precursory phase of large earthquakes" must be downloaded as well as the GTS_CME software 
# Use TransferTo_GTS_CME to get all .dat files in the correct data format for use in GTS_CME. Directorys need to be edited so it works om your computer.
# Apply an ICA/PCA in GTS_CME and place output files in a suitable location. These remove lines of data which needs to be accounted for. I used two methods to solve this problem. 
# 1) Set all NaN values to zero in the GTS_CME source code writefile_hector.m, then use GTStoStack to format these files back into the format for Bletery and Nocquets code.
# 2) Use Fill_Outliers to interpolate for the missing NaN values and then use the second code in GTStoStack to place this data into the file format for Bletery and Nocquets code. 
# Replace the original .dat files with the new .dat files in the stack and run the original code from the dot product.
# Unfortunately this has to be done individually for earthquakes and cannot be applied to the entire stack at once. 

