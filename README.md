# SLR-toolkit
Machine Learning toolkit for selecting studies and topics in systematic literature reviews


## Setup
- Python >3
- Packages : `pandas`, `sklearn`, `scipy`, `networkx`, `community`, `matplotlib`, `itertools`, `collections`
- To install the module `community` follow https://python-louvain.readthedocs.io/en/latest/api.html


## Usage

### STEP1
- Clone repository:
   ```bash
   git clone https://github.com/andrisimonetti/SLR-toolkit.git

#### or
1. Download `toolkit_functions.py` to import the functions needed.
2. Download and run the Notebook `Main Analysis.ipynb` following the instrunctions about the input file required. The file `Dataset_Input_example` provide an example
   
### STEP2
1. Select the relevant topics and assign them the labels: create file excel, as in the file `topic_label_example.xlsx`.
2. Download and run the Notebook `Topic stats and plots.ipynb` following the instrunctions about the input file required.


## Read the outputs:
After running the Notebook `Main Analysis.ipynb` the outputs produced consist of 3 files: 
   - 'svn_words.txt': data frame describing the Statistically Validated Network; each row represents a link between two nodes ('source' and 'target') with its p-value and correlation coefficient.
   - 'topic_definition.xlsx': data frame describing the Topics found as community of words in the Statistically Validated Network;
   - 'Topic_Document_association.xlsx': data frame describing the associations between documents and topics; 'topic_0' represents the 'General'
 topic.


After running the Notebook `Topic stats and plots.ipynb` the outputs produced consist of 3 files:
   - 'stats_topic.xlsx': data frame describing the topics and some related statistics
   - 'topic_overview_1.pdf': scatter-plot of documents along two dimensions: 'ratio of citations' (x-axis) and 'ratio of top journals' (y-axis)
   - 'topic_overview_2.pdf': scatter-plot of documents along two dimensions: 'number of internal citations' (x-axis) and 'total number of citations' (y-axis)
