# Deep-Learning-Challenge

**Introduction and Purpose**

The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

- **EIN and NAME**: Identification columns
- **APPLICATION_TYPE**: Alphabet Soup application type
- **AFFILIATION**: Affiliated sector of industry
- **CLASSIFICATION**: Government organization classification
- **USE_CASE**: Use case for funding
- **ORGANIZATION**: Organization type
- **STATUS**: Active status
- **INCOME_AMT**: Income classification
- **SPECIAL_CONSIDERATIONS**: Special considerations for application
- **ASK_AMT**: Funding amount requested
- **IS_SUCCESSFUL**: Was the money used effectively

**1. Preprocessing**

The process began with importing the dependencies with Pandas, sklearn and tensorflow. The CSV file was imported and read through a link instead of a traditional CSV file read. The next steps were to write a code to drop the non-beneficial ID columns of "EIN" and "NAME" with the written code below:

![image](https://github.com/adelao747/Deep-Learning-Challenge/assets/113153195/51690f8a-8726-4d65-9a58-0a4e57d9446f)

After the non-beneficial columns were deleted, a binning method was used to create a list of application and classification types, which the variable names of "application_types_to_replace" and "classifications_to_replace" were used to then display the list of each application and classification:

![image](https://github.com/adelao747/Deep-Learning-Challenge/assets/113153195/6d154e48-16db-45ae-a886-d756ab863de8)

![image](https://github.com/adelao747/Deep-Learning-Challenge/assets/113153195/6eb84829-13b5-4503-90df-f7e8bf130f61)

Splitting the preprocessed data was done used the "pd.get_dummies" code to then create a training and testing dataset. The codes of: X_train, X_test, y_train and y_test were used to complete this section of the notebook.

**2. Compile, Train and Evaluate the Model**

Defining, compiling and training the models were then complete the next section. Defining the first, second hidden layer, and the output layer were completed to display the layer type, output shape, and parameter numbers. 

![image](https://github.com/adelao747/Deep-Learning-Challenge/assets/113153195/1b745927-381b-478d-bb2e-ad9d0f88b882)

Compiling the model with "binary_crossentrophy", "adam" with "accuracy" for metrics was used for this section, while "fit" was used to create the training model with 100 epochs. An example image is included below:

![image](https://github.com/adelao747/Deep-Learning-Challenge/assets/113153195/e31212c5-d21c-4714-b629-ca0914382356)

**Summary**

The defining model showed the layer type, output shape and parameter numbers. The totals came to be 5,981 total parameters, 5,981 trainable parameters and 0 non-trainable parameters. The training model has displayed 100 epochs with a batch size of 804. Each epoch had a loss and accuracy of varying results. While creating an evaluation of the model during the testing section, we can see a loss of 0.5571 with an accuracy of 0.7306. 
