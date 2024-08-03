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

Here is an overview of the Dataset's (pre-processed Limitation sections data of ACL 23) folder structure:

```plaintext
Datasets/
│
├── All Data/                
│   ├──df_all_data.csv   # combined all dataset (Limitation sections of ACL 2023)
│
├── Biomedical NLP /               
│   ├── df_bioNLP.csv   # dataset of bioNLP
│
├── Clinical NLP data/             
│   ├── df_clinical_nlp.csv   # dataset of clinical NLP      
│
├── Computation and written language data/               
│   └── df_CAWL_2023.csv       # datast of CAWL 2023
│
├── Computational approaches data /               
│   ├── df_computational_approaches.csv   # dataset of computational approaches
│
├── Computational approaches to discourse data/             
│   ├── df_CODI23.csv     # dataset of CODI 23 
│
├── Dialogue and conversational QA data/               
│   └── df_third_dialdoc.csv       # datast of third dialdoc
|
├── Discourse relation parsing treebanking data /               
│   ├── df_DISRPT.csv   # dataset of DISRPT
│
├── Findings ACL data/             
│   ├── df_findings_acl.csv   # dataset of findings ACL
│
├── Indigenous Language of the Americas (AmericasNLP) data/               
│   └── df_americasNLP.csv       # datast of americas NLP
│
├── Industry track /               
│   ├── df_industry_track.csv   # dataset of industry track
│
├── Long Papers data/             
│   ├── df_long.csv     # dataset of long papers
│
├── Matching from unstructured and structed data/               
│   └── df_matching_2023.csv      # datast of matching 2023
|
├── NLP for Building Educational Applications (BEA) data/               
│   └── df_BEA_2023.csv       # datast of BEA
│
└── requirements.txt    # Project dependencies
