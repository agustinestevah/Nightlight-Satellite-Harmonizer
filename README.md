# NightLight-Satellite-Harmonizer
Are you annoyed about the jump in resolution from the pre-2013 DMSP Satellite to the post 2012 VIIRS Satellite? I follow the methodology in existing literature to create Stata code to harmonize the data.

I follow _Li, X., Zhou, Y., Zhao, M. et al. A harmonized global nighttime light dataset 1992–2018. Sci Data 7, 168 (2020)_ and _Zhao, M. et al. Building a Series of Consistent Night-Time Light Data (1992–2018) in Southeast Asia by Integrating DMSP-OLS and NPP-VIIRS. IEEE Trans. Geosci. Remote. Sens. 58, 1843–1856 (2019)_ to code an outline for how to harmonize the data. 

Methodology:
  1) (Not implemented due to time constraints and accurate results without) Clean up the noise (from clouds) of the VIIRS (Post 2011) Satellite Data. Follow the paper if you want to do this.
  2) Make a log transform of the VIIRS data and use a sigmoid fit (trained on either 2012 or 2013 overlapping data) to gather coefficients for an appropriate transformation to apply to later years.
  3) Merge.
  4) Analyze results by creating a table viewing var, skewness, kurtosis, and means to check for consistency across years.

This code was made originally from VIIRS and DMSP nightlight satellight data of Rwanda for my Econ lab, so change it as you see fit.
