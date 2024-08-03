# LimTopic: LLM-based Topic Modeling and Text Summarization for Analyzing Scientific Articles limitations

## Description:
This work uses various LLM with BERTopic to generate topics, titles, and relevant text in a scientific article's 'limitation' section. 
This work includes experiments, including Prompt Engineering, Fine-tuning LLM, BERTopic, and integrating various LLMs with BERTopic. Also, it includes text summarization with LLM to generate a very cohesive
'relevant text' of each topic.


![Screenshot from 2024-08-03 03-28-07](https://github.com/user-attachments/assets/a45bf4d0-ca25-4194-b625-8b39ff382d2d)

### Create a virtual environment: (Step 1): 
mkdir my_project 

cd my_project

### Activate the virtual environment (Step 2): 
env\Scripts\activate (windows)

source env/bin/activate

### install related libraries (Step 3):
pip install -r requirements.txt


### Dataset 

## Project Directory Structure

Here is an overview of the project's folder structure:

```plaintext
Project_Root/
│
├── All Data/                # Source files
│   ├──df_all_data.csv   # combined all dataset (Limitation sections of ACL 2023)
│   ├── module1.py      # Sample module
│   └── module2.py      # Another module
│
├── data/               # Data files
│   ├── datafile1.csv   # Sample data file
│   └── datafile2.csv   # Another data file
│
├── tests/              # Test scripts
│   ├── test1.py        # Test script for module1
│   └── test2.py        # Test script for module2
│
├── docs/               # Documentation files
│   └── README.md       # Project documentation
│
└── requirements.txt    # Project dependencies
