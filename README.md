# Group5_Capstone_WI25

Instructions to reproduce our model results

Disclaimer: Our model was run on our local machines which all have atleast 32 GB of RAM. Time was taken to ensure that not too much memory was used, but our notebooks will likely not run on system with less than 32GB of RAM. Additionally, our models take a long time to run due to our dataset size. If desired, I've included parameters that can be modified to reduce the computational load which will approximate our results, instructions are mentioned below.

1. Navigate to the 'notebooks' folder
  a. Download and run "1. Preprocessing.ipynb"
    i. This will create a 16.9 GB File called "MMSI-daily_merged_2019_2020-vessels-gfw-seasons.csv" and two smaller files called "MMSI-daily-merged_2019_2020.csv" and "vessels_dropped.csv" to the active directory. This is             the desired file we will be using in the rest of our exploration and modeling phase.
    ii. The last code block merges and saves our dataset in chunks of 1,500,000. The entire output dataset is 107,207,569 observations, so this results in processing 72 chunks. If desired, this can be adjusted higher or lower          to fit the memory constrains of your system. 
    iii. Please ensure to clear this notebook's variables from memory or you may encounter memory errors in later notebooks.
  b. Optionally Download and run "2. Exploration.ipynd"
    i. Note this is purely steps taken for exploring our data and generating visuals and summaries for our final report. If you'd like to verify our visuals and summaries this may be run.
    ii. Please ensure to clear this notebook's variables from meory or you may encounter memory erros in the model notebook.
  c. Download an run "3. Modeling.ipynd"
    i. The sample_n value in the third code block causes us to sample 5% of our data, this can be modified to influence processing time.
    ii. Due to the size of the data, this notebook takes about 3 hours to run on our local machines. Please be patient or modify sample_n accordingly.
    iii. Since we are using random state 20, the results should be exact. This can be verified by comparing the results reporting in our final report to those here.
    iv. The last code block downloads pickle files of our model results. The pickle files are avaliable in this github inside of the "models" folder for comparison.
    v. If memory errors are encounter, please ensure no memory is unncessarily commited on your system.
