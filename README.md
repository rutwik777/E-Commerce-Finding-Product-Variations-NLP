# Assesment 1  

## E-Commerce-Finding-Product-Variations-NLP
Code for a function named FindAlternateGroups() that takes store domain as the parameter and returns links of products that are alternates of each other in an array. Detailing approaches used in solving the problem.
  
    
Approach 1: (FILE BoW_method_cc_v4.ipynb) In this approach we use traditional NLP approaches of Bag of Words to encode the titles and then creates a dictornary corpus for individual website and uses this to convert titles into vectors and finally using cosine similarity to find alternate products.  
  
Approach 2: (FILE BERT_method_cc_v2.ipynb) In this approach we use BERT encodings to convert the tiles strings into 384 dimensional dense vector space. Then we pass individual titles and check for semantic similarity using cosine similarity to find alternate products.
  
Approach 3: Additional method, without the use of AI would be to perform string operations:  
1. Take all the tile strings -> Make a list of all colors and patterns -> Delete these words from the original strings -> Perform cosine similairty
2. Take strings -> Find the longest substring that match the words
  
Approach 4: If we have tens of thousands of products, is to use all the rows to make a deep learning model with product parameters(Name, Price, Description, Manufacturer, etc) as inputs to caluculate semantic similarity as output.
  
# Assesment 2  

## E-Commerce-Finding-Differences-in-Product-Variations  
Code for a function named FindKeyDifference() that takes a JSON object containing arrays of similar product links as the parameter and returns a JSON object that outlines the key difference between each product within the groups. Detailing approach used in solving the problem.  

Approach 1: (FILE Key_Difference_method_cc_v7.ipynb) In this approach simple string manipulations followed by a dedicated function to find difference words is integrated to provide output as per question.  
Note:- Due to 430 error for muliple server ping to extract data for each product, I made a work around for this i set the range value to 10 for simplified testing. You can edit the parapmeter at line 67 of cell 2 in notebook. code is as follows  
#Main logic to store and manuplate JSON and Differences
    for i in range(10):
