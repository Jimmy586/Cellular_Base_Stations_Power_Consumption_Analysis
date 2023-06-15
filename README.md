# Cellular_Base_Stations_Power_Consumption_Analysis
This project is about Power consumption estimation and analysis on cellular base stations in France, the dataset was taken from ANFR website for the 4big Telecom companies based in france
Before running the source code, the following steps are to be completed:

* Firstly, three new folders should be created within the code directory. The first should be named as "ANFR Dataset", the second should be "Pre-processed data" and the last one should be "Graphs".
* Within the 'ANFR Dataset' folder, the entire ANFR dataset is to be placed. The dataset including the data and the reference files can be downloaded from the dataset website. The downloading process is tedious as the files for each month needs to be downloaded one by one.
* There are a few mistakes in the downloaded files from the ANFR website. Hence, for specific month's files, the following should be done manually:
    * **April 2022**: In the folder name, 2023 should be changed to 2022.
    * **May 2018**: The date format should be changed from 31052018 to 20180531 in the folder names.
    * **March 2018**: The data and reference folders are within the same folder so they should be separated.
    * **January 2018**: The date should be moved in the front of the folder name. Also it should be formatted similar to what is mentioned for May 2018.
    * **January 2017**: There is no reference folder, so the reference folder for February 2017 should be utilized. A new folder should be created with the correct naming.
    * **May 2016**: The date in the folder name should be changed from 20160402 to 20160430.
    * **April and May 2015**: The dates are missing so they should be added in the correct format with the folder names.
* The 'ANFR_Dataset_Processing_Codes.ipynb' file should be executed first before running the other files.
