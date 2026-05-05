# Greenspace_project722

## Introduction

*Repository for EGM 722 project that uses python for greenspace analyses in NI. Includes code, readme, gitignore and license files.*

The purpose of the code is to allow the user to perform a simple spatial analysis of greenspace availability and accessibility in Northern Ireland, without requiring experience in Geographic Information Systems (GIS). Using the code, the user can answer questions such as which local governments have the highest coverage of greenspaces, what areas are in close distance of greenspaces, and how much land is available for potential greenspaces within a suitable distance of settlements.

The code is provided in the form of a jupyter notebook, to enable the user to use the code interactively, and consists of 4 main parts:
1. An initial setting up of the data, loading the shapefiles and verifying each layer’s co-ordinate reference system (CRS).
2. Coverage analysis: calculating the amount of green space within each area, in terms of Km2 and as a percentage of the total area.
3. Proximity analysis: Counting the number of green spaces within a specified distance of an area and calculating each area’s distance to the nearest greenspace.
4. A basic suitability analysis, utilizing raster layers to calculate the area of land suitable for green space within a specified distance of each area.



---

## Setup and installation






### Prerequisites
Before accessing the code, please ensure that the following are installed on your device:
- `git`: available [here](https://git-scm.com/install/)
- `conda`: which can be installed using [Anaconda Navigator](https://www.anaconda.com/download/success)





### Downloading/cloning the repository 

The reposistory for this project is hosted at: https://github.com/Beebop212/Greenspace_project722

If you have access to a GitHub account, first fork the repository to your own account, and then clone it to your repository using the following command:

`git clone https://github.com/{your_username}/Greenspace_project722.git`

where {your_username} = your GitHub Username

Alternatively, if you do not have access to a GitHub account, clone the repository using the following command:

`git clone https://github.com/Beebop212/Greenspace_project722.git`





### Environment Set Up

Once the repository is cloned, create a conda environment using the **proj_environment.yml** file provided in the repository. This can be done through one of two ways:

a) Importing via. the environments tab in Anaconda Navigator or
b) Entering `conda env create -f proj_environment.yml` on a command prompt or terminal, from the directory where the project repository was cloned

Creating the environment file will install the following packages:

- `geopandas` available at https://geopandas.org/en/stable/
- `cartopy` available at: https://scitools.org.uk/cartopy/docs/latest/
- `jupyterlab` available at: https://jupyter.org/
- `notebook`available at: https://jupyter.org/
- `rasterio` available at: https://rasterio.readthedocs.io/en/stable/
- `pyepsg` available at: https://pyepsg.readthedocs.io/en/latest/
- `folium` available at: https://python-visualization.github.io/folium/latest/
- `rasterstats`available at: https://pythonhosted.org/rasterstats/



## Optional Steps: Downloading the data

While the datasets used in the code have been provided in the repository, they are available online and can be downloaded to replace the files in the data_files folder if you wish.
The data used in this project given below, along with links of where to find and download the data:

- `District Electoral Area Boundaries (2012)` available at: https://admin.opendatani.gov.uk/dataset/osni-open-data-largescale-boundaries-district-electoral-areas-2012/resource/ffdc1fc9-bf50-4987-bdfa-fe6512531db1
- `Local Government District (LGD) Boundaries (2012)` available at: https://admin.opendatani.gov.uk/dataset/osni-open-data-largescale-boundaries-local-government-districts-2012
- `NI Census Data Zone (DZ) Boundaries (2021)` available at: https://www.nisra.gov.uk/publications/super-data-zone-boundaries-gis-format
- `NI Census Super Data Zone (SDZ) Boundaries (2021)` available at: https://www.nisra.gov.uk/publications/data-zone-boundaries-gis-format
- `NI Settlmement Development Limits (2015)` available at: https://www.nisra.gov.uk/support/geography/urban-rural-classification#toc-1
- `NI Greenspaces` viewable [here](https://out-scape.com/greenspace-ni-map/), dowlnoaded via. [arcgis online](https://www.arcgis.com/home/item.html?id=9867486d0d6c4beda45d320ded755f62)  )
