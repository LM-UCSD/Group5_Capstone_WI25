# Group5_Capstone_WI25
Contributors: Lauren Marrs, Chris Scholz, and Chase Farrell

Group 5's Capstone uses Global Fishing Watch's "Public Fishing Effort" data in order to build a model to predict flag counts for a given grid cell and time. The purpose of this excerise is to build a model that could give an end-user a prediction of which countries and how many vessels from that country will operate in a grid cell. Predictions of this nature could give governments and international organizations valuable insights on where clusters of fishing vessels may appear and aid in the enforcement and management of fisheries and Exclusive Economic Zones.

## Instructions to Reproduce Our Model Results

#### Disclaimer
Our model was run on local machines with at least 32 GB of RAM. Although we took steps to minimize memory usage, the notebooks will likely not run on systems with less than 32 GB of RAM. Additionally, our models take a long time to run due to the large dataset. If needed, parameters are provided that can be modified to reduce the computational load and approximate our results, although there is no guarantee that systems with smaller memory sizes can run these notebooks. Additional time to test different machine configurations were not feasible.

Instructions are detailed below.

### Preprocessing

    Navigate to the notebooks folder.
    Download and run 1. Preprocessing.ipynb:
        Output Files:
            A 16.9 GB file: MMSI-daily_merged_2019_2020-vessels-gfw-seasons.csv (saved in the active directory)
            Two smaller files: MMSI-daily-merged_2019_2020.csv and vessels_dropped.csv (saved in the active directory)
        These files will be used for the rest of the exploration and modeling phase.
        Chunk Processing:
            The final code block merges and saves the dataset in chunks of 1,500,000 rows.
            The complete dataset consists of 107,207,569 observations, resulting in 72 chunks.
            You can adjust the chunk size to better fit your system’s memory constraints.
        Memory Note:
            Please clear this notebook's variables from memory after running it to avoid memory errors in 
            subsequent notebooks.
            
### Exploration (Optional)

    Download and run 2. Exploration.ipynb:
        This notebook contains steps for data exploration and generates visuals and summaries for our final report.
        If you wish to verify our visuals and summaries, you may run this notebook.
    Memory Note:
        Clear this notebook's variables from memory after running it to prevent memory errors in the modeling notebook.
   
### Modeling

    Download and run 3. Modeling.ipynb:
        Sampling Parameter:
            The sample_n value in the third code block samples 5% of the data. Modify this value to influence processing time
            if needed.
        Processing Time:
            Due to the large dataset, this notebook takes about 3 hours to run on our local machines. Please be patient or adjust
            sample_n accordingly.
        Reproducibility:
            We use a random state of 20, so the results should be exactly reproducible. You can verify this by comparing the
            outcomes in this notebook with those reported in our final report.
        Model Output:
            The final code block downloads pickle files containing our model results.
            These pickle files are also available in the models folder of this GitHub repository for comparison.
    Memory Note:
        If you encounter memory errors, ensure that no unnecessary data is committed to memory on your system.
