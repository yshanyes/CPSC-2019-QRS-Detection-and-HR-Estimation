# Solution&Code for the CPSC 2019, rank 4/5 on the HR/QRS track, respectively.

## Solution

The QRS complex is the most prominent feature and it can be used to obtain additional useful clinical information from electrocardiogram (ECG) signals, therefore, QRS complex detection is critical for ECG signal analysis. Accurate QRS location keeps a challenging task. in noisy ECG signals. The rule-based QRS detection methods largely depend on hand-crafted manual features and parameters, the fixed features and parameters of which require difficult offline tuning for adapting to new scenarios.
In this study, based on 1-D convolutional neural network (CNN) and U-Net-like architecture, an accurate QRS complex detection method is proposed. Inspired by previous work, the residual block is introduced as backbone of encoder in 1-D U-Net-like model. In addition, multi-level deep supervision is designed to ease the potential gradient vanishing problem and to improve the performance when only restricted set of labeled data are available.
The proposed method has been validated against the 2nd china physiological signal challenge data set, obtaining a QRS accuracy score of 0.9004, HR accuracy score of 0.9421 on the hidden test set, respectively. Experimental results show that the proposed method acquires competitive accuracy and comparable generalization performance.

## Contents
This code uses two main scripts to train the model and test the data:

* `train_cv.py` is used to train model with five folds cross validation. 
* `cpsc2019_score.py` is used to test model through feeding test data into data folder. 

This is only part of the code, and the entire solution code will be coming soon.

## Use

You can run this code by installing the requirements and running

- training

    python train_cv.py 

- prediction

    python cpsc2019_score.py 

The [CPSC 2019 webpage](http://2019.icbeb.org/Challenge.html) provides a training database with data files and a description of the contents and structure of these files.

## Submission

The CPSC 2019 webpage provides the sample python entry.

## Details

See the [CPSC 2019 webpage](http://2019.icbeb.org/Challenge.html) for more details, including instructions for the challenge data and challenge score.


