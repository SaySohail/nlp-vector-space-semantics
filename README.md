



<h3 align="center"> Vector Space Semantics for Similarity between Eastenders Characters</h3>

<div align="center">

  [![code coverage](coverage.svg "Code coverage")]()
</div>

---


## 🧐 About <a name = "about"></a>

In this assignment, the goal is to create a vector representation of character documents containing lines spoken by characters in the Eastenders script data. The vector representations will be improved to maximize the distinction between character documents. This distinction will be measured based on the performance of an information retrieval classification method, which aims to select documents from the validation and test data accurately.

The assignment consists of several tasks aimed at improving the vector representations, pre-processing techniques, linguistic feature extraction, analyzing similarity results, incorporating dialogue context and scene features, improving vectorization methods, and conducting final testing on the test data. The main metric to focus on is the mean rank, where lower values indicate better performance.

### Pre-processing:
* Enhance the pre_process function by incorporating pre-processing techniques learned in the module.
* Use the 90% train and 10% validation data split from the training file to evaluate the improvements.
* Aim to reduce the mean rank and improve accuracy on the test and validation sets.
### Improve Linguistic Feature Extraction:
* Apply feature extraction techniques to enhance the to_feature_vector_dictionary function.
* Explore techniques such as n-gram extraction, POS-tagging, sentiment analysis, and gender classification (without using the GENDER column directly).
* Utilize feature selection/reduction techniques like minimum/maximum document frequency and k-best selection.
* Evaluate the impact of the techniques on the mean rank.

### Analyze Similarity Results:
* Identify character vectors from the 90%/10% training/validation split that are closest to each character's training vector but not the character themselves.
* Analyze the language use similarities that result in similar word or n-gram features.
* Provide observations and explanations for instances where the highest match is not successful.

### Add Dialogue Context and Scene Features:
* Modify the create_character_document_from_dataframe function to include dialogue context and scene features.
* Incorporate lines spoken by other characters in the same scene to capture the context.
* Utilize the Episode, Scene, and scene_info columns to decide which lines to include.
* Avoid using the GENDER and CHARACTER columns directly in the features.
### Improve Vectorization Method:
* Utilize matrix transformation techniques such as TF-IDF to enhance the create_document_matrix_from_corpus function.
* Implement the TF-IDF transformation and compare its performance with the existing DictVectorizer.
* Initialize transformers appropriately based on the fitting and transformation stages.
* Evaluate the impact of the technique on the mean rank.
### Run on Final Test Data:
* Test the best system developed using all of the training data (400 lines per character maximum) on the test file (40 lines per character maximum).
* Ensure that the final testing is consistent with the training/testing regime developed.
* Report the mean rank and accuracy of document selection on the test data.

### Conclusion:
This project aimed to improve the vector representations of character documents from the Eastenders script data by implementing various techniques such as pre-processing enhancements, linguistic feature extraction, analyzing similarity results, incorporating dialogue context and scene features, improving vectorization methods, and conducting final testing. The objective was to maximize the distinction between character documents and improve the performance of the information retrieval classification method. The results and improvements made contribute to enhancing the accuracy and effectiveness of character document similarity assessment in the Eastenders script data.

## 🔖 Project structure

```
Project_folder/
|- bin/          # contains scripts and main files that should be run
|- config/       # config files
|- notebooks/    # notebooks for EDA, exploration, predictions and results and conclusions
|- src/          # source code - contains functions
|- tests/        # Test files should mirror the src folder
|- Makefile      # automatize taks through make utility
```

## 🏁 Getting Started <a name = "getting_started"></a>
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites
Setup your environement and install project dependencies
```
conda create -n my_project python=3.10
source activate my_project

python -m pip install pip-tools
pip-compile --output-file requirements.txt requirements.in requirements_dev.in
python -m pip install -r requirements.txt
```

### Installing

## 🔧 Running the tests
Tests are implemented in ./tests, you need to run the following command to run them.
```
make tests
```


