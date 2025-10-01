# Non-tidal loading in Antarctica
This repository contains code used to analyse effectiveness of non-tidal loading (NTL) corrections in Antarctica.
## Repository structure
### Improving-GNSS-NTL
This folder contains Jupyter notebooks for applying NTL corrections to GNSS time series and analysing their effectiveness. The focus is on Antarctic GNSS stations and how different NTL models (atmospheric, oceanic, hydrological) affect displacement estimates, noise properties, and stability of long-term trends. <br />
**Note**: GNSS data is not included, but links to their sources are provided. NTL corrections are downloaded directly from the EOST (École & Observatoire des Sciences de la Terre, Strasbourg) and ESMGFZ (Earth System Modelling Group of GeoForschungsZentrum Potsdam) services within the scripts.
- `NTL_corrections.ipynb` <br />
  Applies NTL corrections (atmospheric oceanic, hydrological) to GNSS displacement time series.
  - Downloads loading displacement series from the EOST and ESMGFZ services.
  - Preprocesses and aligns loading data with GNSS time series.
  - Applies NTL corrections to GNSS time series.
  - Saves corrected series in Hector-compatible `.mom` format.
- `NTL_analysis.ipynb` <br />
  Analyses Hector-processed GNSS data and evaluates the impact of NTL corrections
    - Compares uncorrected and corrected GNSS time series.
    - Evaluates trend estimates, seasonal amplitudes, RMS, and noise characteristics.
    - Produces plots and tables for comparison across datasets and stations.
