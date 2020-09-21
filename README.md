# Solution&Code for the CPSC 2019, rank 4/5 on the HR/QRS track, respectively.

## Solution

The QRS complex is the most prominent feature and it can be used to obtain additional useful clinical information from electrocardiogram (ECG) signals, therefore, QRS complex detection is critical for ECG signal analysis. Accurate QRS location keeps a challenging task. in noisy ECG signals. The rule-based QRS detection methods largely depend on hand-crafted manual features and parameters, the fixed features and parameters of which require difficult offline tuning for adapting to new scenarios.
In this study, based on 1-D convolutional neural network (CNN) and U-Net-like architecture, an accurate QRS complex detection method is proposed. Inspired by previous work, the residual block is introduced as backbone of encoder in 1-D U-Net-like model. In addition, multi-level deep supervision is designed to ease the potential gradient vanishing problem and to improve the performance when only restricted set of labeled data are available.
The proposed method has been validated against the 2nd china physiological signal challenge data set, obtaining a QRS accuracy score of 0.9004, HR accuracy score of 0.9421 on the hidden test set, respectively. Experimental results show that the proposed method acquires competitive accuracy and comparable generalization performance.

## Contents
This code uses two main scripts to train the model and test the data:

* `train_cv.py` is used to train model . 
* `cpsc2019_score.py` is used to test model . 

Check the code in these files for the input and output formats for the `train_model` and `driver` scripts.

To create and save your model, you should edit `train_12ECG_classifier.py` script. Note that you should not change the input arguments of the `train_12ECG_classifier` function or add output arguments. The needed models and parameters should be saved in a separated file. In the sample code, an additional script, `get_12ECG_features.py`, is used to extract hand-crafted features. 

To run your classifier, you should edit the `run_12ECG_classifier.py` script, which takes a single recording as input and outputs the predicted classes and probabilities. Please, keep the formats of both outputs as they are shown in the example. You should not change the inputs and outputs of the `run_12ECG_classifier` function.

## Use

You can run this code by installing the requirements and running

    python train_cv.py 

The [CPSC 2019 webpage](http://2019.icbeb.org/Challenge.html) provides a training database with data files and a description of the contents and structure of these files.

## Submission

The `driver.py`, `get_12ECG_score.py`, and `get_12ECG_features.py` scripts must be in the root path of your repository. If they are inside a folder, then the submission will be unsuccessful.

## Details

See the [CPSC 2019 webpage](http://2019.icbeb.org/Challenge.html) for more details, including instructions for the challenge data and challenge score.


