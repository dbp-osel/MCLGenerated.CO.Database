# MCLGen.CO.Database
**Title:**

**Mock Circulatory Loop Generated Database for Dynamic Characterization of Pressure-based Cardiac Output Monitoring Systems**

*Masoud Farahmand; Gavin A. D’Souza; Luke H. Herbertson; and Christopher G. Scully*
 <hr style="border:2px solid black">
 
**Abstract** 

This database contains central (aortic) flow and central (aortic) and peripheral (radial) pressure waveforms recorded from a mock circulation loop (MCL) that is configured to simulate three different hemodynamic states representing a range of flow and pressure conditions. The MCL relationship between central pressure and peripheral pressure was validated against clinical data to ensure that realistic physiologic peripheral pressure waveforms correlated with the cardiac hemodynamics are generated {reference}. This non-clinical database is intended as a tool for assessing the dynamic attributes of pressure-based cardiac output (CO) monitoring systems, including the response time of a system to a change in CO (i.e., CO response time), and the smallest CO and stroke volume variation (SVV) change that a system can reliably detect (i.e., CO resolution, and SVV resolution). The database can be used to characterize the device algorithm or the entire system (i.e., software and hardware). We have provided a full technical description of the database and an example application in [1].

**Background**

Pulse contour cardiac output monitoring systems enable real-time and continuous measurement of CO and other hemodynamics in a minimally invasive manner through the analysis of arterial blood pressure waveforms [2]. Clinical use of these systems has involved tracking rapid changes in CO, stroke volume and/or SVV to monitor patient responses to treatment, distinguish between fluid responders and non-responders, and guide fluid therapy [3]. Currently, there are no consensus standards for assessment of pressure-based CO monitoring systems. Highly controlled experiments are needed to calculate these attributes for a system and to our knowledge, currently there’s no other method to reliably determine the abovementioned attributes of this type of system. 
We developed an MCL that can simulate rapid changes in different parameters, such as CO and SVV. The MCL was configured to simulate three different hemodynamic states representing a range of flow and pressure conditions. For each state, we simulated controlled stepwise changes in the MCL flow and collected a dataset for characterizing dynamic attributes of pressure-based CO systems. Nine datasets were generated in all, which contain several hours of central flow, central pressure, and peripheral pressure waveforms.

**Methods**

The MCL was used to simulate three hemodynamic states (i.e., hyperdynamic [HD], normovolemic [NV], and cardiogenic shock [CS]) based on average hemodynamic values and mimic central-to-peripheral pressure transfer functions reported in the literature. For each state, 

•	we simulated stepwise changes in the MCL flow and collected datasets for characterizing CO resolution and SVV resolution of pressure-based CO systems. 

•	we determined CO Response time of a system via simulating rapid changes in MCL flow rate in one step. 

Flow and pressure waveforms were simultaneously recorded with high fidelity flow and pressure sensors in each step. Detailed methods are described in [1].

**Data Description**



Overall, nine mock flow loop-generated datasets were collected to quantify three dynamic attributes of pressure-based CO monitoring systems.

•	The database contains 9 datasets that correspond to 3 hemodynamic states (i.e., Normovolemic, Cardiogenic shock, and Hyperdynamic states) × 3 types of tests for each state as follows:

    - 	CO resolution dataset (COres): ~1 L/min mean central flow (i.e. CO) change in both directions from baseline in incremental steps (Data is recorded for 60 seconds in each step)

    - 	CO response time dataset (COrt): A rapid ~10% decrease in CO from baseline followed by an increase of ~10% back to baseline (Data is recorded for 360 seconds)

    - 	SVV resolution dataset (SVVres): SVV change in both directions in incremental steps at two different respiration rates (20 times/min and 12 times/min) (Data is recorded for 60 seconds in each step)

Accordingly: 

•	MCLGen.CO.Database.zip file contains folders for CO resolution, SVV resolution and CO response time datasets named as COres, SVVres, and COrt, respectively. Please see the following figure:

![image](https://github.com/dbp-osel/MCLGenerated.CO.Database/assets/128830050/b7728aec-631a-4039-a675-f349aa5a57e5)

•	Under each folder corresponding to each hemodynamic state there are three folders named ‘normovolemic [NV]’, ‘cardiogenic_shock [CS], and ‘hyperdynamic [HD]’.

    - 	Also, for the SVV resolution test, there are two folders ‘RR20’ and ‘RR12’ corresponding to two different respiration rates (i.e., 20 times/min and 12 times/min) under each hemodynamic state folder.

•	Each of the folders contain CSV files corresponding to different steps and hemodynamic states. For example, ’NV_step1_COresolution.csv’ contains normovolemic flow and pressure data in step 1 for CO resolution test.

•	Each CSV file contains timestamps, and flow and pressure data that are arranged in four columns as follows: 

| Column1  | Column2 |Column3 |Column4 |
| ------------- | ------------- |------------- |------------- |
| **Time stamp in second** | **Central flow rate in mL/second**  | **Central pressure in mmHg**  | **Peripheral pressure in mmHg** |


•	Flow data were sampled at 1kHz with a low-pass filter at 10 Hz.

•	Central pressure, and peripheral pressure waveforms sampled at 1kHz with a low-pass filter applied with a 55 Hz cut-off frequency.

🔴 **An "info.txt" file exist in each folder that provides information about the folder content.**

# Regulatory Science Tool (RST) Reference
•	RST Reference Number: RST24CV01.01  
•	Date of Publication: 02/07/2024  
•	Recommended Citation: U.S. Food and Drug Administration. (2024). Mock Circulatory Loop Generated Database for Dynamic Characterization of Pressure-based Cardiac Output Monitoring Systems (RST24CV01.01). https://cdrh-rst.fda.gov/mock-circulatory-loop-generated-database-dynamic-characterization-pressure-based-cardiac-output  

# Disclaimer
**About the Catalog of Regulatory Science Tools**
The enclosed tool is part of the Catalog of Regulatory Science Tools, which provides a peer- reviewed resource for stakeholders to use where standards and qualified Medical Device Development Tools (MDDTs) do not yet exist. These tools do not replace FDA-recognized standards or MDDTs. This catalog collates a variety of regulatory science tools that the FDA's Center for Devices and Radiological Health's (CDRH) Office of Science and Engineering Labs (OSEL) developed. These tools use the most innovative science to support medical device development and patient access to safe and effective medical devices. If you are considering using a tool from this catalog in your marketing submissions, note that these tools have not been qualified as Medical Device Development Tools and the FDA has not evaluated the suitability of these tools within any specific context of use. You may request feedback or meetings for medical device submissions as part of the Q-Submission Program.  
For more information about the Catalog of Regulatory Science Tools, email OSEL_CDRH@fda.hhs.gov.  



**Usage Notes**

The csv files can be downloaded and used directly to characterize pressure-based cardiac output monitoring systems or algorithms. The database has been used in a publication to determine dynamic attributes of an example benchtop pressure-based CO monitoring system [1]. While this database enables testing of certain characteristics that are challenging and impractical to address in clinical studies, it is not a replacement for accuracy testing in clinically relevant patient populations with appropriate reference methods. 

**Contributors**

For more information about the dataset, please contact the authors at: masoud.farahmand@fda.hhs.gov, and christopher.scully@fda.hhs.gov .

**Files**
Total size: 207.7 MB (unzipped).

**References**

[1] Farahmand, M., Bodwell, E., D'Souza, G. A., Herbertson, L. H., & Scully, C. G. (2023). Mock circulatory loop generated database for dynamic characterization of pressure-based cardiac output monitoring systems. Computers in Biology and Medicine, 160, 106979. https://doi.org/10.1016/j.compbiomed.2023.106979 

[2] J. A. Alhashemi, M. Cecconi, and C. K. Hofer, "Cardiac output monitoring: an integrative perspective," (in eng), Crit Care, vol. 15, no. 2, p. 214, 2011, doi: 10.1186/cc9996.

[3]	C. Correa-Gallego et al., "Goal-directed fluid therapy using stroke volume variation for resuscitation after low central venous pressure-assisted liver resection: a randomized clinical trial," Journal of the American College of Surgeons, vol. 221, no. 2, pp. 591-601, 2015.

