# EEG classification over time with temporal fetures
## Dataset
In this project we have an EEG dataset which contains signals from 126 electrodes(channels) for two tasks, seeing human face and piano pictures. the dataset has 3 dimension, num_trials,num_channels and time (90,126,3500).The sampling frequency is 500Hz,which result in 7 seconds records for each trial. The dataset for both tasks are seperated and in *.mat* format. 
## Feature Extraction
12 temporal features are obtained from time series of each channel. These features are as below: 
1. mean
2. standard deviation
3. peak to peak 
4. variance
5. maximum
6. minimum
7. arg maximum
8. arg minimum
9. root mean square
10. sum of absolute of signal's first differential
11. skewness
12. kurtosis 
## Classification
Each signals with 3500 size are devided into 100 equal segments with 5% overlap. Originally we have 90 trials each contains 126 channels and each channel contains a time series of 3500 samples. First of all we segment each time series into 100 equal segments, which results in  90×100=9000 trials with 126 channels with time series of 40 samples. Secondly, for each of this segmented trials, we extract those 12 features for each channels. So, we have 12×126=1512 features for each of the 9000 segmented trials.
To be more clear, we have 100 different datasets(each of them relates to an specificic time interval), each of them contains 90 segmented trials with 1512 features. For each of these datasets we train a KNN classifier to classify these two tasks. finally we analyzed the accuracy of each of this classifiers, in order to find the best time interval in which the accuracy of the classification is maximum.  
