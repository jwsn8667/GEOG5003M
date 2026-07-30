# GEOG5003M
Repository for Assignment 2 in Programming for Geographical Information and Analysis

A fully reproducible spatial data science report is presented as a Jupyter notebook, investigating determinants of local variation in greenhouse gas emissions from domestic gas and electricity use per household, in Sheffield MSOAs.

**Background**

Domestic gas, electricity and other energy use comprised nearly a quarter of all UK territorial greenhouse gas (GHG) emissions in 2021, more than any other sector apart from transport [1].  Notwithstanding the rapid decarbonisation of UK electricity supply [2], cutting emissions from domestic energy use remains a significant challenge: in 2021, only 77.85% of domestic energy use was from non-electrical sources [3].  Air source heat pumps have emerged as the leading low-carbon alternative to natural gas heating in most households [4] but risk increasing energy costs in poorly insulated homes [5].

To date, government financial support for energy efficiency improvements in England has been directed at ‘low income, low energy efficiency’ households [6], but this ‘LILEE’ definition of fuel poverty has been criticised as a poor measure which is insensitive to effect of multiple energy price crises on household energy bills [7].  Whereas alleviating fuel poverty has been cited as a potential ‘co-benefit’ of mitigating climate change, not least by the Committee on Fuel Poverty [8], there is a complementary suspicion that higher-earning households might be guilty of ‘energy decadence’, using more energy than really needed to maintain a decent standard of living [9].  A recently published survey of energy use in South Yorkshire [10] complicates any assumptions of ‘energy decadence’ in the region, with its finding that higher-earning households are no less motivated to cut their energy or to protect the environment.

By investigating determinants of GHG emissions from domestic gas and electricity use in Sheffield, this project aims to explore potential additional or alternative characterisations of energy use, beyond a ‘fuel poor’/‘energy decadent’ binary, which might support local climate change policy goals.

**Materials and Methods**

All code was written in Python 3 in a Jupyter notebook environment: a full summary of packages used is available below.

|Package|Version|Sub-module(s)|Citation|
|---|---|---|---|
|**Standard packages for data analysis:**|
|numpy|2.0.2|-|---|
|pandas|2.2.2|-|---|
|matplotlib|3.10.0|pyplot, colors|---|
|seaborn|0.13.2|-|---|
|**Processing and visualising spatial data**:|
|geopandas|1.1.4|-|---|
|contextily|1.7.1|-|---|
|pyproj|3.7.2|-|---|
|matplotlib-map-utils|4.1.1|core.north_arrow, core.scale_bar|---|
|shapely|2.1.2|geometry|---|
|**Data collection:**|
|requests|2.32.4|-|---|
|json|-|-|---|
|**Statistical modelling:**|
|scipy|1.16.3|stats|---|
|sklearn|---|linear_model, preprocessing|---|
|**Miscallaneous:**|
|warnings|-|-|---|

**Table**: Python packages used in analysis.

All code and data inputs are available from the GitHub repository for the project, albeit Census data are retrieved directly from nomis API and are not saved as duplicate, local versions.  Code is commented throughout, interspersed with additional supporting information.  All data are open source, published under the Open Government Licence.  Datasets are selected to align as closely as possible with a 2021 data period, to facilitate comparison between sources.

OLS regression and K-means clustering statistical modelling techniques are applied, (1) to identify net annual income and energy efficiency score as determinants of emissions and (2) to define ‘income-energy efficiency’ clusters of MSOAs, supporting the interpretation of insights in a local policy context.  Final outputs are presented in one spatial, one non-spatial data visualisation, designed for accessibility and to support visually supported inferences by a non-technical audience.

A separate reference list is provided below for citations in this readme file; there is a dedicated reference section for citations in the Jupyter notebook.

**References**

1.  Local and Regional GHG...
2.  *Grid decarbonisation timeline*
3.  Total final energy consumption...
4.  *ASHP leading low carbon technology for domestic heating - CCC?*
5.  Research risks, Salford Uni.
6.  *ECO eligibility*
7.  LSE blog
8.  CFP
9.  2015 energy excess research paper
10.  Jayne Carrick
