Dataset
Fishing Effort
Last Update
03/18/2021
description
Global Datasets of AIS-based Fishing Effort and Vessel Presence

This dataset contains the Global Fishing Watch AIS-based fishing effort and vessel presence datasets. Data is based on fishing detections of >114,000 unique AIS devices on fishing vessels, of which ~70,000 are active each year. Fishing vessels are identified via a neural network classifier, vessel registry databases, and manual review by GFW and regional experts. Data are binned into grid cells 0.01 (or 0.1) degrees on a side and measured in units of hours. The time is calculated by assigning an amount of time to each AIS detection (which is the time to the previous position), and then summing all positions in each grid cell.

Data are available in two formats:

1) Fishing effort by flag state and gear type at 100th degree resolution
2) Fishing effort by MMSI at 10th degree resolution

Each version of the fishing effort dataset is accompanied by a table of vessel information (e.g. gear type, flag state, dimensions, etc.).

Note: When attempting to download multiple files, you will receive an email containing download links after the data has been packaged. For large requests, it may take up to 24 hours to receive this email.
Versions

The fishing effort data is updated periodically to include more recent data and as improvements are made to our models and input data. Data from different major/minor versions should not be combined, as each version uses a different set of inputs.
Current version

    2.0: Fishing effort data for 2012-2020 using our latest AIS algorithms, neural network models, and vessel registry database.

Archived versions

    1.5: A provisional update to version 1.0, including data for 2012-2018 and an additional 11 gear types.
    1.0: The initial release of our fishing effort data, including data for 2012-2016, which accompanied our "Tracking the footprint of fisheries" publication.

File structure

Fishing effort and vessel presence data are available as .csv files in daily formats. Files for each year are stored in separate .zip files. A README.txt file is provided for each dataset version and contains the table schema and additional information. There is also a README-known-issues-v2.txt file outlining some of the known issues with the version 2 release.

Files are names according to the following convention:

    Daily file format: [fleet/mmsi]-daily-csvs-[100/10]-[version]-[year].zip
    Fishing vessel format: fishing-vessels-[version].csv
    README file format: README-[fleet/mmsi/fishing-vessels]-[version].txt

File identifiers:

    [fleet/mmsi]: Data by fleet (flag and geartype) or by MMSI
    [100/10]: 100th or 10th degree resolution
    [version]: Fishing effort version (v2, v1-5,v1)
    [year]: Year of data included in .zip or .csv file

Examples: fleet-daily-csvs-100-v2-2020.zip; mmsi-daily-csvs-10-v2-2020.csv; fishing-vessels-v2.csv; README-fleet-v2.txt
Reference & Code

For additional information about these results, see the associated journal article: D.A. Kroodsma, J. Mayorga, T. Hochberg, N.A. Miller, K. Boerder, F. Ferretti, A. Wilson, B. Bergman, T.D. White, B.A. Block, P. Woods, B. Sullivan, C. Costello, and B. Worm. "Tracking the global footprint of fisheries." Science 361.6378 (2018).

    GitHub repository for Tracking the global footprint of fisheries: https://github.com/GlobalFishingWatch/paper-global-footprint-of-fisheries

License

Unless otherwise stated, Global Fishing Watch data is licensed under a Creative Commons Attribution-ShareAlike 4.0 International license and code under an Apache 2.0 license.