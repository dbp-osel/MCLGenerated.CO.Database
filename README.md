# MCLGen.CO.Database
**Title:**

**Mock Circulatory Loop Generated Database for Dynamic Characterization of Pressure-based Cardiac Output Monitoring Systems**

*Masoud Farahmand; Gavin A. D’Souza; Luke H. Herbertson; and Christopher G. Scully*
 <hr style="border:2px solid black">
 
**Abstract** 

This database contains central (aortic) flow and central (aortic) and peripheral (radial) pressure waveforms recorded from a mock circulation loop (MCL) that is configured to simulate three different hemodynamic states representing a range of flow and pressure conditions. The MCL relationship between central pressure and peripheral pressure was validated against clinical data to ensure that realistic physiologic peripheral pressure waveforms correlated with the cardiac hemodynamics are generated {reference}. This non-clinical database is intended as a tool for assessing the dynamic attributes of pressure-based cardiac output (CO) monitoring systems, including the response time of a system to a change in CO (i.e., CO response time), and the smallest CO and stroke volume variation (SVV) change that a system can reliably detect (i.e., CO resolution, and SVV resolution). The database can be used to characterize the device algorithm or the entire system (i.e., software and hardware). We have provided a full technical description of the database and an example application in {reference}.

**Background**

Pulse contour cardiac output monitoring systems enable real-time and continuous measurement of CO and other hemodynamics in a minimally invasive manner through the analysis of arterial blood pressure waveforms [1]. Clinical use of these systems has involved tracking rapid changes in CO, stroke volume and/or SVV to monitor patient responses to treatment, distinguish between fluid responders and non-responders, and guide fluid therapy [2]. Currently, there are no consensus standards for assessment of pressure-based CO monitoring systems. Highly controlled experiments are needed to calculate these attributes for a system and to our knowledge, currently there’s no other method to reliably determine the abovementioned attributes of this type of system. 
We developed an MCL that can simulate rapid changes in different parameters, such as CO and SVV. The MCL was configured to simulate three different hemodynamic states representing a range of flow and pressure conditions. For each state, we simulated controlled stepwise changes in the MCL flow and collected a dataset for characterizing dynamic attributes of pressure-based CO systems. Nine datasets were generated in all, which contain several hours of central flow, central pressure, and peripheral pressure waveforms.

**Methods**

The MCL was used to simulate three hemodynamic states (i.e., hyperdynamic, normovolemic, and cardiogenic shock) based on average hemodynamic values and mimic central-to-peripheral pressure transfer functions reported in the literature. For each state, 

•	we simulated stepwise changes in the MCL flow and collected datasets for characterizing CO resolution and SVV resolution of pressure-based CO systems. 

•	we determined CO Response time of a system via simulating rapid changes in MCL flow rate in one step. 

Flow and pressure waveforms were simultaneously recorded with high fidelity flow and pressure sensors in each step. Detailed methods are described in [reference].

**Data Description**

Overall, nine mock flow loop-generated datasets were collected to quantify three dynamic attributes of pressure-based CO monitoring systems.

•	The database contains 9 datasets that correspond to 3 hemodynamic states (i.e., Normovolemic, Cardiogenic shock, and Hyperdynamic states) × 3 types of tests for each state as follows:

    - 	CO resolution dataset (COres): ~1 L/min mean central flow (i.e. CO) change in both directions from baseline in incremental steps (Data is recorded for 60 seconds in each step)

    - 	CO response time dataset (COrt): A rapid ~10% decrease in CO from baseline followed by an increase of ~10% back to baseline (Data is recorded for 360 seconds)

    - 	SVV resolution dataset (SVVres): SVV change in both directions in incremental steps at two different respiration rates (20 times/min and 12 times/min) (Data is recorded for 60 seconds in each step)

Accordingly: 

•	MCLGen.CO.Database.zip file contains folders for CO resolution, SVV resolution and CO response time datasets named as COres, SVVres, and COrt, respectively. 

•	Under each folder corresponding to each hemodynamic state there are three folders named ‘normovolemic’, ‘cardiogenic_shock, and ‘hyperdynamic’.

    - 	Also, for the SVV resolution test, there are two folders ‘RR20’ and ‘RR12’ corresponding to two different respiration rates (i.e., 20 times/min and 12 times/min) under each hemodynamic state folder.

•	Each of the folders contain CSV files corresponding to different steps and hemodynamic states. For example, ’NV_step1_COresolution.csv’ contains normovolemic flow and pressure data in step 1 for CO resolution test.

    - 	An info.txt file exist in each folder that provides information about the folder content. 

•	Each CSV file contains timestamps, and flow and pressure data that are arranged in four columns as follows: 

| Column1  | Column2 |Column3 |Column4 |
| ------------- | ------------- |------------- |------------- |
| **Time stamp in second** | **Central flow rate in mL/second**  | **Central pressure in mmHg**  | **Peripheral pressure in mmHg** |


•	Flow data were sampled at 1kHz with a low-pass filter at 10 Hz.

•	Central pressure, and peripheral pressure waveforms sampled at 1kHz with a low-pass filter applied with a 55 Hz cut-off frequency.

**Usage Notes**

The csv files can be downloaded and used directly to characterize pressure-based cardiac output monitoring systems or algorithms. The database has been used in a publication to determine dynamic attributes of an example benchtop pressure-based CO monitoring system [reference]. While this database enables testing of certain characteristics that are challenging and impractical to address in clinical studies, it is not a replacement for accuracy testing in clinically relevant patient populations with appropriate reference methods. 

**Contributors**

For more information about the dataset, please contact the authors at: masoud.farahmand@fda.hhs.gov, and christopher.scully@fda.hhs.gov .

**Files**
Total size: 207.7 MB (unzipped).

**References**

[1]	J. A. Alhashemi, M. Cecconi, and C. K. Hofer, "Cardiac output monitoring: an integrative perspective," (in eng), Crit Care, vol. 15, no. 2, p. 214, 2011, doi: 10.1186/cc9996.

[2]	C. Correa-Gallego et al., "Goal-directed fluid therapy using stroke volume variation for resuscitation after low central venous pressure-assisted liver resection: a randomized clinical trial," Journal of the American College of Surgeons, vol. 221, no. 2, pp. 591-601, 2015.

