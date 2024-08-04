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
|
├── NLP for conversational AI data/             
│   ├── df_NLPConvAI.csv   # dataset of NLPconvAI
│
├── Narrative understanding data/               
│   └── df_narrative_understanding.csv   # datast of narrative understanding
│
├── Natural language reasoning and structured explanations data/           
│   ├── df_NLRSE.csv   # dataset of NLRSE
│
├── Online abuse and harms data/             
│   ├── df_woah.csv     # dataset of WOAH
│
├── Representation learning for NLP data/               
│   └── df_Repl4NLP.csv      # datast of Repl4NLP
|
├── Sigmorphon data/               
│   └── df_sigmorphon.csv       # datast of sigmorphon
|
├── Spoken language translation data/               
│   └── df_IWSLT.csv   # datast of spoken language translation data
│
├── Student research workshop data/           
│   ├── df_student_research_workshop.csv   # dataset of student research workshop
│
├── Sustain NLP data/             
│   ├── df_sustain_NLP.csv     # dataset of sustain NLP
│
├── Trust NLP data/               
│   └── df_trust_NLP.csv     # datast of trust NLP
|
├── short papers data/               
   └── df_short.csv     # datast of short papers ```


### Code 

Here is an overview of the code folder structure:

```plaintext
Datasets/
│
├── LLM Prompt/                
│   ├── Prompt_Engineering.ipynb   # code regarding prompt engineering process to LLM to generate topics, title, and relevant text
│
├── Fine tuned LLM /               
│   ├── Llama_fine_tuning.ipynb   # code reagarding fine tuning of Llama 2 for generating topics, title, and relevant text
│
├── BERTopic /             
│   ├── BERTopic.ipynb   # applying BERTopic to generate topics (topic words) and representative docs of each topic      
│
├── BERTopic + LLM /    # various model and LLMs used with BERTopic to generate topic titles with relevant text           
│    └── LDA.ipynb      # use Latent Dirchlet Allocation (LDA) to model to generate topics, and aggregrate texts of each topic
│    ├── Llama_2.ipynb  # used Llama 2 intergrating with BERTopic to generate title, and relevant text (result is not good)
│    ├── Mistral.ipynb  # used Mistral intergrating with BERTopic to generate title, and relevant text (result is not good). One of the main reason is token limit 512 
│    ├── gpt_3_5.ipynb  # used GPT 3.5 api after applying BERTopic to generate title, and relvant text. Title was good but not relevant text
│    ├── Llama_13b.ipynb # the performance was almost similar to Llama 2 
│    ├── gpt_4.ipynb    # integrating GPT 4 after applying BERTopic provides best results and the titles, relevant text is very good
|
├── Data preprocessing /               
│   ├── Data_preprocessing.ipynb  # taking the dataset and apply pre processing, such as remove unnessary text, links, symbols. 
|
├── LLM text summarization /               
│   ├── Text_summarization.ipynb  # taking the 'representative docs' after applying BERTopic and apply LLM text summarizer to get very relevant, cohesive 'relevant text'
|
├── visualization /               
│   ├── keyBERT_and_Visualization.ipynb  # apply `keyBERT' in 'representative docs' to generate coherence score and various visualization such as heatmap, hierarchical clustering, 
 

