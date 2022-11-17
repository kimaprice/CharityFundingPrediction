# Charity Funding Prediction

## Overview
The nonprofit foundation Alphabet Soup has data points for more than 34,000 organizations that they have donated funding to over the years.  This data has been analyzed in order to create a model to predict if funding will be used succesfully in order to assist them make future funding decisions.

### Results: 

  * Data in file
    * **EIN**—Identification number
    * **NAME**—Identification name
    * **APPLICATION_TYPE**—Alphabet Soup application type
    * **AFFILIATION**—Affiliated sector of industry
    * **CLASSIFICATION**—Government organization classification
    * **USE_CASE**—Use case for funding
    * **ORGANIZATION**—Organization type
    * **STATUS**—Active status
    * **INCOME_AMT**—Income classification
    * **SPECIAL_CONSIDERATIONS**—Special consideration for application
    * **ASK_AMT**—Funding amount requested
    * **IS_SUCCESSFUL**—Was the money used effectively

  * Data Preprocessing
    * Target:  **IS_SUCCESSFUL**—Was the money used effectively
    * Variables:
        * **APPLICATION_TYPE**—Alphabet Soup application type
        * **AFFILIATION**—Affiliated sector of industry
        * **CLASSIFICATION**—Government organization classification
        * **USE_CASE**—Use case for funding
        * **ORGANIZATION**—Organization type
        * **STATUS**—Active status
        * **INCOME_AMT**—Income classification
        * **SPECIAL_CONSIDERATIONS**—Special consideration for application
        * **ASK_AMT**—Funding amount requested
    * Removed Variables (not helpful in analyzing funding success):
        * **EIN**—Identification number
        * **NAME**—Identification name


* Initial Model
    * neurons/params = 16,633, each hidden layer 108 outputs (2.5 times the input)
    * layers = 2 hidden layers
    * activation functions = relu, sigmoid output
    * epochs = 100
    * Accuracy: 0.726064145565033
    
* Optimization Trial 1: Add more Nuerons
    * neurons/params = 22, 576, each hidden layer 129 outputs (3 times the input)
    * layers = 2 hidden layers
    * activation functions = relu, sigmoid output
    * epochs = 100
    * Accuracy: 0.7257142663002014

* Optimization Trial 2: Add more hidden layers
    * neurons/params = 28,405, each hidden layer 108 (2.5 times the input)
    * layers = 3 hidden layers
    * activation functions = relu, sigmoid output
    * epochs = 100
    * Accuracy: 0.7254810333251953

* Optimization Trial 3: Add Epochs
    * neurons/params = 16,633, each hidden layer 108 outputs (2.5 times the input)
    * layers = 2 hidden layers
    * activation functions = relu, sigmoid output
    * epochs = 200
    * Accuracy: 0.7258309125900269

* Optimization Trial 4: Try different activation functions
    * neurons/params = 16,633, each hidden layer 108 outputs (2.5 times the input)
    * layers = 2 hidden layers
    * activation functions = tanh, sigmoid output
    * epochs = 100
    * Accuracy: 0.7261807322502136
    

## Summary
The model's accuracy was never able to get to the target of over 75% despite the 4 trials at optimization.  There may be some benefit running the keras-tuner to to more efficient optimization testing.