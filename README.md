# deep-learning-challenge
## Overview
This analysis is aimed to create and train a deep-learning model that can help Alphabet Soup select the applicants with the best chance of success in their venture. The libraries that are mainly used are Sklearn, Pandas, and Tensorflow. The database that are provided can be find and download from
"https://static.bc-edx.com/data/dl-1-2/m21/lms/starter/charity_data.csv". In the analysis, the model are optimized multiple times. Different versions of the model are saved as HDF5 files.
## Results
![Data_Overview](https://github.com/henrychan990805/deep-learning-challenge/blob/c00672fa5de465ac01558c9fce85faa2cd84b804/ScreenShots/Data_Overview.png)
### Data Processing
* Targets of the model <br>
  "IS_SUCCESSFUL" is the target of this model since the model aims to predict the success of venture. (0 represents failure, and 1 represents success.) <br><br>
* Features of the model <br>
  "APPLICATION_TYPE": Alphabet Soup application type <br>
  "AFFILIATION": Affiliated sector of industry <br>
  "CLASSIFICATION": Government organization classification <br>
  "USE_CASE": Use case for funding <br>
  "Organization": Organization type <br>
  "STATUS": Active Status <br>
  "INCOME_AMT": Income classification <br>
  "SPECIAL_CONSIDERATIONS": Special Considerations for application <br>
  "ASK_AMT": Funding amount requested <br><br>
* Dropped Data <br>
  "EIN" and "NAME": These data are identification data. They are neither targets or features. Therefore, they are removed and not used in our model.

### Compiling, Training, and Evaluating the Model
#### AlphabetSoupChairy
![Model Summary1](https://github.com/henrychan990805/deep-learning-challenge/blob/c138612c6bbfd55211a9fdf9c1153e73481718fe/ScreenShots/Summary/AlphabetSoupChairy_summary.png)
* Number of Hidden Layers: 2
  * First Layer
    * Number of Neurons: 8
    * Activation Functin: Relu
  * Second Layer:
    * Number of Neurons: 5
    * Activation Function: Relu
  * Output Layer:
    * Number of Neurons: 1
    * Activation Function: Sigmoid
  <br><br>
* Preformance: <br>
![Model Summary](https://github.com/henrychan990805/deep-learning-challenge/blob/1ec65a342f1b3f047f048a48bded5e9017b2f041/ScreenShots/Evaluation/AlphabetSoupChairy_evaluation.png)
* The model does not achieve the model performance. For the optimization, More nodes are added in each hidden layers, and the number of epochs are also increase from 100 to 200.
<br><br>
#### AlphabetSoupChairy_Optimization(1)
![Model Summary](https://github.com/henrychan990805/deep-learning-challenge/blob/bf73acd466b205ab979b61475f872a0600d2b27c/ScreenShots/Summary/AlphabetSoupChairy_Optimization(1)_summary.png)
* Number of Hidden Layers: 2
  * First Layer
    * Number of Neurons: 40
    * Activation Functin: Relu
  * Second Layer:
    * Number of Neurons: 30
    * Activation Function: Relu
  * Output Layer:
    * Number of Neurons: 1
    * Activation Function: Sigmoid
<br><br>
* Preformance: <br>
![Model Summary](https://github.com/henrychan990805/deep-learning-challenge/blob/bf73acd466b205ab979b61475f872a0600d2b27c/ScreenShots/Evaluation/AlphabetSoupChairy_Optimization(1)_evaluation.png)
* The model does not achieve the model performance. For the optimization, one more hidden layers are added.
<br><br>
#### AlphabetSoupChairy_Optimization(2)
![Model Summary](https://github.com/henrychan990805/deep-learning-challenge/blob/bf73acd466b205ab979b61475f872a0600d2b27c/ScreenShots/Summary/AlphabetSoupChairy_Optimization(2)_summary.png)
* Number of Hidden Layers: 3
  * First Layer
    * Number of Neurons: 8
    * Activation Functin: Relu
  * Second Layer:
    * Number of Neurons: 5
    * Activation Function: Relu
  * Third Layer:
    * Number of neurons: 5
    * Activation Function: Relu
  * Output Layer:
    * Number of Neurons: 1
    * Activation Function: Sigmoid
<br><br>
* Preformance: <br>
![Model Summary](https://github.com/henrychan990805/deep-learning-challenge/blob/bf73acd466b205ab979b61475f872a0600d2b27c/ScreenShots/Evaluation/AlphabetSoupChairy_Optimization(2)_evaluation.png)
* The model does not achieve the model performance. For the optimization, two more hidden layers are added. The number of neurons are also added in each layer. Changed activation function to relu6.
<br><br>
#### AlphabetSoupChairy_Optimization(3)
![Model Summary](https://github.com/henrychan990805/deep-learning-challenge/blob/bf73acd466b205ab979b61475f872a0600d2b27c/ScreenShots/Summary/AlphabetSoupChairy_Optimization(3)_summary.png)
* Number of Hidden Layers: 5
  * First Layer
    * Number of Neurons: 6
    * Activation Functin: Relu
  * Second Layer: 5 neurons
    * Number of Neurons: 10
    * Activation Function: Relu
  * Third Layer:
    * Number of neurons: 10
    * Activation Function: Relu
  * Forth Layer:
    * Number of neurons: 10
    * Activation Function: Relu
  * Fifth Layer:
    * Number of neurons: 10
    * Activation Function: Relu
  * Output Layer:
    * Number of Neurons: 1
    * Activation Function: Sigmoid
<br><br>
* Preformance: <br>
![Model Summary](https://github.com/henrychan990805/deep-learning-challenge/blob/bf73acd466b205ab979b61475f872a0600d2b27c/ScreenShots/Evaluation/AlphabetSoupChairy_Optimization(3)_evaluation.png)
* The model does not achieve the model performance. For the optimization, some features ("STATUS", "APPLICATION_TYPE") are dropped. Acctivation Function changed to leaky relu. Added more nodes to hidden layers.
<br><br>
#### AlphabetSoupChairy_Optimization(4)
![Model Summary](https://github.com/henrychan990805/deep-learning-challenge/blob/bf73acd466b205ab979b61475f872a0600d2b27c/ScreenShots/Summary/AlphabetSoupChairy_Optimization(4)_summary.png)
* Number of Hidden Layers: 5
  * First Layer
    * Number of Neurons: 80
    * Activation Functin: Relu
  * Second Layer: 5 neurons
    * Number of Neurons: 30
    * Activation Function: Relu
  * Third Layer:
    * Number of neurons: 10
    * Activation Function: Relu
  * Forth Layer:
    * Number of neurons: 10
    * Activation Function: Relu
  * Fifth Layer:
    * Number of neurons: 10
    * Activation Function: Relu
  * Output Layer:
    * Number of Neurons: 1
    * Activation Function: Sigmoid
<br><br>
* Preformance: <br>
![Model Summary](https://github.com/henrychan990805/deep-learning-challenge/blob/bf73acd466b205ab979b61475f872a0600d2b27c/ScreenShots/Evaluation/AlphabetSoupChairy_Optimization(4)_evaluation.png)
* The model does not achieve the model performance. For the optimization, two more hidden layers are added. The number of neurons are also added in each layer. Epochs increase from 100 to 300. Activation function are changed to leaky_relu rather than relu.
<br><br>
#### AlphabetSoupChairy_Optimization(5)
![Model Summary](https://github.com/henrychan990805/deep-learning-challenge/blob/bf73acd466b205ab979b61475f872a0600d2b27c/ScreenShots/Summary/AlphabetSoupChairy_Optimization(5)_summary.png)
* Number of Hidden Layers: 7
  * First Layer
    * Number of Neurons: 53
    * Activation Functin: Leaky Relu
  * Second Layer: 5 neurons
    * Number of Neurons: 30
    * Activation Function: Leaky Relu
  * Third Layer:
    * Number of neurons: 20
    * Activation Function: Leaky Relu
  * Forth Layer:
    * Number of neurons: 15
    * Activation Function: Leaky Relu
  * Fifth Layer:
    * Number of neurons: 10
    * Activation Function: Leaky Relu
  * Sixth Layer:
    * Number of neurons: 5
    * Activation Function: Leaky Relu
  * Seventh Layer:
    * Number of neurons: 2
    * Activation Function: Leaky Relu
  * Output Layer:
    * Number of Neurons: 1
    * Activation Function: Sigmoid
<br><br>
* Preformance: <br>
![Model Summary](https://github.com/henrychan990805/deep-learning-challenge/blob/bf73acd466b205ab979b61475f872a0600d2b27c/ScreenShots/Evaluation/AlphabetSoupChairy_Optimization(5)_evaluation.png)
* The model does not achieve the model performance. For the optimization, model structure is changed.
<br><br>
#### AlphabetSoupChairy_Optimization(6)
![Model Summary](https://github.com/henrychan990805/deep-learning-challenge/blob/bf73acd466b205ab979b61475f872a0600d2b27c/ScreenShots/Summary/AlphabetSoupChairy_Optimization(6)_summary.png)
* Number of Hidden Layers: 7
  * First Layer
    * Number of Neurons: 10
    * Activation Functin: Leaky Relu
  * Second Layer: 5 neurons
    * Number of Neurons: 20
    * Activation Function: Leaky Relu
  * Third Layer:
    * Number of neurons: 50
    * Activation Function: Leaky Relu
  * Forth Layer:
    * Number of neurons: 30
    * Activation Function: Leaky Relu
  * Fifth Layer:
    * Number of neurons: 20
    * Activation Function: Leaky Relu
  * Sixth Layer:
    * Number of neurons: 10
    * Activation Function: Leaky Relu
  * Seventh Layer:
    * Number of neurons: 5
    * Activation Function: Leaky Relu
  * Output Layer:
    * Number of Neurons: 1
    * Activation Function: Sigmoid
<br><br>
* Preformance: <br>
![Model Summary](https://github.com/henrychan990805/deep-learning-challenge/blob/bf73acd466b205ab979b61475f872a0600d2b27c/ScreenShots/Evaluation/AlphabetSoupChairy_Optimization(6)_evaluation.png)
* The model does not achieve the model performance.
<br><br>
  
