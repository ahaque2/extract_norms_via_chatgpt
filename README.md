# Extracting Norms from Contracts Via ChatGPT: Opportunities and Challenges

We investigate the effectiveness of ChatGPT in extracting norms from contracts. Norms provide a natural way to engineer multiagent systems by capturing how to govern the interactions between two or more autonomous parties. We extract norms of commitment, prohibition, authorization, and power, along with associated norm elements (the parties involved, antecedents, and consequents) from contracts. Our investigation reveals ChatGPT's effectiveness and limitations in norm extraction from contracts. ChatGPT demonstrates promising performance in norm extraction without requiring training or fine-tuning, thus obviating the need for annotated data, which is not generally available in this domain. However, we found some limitations of ChatGPT in extracting these norms that lead to incorrect norm extractions. The limitations include oversight of crucial details, hallucination, incorrect parsing of conjunctions, and empty norm elements. Enhanced norm extraction from contracts can foster the development of more transparent and trustworthy formal agent interaction specifications, thereby contributing to the improvement of multiagent systems.

### To run the code

Use Jupyter Notebook 1_Extract_norms_via_chatgpt.ipynb to extract norms via ChatGPT from contract clauses. The contract clauses are sampled from the Contract Understanding Atticus Dataset \((CUAD)[https://www.atticusprojectai.org/cuad]\)
You will need an OpenAI (ChatGPT) account to be able to run this code. Just replace the _your_api_key_ in the code with your API key in the code.

We use prompts to extract the norms. Prompts can be found under the 'prompt' folder.

### Analysis

#### Dataset

The 'dataset' folder contains the sampled clauses. 
- _sample_100.csv_ contains 100 contract clauses sampled from CUAD, and
- _challenging_examples.csv_ contains clauses with complex sentences we identified based on keywords such as
    - _multiple conjunctions_ in a clause such as or \& and that can complicate the interpretation of clause
    - _conditional words_ such as upon, provided, that can add subtle conditions that may be challenging to detect, and
    - _temporal words_ such as until, sooner, and later that can make the clause conditioned upon some time-bound actions.
    - 

#### Analysis

The results can be found under the 'results' folder.  
- _sample_100_results_analysis.csv_ contains the norms extracted using the prompts contained in the 'prompt' folder.
- _challenging_examples.csv_ contains some of the challenging examples (identified via keyword-based search) along with extracted norms and the authors' comments for the extracted norms

If you use our work, kindly cite the following paper.

Amanul Haque, and Munindar P. Singh. *"Extracting Norms from Contracts Via ChatGPT: Opportunities and Challenges."* arXiv preprint arXiv:2404.02269 (2024).
