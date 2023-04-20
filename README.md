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
