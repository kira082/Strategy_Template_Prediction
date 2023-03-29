# Strategy_Template_Prediction
## Predicting Strategy Templates and Block Templates of a plant based on historical data

# Installation
Install python 3.11.8
- command prompt − type path %path%;C:\Python and press Enter.

Open a terminal and run:
- pip install -r requirements.txt


# Code

### code_wrapper.py
- library imports, fastapi initilization
- local configuration file import
- warning list and message initilization
- fastapi post method
- Database connection
- extracting data from the json input
- interchanging columns as required
- validating the received data
- extracting project information from the input data
- calling the main function
- returning the output

### Main_Template_Recommendation.py
  - extracting encoding, strategy, block, confidence score models from pickle files
  -  importing required tables from the database and local files
  -  renaming the columns as required
  -  validating the data
  -  calling preparation function
  -  calling preprocessing function
  -  calling strategy template prediction, its confidence score
  -  calling block prediction, its confidence score
  - calling post validation
  - calling data conversion function
  - aggregating the data and returing it to the 'code_wrapper' file

### Pre_Processing.py

  - model and enduser selection function
  - model encoding selection function
  - pre and post filter, grouping the tags, filtering the tags function
  - preprocessing steps for OilandGas, Desal and Satorp plants
  - NLP loop category function
  

### Preparation.py

  - Deriving IOType from IOType
  - System Derivation from System
  - Deriving Interlock using PFD specific columns

### db_connect.py
  - connect and disconnect functions to the Database

### Data_Validation.py
  - validation steps fro RTDB data and configuration input file

### encoder.py
  - custom encoding data for encoding during Strategy and Block prediction

### Post_Validation.py
  - block rule based
  - validating the predicted model
  - converting  the templates and block data
### Text_Preprocessor.py

### Data

- config.json : all the user inputs stored here
- corpus.xlsx : training data required for the NLP model
- db_config.pkl : Database information in pickled format
- Feature_Extraction.xlsx : local data required for preprocessing
- TEMPLATE_IO_MAP_DATA.xlsx : mapping table required for pre and post filtering the data

**Features**


**Target Variable**


**DataBase**








# Run
Open a terminal and go to 
- Write in the command prompt: SET the path of project directory.
- Run in terminal command : 
- python code_wrapper.py




