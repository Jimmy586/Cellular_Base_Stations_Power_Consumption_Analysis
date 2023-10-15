# Cellular_Base_Stations_Power_Consumption_Analysis and ENERGY SAVING
* This repo contains the code and documentation/report of my internship at IMT Atlantique Rennes, France during the summer 2023, I was supervied by Prof NUAYMI Loutfi and MERLHE Christopher.
* The main topic of my research was to find key indicators and approaches to tackle power greediness of BS and apply the result to the BS stations here in France.
  To do this we were equiped with the open-source from ANFR to estimate the power consumed by BS in France and then analyse the key factor influencing these consumptions, and then design approaches to save energy in a seamless way without too much affecting the QOS.

## PART 1 :  POWER USAGE ESTIMATION
This part is about Power usage estimation and analysis on cellular base stations in France, the dataset was taken from ANFR website for the 4giant  Telecom companies based in france (ORANGE, SFR, BOUYGUES, FREE)
Before running the source code, the following steps are to be completed:

* Firstly, three new folders should be created within the code directory. The first should be named as "ANFR Dataset", the second should be "Pre-processed data" and the last one should be "Graphs".
* Within the 'ANFR Dataset' folder, the entire ANFR dataset is to be placed. The dataset including the data and the reference files can be downloaded from the dataset website. The downloading process is tedious as the files for each month needs to be downloaded one by one.
* There are a few mistakes in the downloaded files from the ANFR website. here are some examples of them
    * **April 2022**: In the folder name, 2023 should be changed to 2022.
    * **May 2018**: The date format should be changed from 31052018 to 20180531 in the folder names.
    * **March 2018**: The data and reference folders are within the same folder so they should be separated.
    * **January 2018**: The date should be moved in the front of the folder name. Also it should be formatted similar to what is mentioned for May 2018.
    * **January 2017**: There is no reference folder, so the reference folder for February 2017 should be utilized. A new folder should be created with the correct naming.
    * **May 2016**: The date in the folder name should be changed from 20160402 to 20160430.
    * **April and May 2015**: The dates are missing so they should be added in the correct format with the folder names.
* The 'ANFR_Dataset_Processing_Codes.ipynb' file should be executed first before running the other files.
* Model used to estimate BS Power consumption : EARTH 2011 which was designed specifically for 4G
* Frew improvements were implemented to have more accurate estimation :
     * **5G NR 3500 Specific Model** : this solve the fact that there is no 3500MHz frequency band in 4G so the estimation can't be applied, so here we adapted the EARTH formula to better fit the 5G BS specifications in terms of Bandwidth usage, the Massive MIMO 64 X 64 RXTX, and the other hardware components of the BS.
     * **Performance Improvements** : the old EARTH Model doesn't take into account the technilogical improvement and time constraints, so here we implemented in the Model a mecanism which takes into account the Moore's Law (every 2 years, a reduction of 2% per year was observed in the power lost inside a Power Amplificator of a BS [B. Dabaillie, C. Dasset, and F. Louagie]), this resulted in increased BS power efficiencies.

## PART 2 AND 3 : KEY INDICATORS INFLUENCING THE ENERGY CONSUMPTION AND APPROACHES TO IMPLEMENT ENERGY SAVING ON BS INSTALLED IN FRANCE
This part is contained mainly in the APPROACHES-ENERGY-SAVING folder, with its application using the traffic load of a BS station here in Rennes (Antenne SFR Atalante Beaulieu, Rennes) and were able to save up to 20% of a normal energy usage at Low load and ~15% of gain on high Load.
       
