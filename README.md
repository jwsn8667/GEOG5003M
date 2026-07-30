# GEOG5003M
Repository for Assignment 2 in Programming for Geographical Information and Analysis

A fully reproducible spatial data science report is presented as a Jupyter notebook, investigating determinants of local variation in greenhouse gas emissions from domestic gas and electricity use per household, in Sheffield MSOAs.

**Background**

Domestic gas, electricity and other energy use comprised nearly a quarter of all UK territorial greenhouse gas (GHG) emissions in 2021, more than any other sector apart from transport [1].  Notwithstanding the rapid decarbonisation of UK electricity supply [2], cutting emissions from domestic energy use remains a significant challenge: in 2021, only 77.85% of domestic energy use was from non-electrical sources [3].  Air source heat pumps have emerged as the leading low-carbon alternative to natural gas heating in most households [4] but risk increasing energy costs in poorly insulated homes [5].

To date, government financial support for energy efficiency improvements in England has been directed at ‘low income, low energy efficiency’ households [6], but this ‘LILEE’ definition of fuel poverty has been criticised as a poor measure which is insensitive to effect of multiple energy price crises on household energy bills [7].  Whereas alleviating fuel poverty has been cited as a potential ‘co-benefit’ of mitigating climate change, not least by the Committee on Fuel Poverty [8], there is a complementary suspicion that higher-earning households might be guilty of ‘energy decadence’, using more energy than really needed to maintain a decent standard of living [9].  A recently published survey of energy use in South Yorkshire [10] complicates any assumptions of ‘energy decadence’ in the region, with its finding that higher-earning households are no less motivated to cut their energy or to protect the environment.

By investigating determinants of GHG emissions from domestic gas and electricity use in Sheffield, this project aims to explore potential additional or alternative characterisations of energy use, beyond a ‘fuel poor’/‘energy decadent’ binary, which might support local climate change policy goals.

**Materials and Methods**

All code was written in Python 3 in a Jupyter notebook environment: a full summary of packages used is available below.

|Package|Version|Sub-module(s)|
|---|---|---|
|**Standard packages for data analysis:**|
|numpy|2.0.2|-|
|pandas|2.2.2|-|
|matplotlib|3.10.0|pyplot, colors|
|seaborn|0.13.2|-|
|**Processing and visualising spatial data**:|
|geopandas|1.1.4|-|
|contextily|1.7.1|-|
|pyproj|3.7.2|-|
|matplotlib-map-utils|4.1.1|core.north_arrow, core.scale_bar|
|shapely|2.1.2|geometry|
|**Data collection:**|
|requests|2.32.4|-|
|json|-|-|
|**Statistical modelling:**|
|scipy|1.16.3|stats|
|sklearn|---|linear_model, preprocessing|
|**Miscallaneous:**|
|warnings|-|-|

**Table**: Python packages used in analysis.

All code and data inputs are available from the GitHub repository for the project, albeit Census data are retrieved directly from nomis API and are not saved as duplicate, local versions.  Code is commented throughout, interspersed with additional supporting information.  All data are open source, published under the Open Government Licence.  Datasets are selected to align as closely as possible with a 2021 data period, to facilitate comparison between sources.

OLS regression and K-means clustering statistical modelling techniques are applied, (1) to identify net annual income and energy efficiency score as determinants of emissions and (2) to define ‘income-energy efficiency’ clusters of MSOAs, supporting the interpretation of insights in a local policy context.  Final outputs are presented in one spatial, one non-spatial data visualisation, designed for accessibility and to support visually supported inferences by a non-technical audience.

A separate reference list is provided below for citations in this readme file; there is a dedicated reference section for citations in the Jupyter notebook.

**References**

1.  DESNZ.  *UK local authority and regional greenhouse gas emissions statistics, 2005 to 2024*.  [Online].  2026.  [Accessed 30 July 2026].  Available from: https://www.gov.uk/government/statistics/uk-local-authority-and-regional-greenhouse-gas-emissions-statistics-2005-to-2024
2.  NESO.  *Clean Power 2030*.  [Online].  2024.  [Accessed 20 July 2026].  Available from: https://www.neso.energy/document/346651/download
3.  DESNZ.  *Total final energy consumption at regional and local authority level: 2005 to 2023*.  [Online].  2025.  [Accessed 30 July 2026].  Available from: https://www.gov.uk/government/statistics/total-final-energy-consumption-at-regional-and-local-authority-level-2005-to-2023
4.  CCC.  *The Seventh Carbon Budget*.  [Online].  2025.  [Accessed 30 July 2026].  Available from: https://www.theccc.org.uk/wp-content/uploads/2025/02/The-Seventh-Carbon-Budget.pdf
5.  Sherriff, G., Butler, D. & Brown, P.  'The reduction of fuel poverty may be lost in the rush to decarbonise': Six research risks at the intersection of fuel poverty, climate change and decarbonisation.  *People, Place and Policy*.  [Online].  2022, pp.1-20.  [Accessed 30 July 2026].  Available from: http://dx.doi.org/10.3351/ppp.2022.3776894798
6.  GOV.UK.  *Help from your energy supplier: the Energy Company Obligation*.  [Online].  [No date].  [Accessed 30 July 2026].  Available from: https://www.gov.uk/energy-company-obligation
7.  McKnight, A.  There’s a problem with how we measure fuel poverty. 25 Febbruary.  *LSE British Politics*.  2025.  [Online]. [Accessed 30 July 2026]. Available from: https://blogs.lse.ac.uk/politicsandpolicy/theres-a-problem-with-how-we-measure-fuel-poverty/
8.  Committee on Fuel Poverty.  *Response to Tackling Fuel Poverty report by the Centre for Sustainable Energy*.  [Online].  [No date].  [Accessed 30 July 2026].  Available from: https://assets.publishing.service.gov.uk/media/5b167e8240f0b634b73dbe82/Research_by_CSE_for_CFP_-_Policy_Tensions_and_Synergies_-_CFP_response-.pdf
9.  Chatterton, T, Barnes, J., Yeboah, G. & Anable, J.  Energy justice? A spatial analysis of variations in household direct energy consumption in the UK.  In: *eceee 2015 Summer Study on energy efficiency, 1-6 June 2015, Giens Peninsula*.  [Online].  Stockholm: European Council for an Energy Efficient Economy, 2016.  [Accessed 30 July 2026].  Available from: https://www.eceee.org/library/conference_proceedings/eceee_Summer_Studies/2015/1-foundations-of-future-energy-policy/energy-justice-a-spatial-analysis-of-variations-in-household-direct-energy-consumption-in-the-uk/
10.  Carrick, J. & Wood, M.  What drives energy decadence? Survey evidence on energy consumption perceptions in South Yorkshire.  *Local Environment*.  [Online].  2026, pp.1-20.  [Accessed 30 July 2026].  Available from: https://doi.org/10.1080/13549839.2026.2644484
