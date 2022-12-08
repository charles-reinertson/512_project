# DATA 512 Course Project
# Covid Analysis + Mask Compliance Forecasting

This project is broken down into two parts

**Part 1 - Common Analysis sets the stage for the subsequent assignments. In A4 you conduct a base analysis.** 

    1. Notebook: part_1.ipynb
    2. Files: covid_case_changepoints.jpg, derivation.jpg

**Part 2 - Extension Plan asks a human centered data science question that extends the Common Analysis.** 

    1. Notebooks (in order of execution): step_1_clean_train_data.ipynb, step_2_train_model.ipynb, step_3_clean_prod_data.ipynb, step_4_prod_model.ipynb 
    2. Files: models/*, outputted_images/*, data/*
    
    note: the file data/* is where all intermediary data files and initial data files must be present.

**Data Descriptions**

    1. The RAW_us_confirmed_cases.csv file from the Kaggle repository of John Hopkins University COVID-19 data. This data is updated daily. You can use any revision of this dataset posted after October 1, 2022. Liscense Attribution 4.0 International (CC BY 4.0) which means we are free to share and adapt this data. (https://www.kaggle.com/datasets/antgoldbloom/covid19-data-from-john-hopkins-university?select=RAW_us_deaths.csv)
    
    2. The CDC dataset of masking mandates by county. Note that the CDC stopped collecting this policy information in September 2021. (https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i)
    
    3. The New York Times mask compliance survey data. The New York Times Company is providing this database under the following free-of-cost, perpetual, non-exclusive license - https://github.com/nytimes/covid-19-data/blob/master/LICENSE.  (https://github.com/nytimes/covid-19-data/blob/master/mask-use/mask-use-by-county.csv)

**Intermediary Data Files**

    1. cleaned_data.csv - After running the three intermediary data files through the notebook step_1_clean_train_data.ipynb, the output of this file is this csv file that is used for model training.
    2. validate_data.csv - Performs the same steps that created cleaned_data.csv except for the counties that the model did not see during training (counties named Wayne). This action is performed in step_3_clean_prod_data.ipynb.
    3. model.pt - After the model is trained in step_2_train_model.ipynb, we save the trained model in models/model.pt so it can be used on our test data in step_4_prod_model.ipynb.
