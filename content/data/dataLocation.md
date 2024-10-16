---
title: 'Data Description'
date: 2019-02-11T19:27:37+10:00
weight: 2
---

The PI Instrument page is found at https://oceanobservatories.org/pi-instrument/cabled-array-vent-imaging-sonar-covis/ . This is the official description of COVIS for the Ocean Observatories Initiative (OOI).
COVIS data from the OOI deployment can be found at  http://piweb.ooirsn.uw.edu/covis/. This folder has two subfolders ~/covis/data/ and ~/covis/processed/.  

The raw data is under ~/covis/data/ which contains ~BROWSE/, ~COVIS/, ~COVIS-ENG/, and ~INPUT/.  All COVIS raw data files come in a compressed file folder (...tar.gz).
- **BROWSE** - data organized in folders by year and julian day  (same data as in COVIS and INPUT but reorganized in folders rather than just a long list)
- **COVIS** - incoming data from 2018 to 2020
- **COVIS-ENG** -- information on COVIS operations but only 2018-2020
- **INPUT** - incoming data from 2020 to 2023

The processed data is under ~/covis/processed/
- **2019 Thermistor Data/** - temperature data from small arrays of RBR solo thermistors set within COVIS’s field of vision - this is a curated data set related to a particular publication [\[ 5 \]]({{< relref "#References and Acknowledgments" >}})
- **Automatic_Postprocessing_Version3.2/** - processed data 2020 - 2023
- **COVIS_data_structure_description_diffuse_rev1.pdf** - description of the processed data files (.mat format containing a single structure called covis) for the diffuse mode results
- **COVIS_data_structure_description_imaging_rev1.pdf** - description of the processed data files (.mat format containing a single structure called covis) for the imaging mode results
- **latest/** - processed data 2020 - 2023 - seems to be same as Automatic_Postprocessing_Version3.2/ but was probably intended to be more temporary

Data collection varies a bit but for 2020-2023, COVIS was collecting diffuse mode data hourly every day for 6 days and then imaging and doppler mode data hourly on the 7th day. Note that a diffuse map output is also computable from the imaging data so you will see diffuse mode files every day. There is no automatic computation of doppler mode data so those files are empty or missing (but the raw data exists).

**Data file sizes:**\
Diffuse files are 325 kb or thereabouts (varies a bit but shouldn’t be much smaller)\
Imaging files are 21.5 Mb or thereabouts 



COVIS code repository: https://github.com/COVIS-Sonar/postprocessing.git.  This has both the operational processing code to get from raw data (including all inputs other than the raw data files) to gridded data as well as some (very basic) visualization options.


{{< rawhtml >}}
<div style="height:  20px"></div>
{{< /rawhtml >}} 

----------   

{{< rawhtml >}}
<div style="height:  20px"></div>
{{< /rawhtml >}}