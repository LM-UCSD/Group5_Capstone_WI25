# Group5 Capstone WI25
Contributors: Lauren Marrs, Chris Scholz, and Chase Farrell

Group 5's Capstone uses Global Fishing Watch's "Public Fishing Effort" data in order to build a model to predict flag counts for a given grid cell and time. The purpose of this excerise is to build a model that could give an end-user a prediction of which countries and how many vessels from that country will operate in a grid cell and build a model that would predict the flagging of vessels. Predictions of location could give governments and international organizations valuable insights on where clusters of fishing vessels may appear and aid in the enforcement and management of fisheries and Exclusive Economic Zones. While predicitions of flags could give governments and international organizations the ability to determine the likley flag of a vessel obscuring their registration or otherwise not projecting their Automatic identification signal (AIS).

## Instructions to Reproduce Our Model Results

#### Disclaimer
Our model was run on local machines with at least 32 GB of RAM. Although we took steps to minimize memory usage, the notebooks will likely not run on systems with less than 32 GB of RAM. Additionally, our models take a long time to run due to the large dataset. If needed, parameters are provided that can be modified to reduce the computational load and approximate our results. There is no guarantee that systems with smaller memory sizes can run these notebooks. Additional time to test different machine configurations besides on the personal machines of our contributors were not feasible and were not accounted for. If there is a desire to check our models without running our model building step notebook, please skip to the "Pre-Training Model" section for instructions, this notebook uses the pre-trained pickle files present on this repo for reproduction purposes.

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

    Download and run 3. Modeling Location Predicitions.ipynb:
        Sampling Parameter:
            The sample_n value in the third code block samples 5% of the data. Modify this value to influence processing time
            if needed.
        Processing Time:
            Due to the large dataset, this notebook takes a significant amount of time to run on our local machines. 
            Please be patient or adjust sample_n accordingly.
        Reproducibility:
            We use a random state of 20, so the results should be exactly reproducible. You can verify this by comparing the
            outcomes in this notebook with those reported in our final report.
        Model Output:
            The final code block downloads pickle files containing our model results.
            These pickle files are also available in the models folder of this GitHub repository for comparison.
    Memory Note:
        If you encounter memory errors, ensure that no unnecessary data is committed to memory on your system.
        Clear this notebook's variables for memory after runnin it ot prevent memory errors in the next modeling ntoebook.

## Pre-Trained Model 

    Download and run 4. Pre-Trained Model Notebook.ipynb:
        This note book contains steps for using our pre-trained model (pickle file format). This notebook can be
        used to run verify the results of our model if desired and the processing time of our model notebooks
        are untenable.
    Note:
        This notebook uses files present in our github repo and should require no intervention to run if you
        are using Sklearn 1.3.2.
        
        If you are running Sklearn 1.4.2, there are ()_model2.pkl files present in our models folder on this repo
        In the notebook there are commented out url paths to these ()_model2.pkl files. Please comment the url_()
        variables using ()_model.pkl paths out and uncomment the ()model2.pkl paths in. There this a note
        comment in the notebook itself also explaining this. Our notebook does not support other verisons of
        Sklearn, these were just the common verisons our group were running.
    
