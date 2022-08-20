# Human_activities_cnn_lstm

**DATA DESCRIPTION AND FEATURES**

 I will visualize the data along with labels to get an idea about what we will be dealing with. We will be using the [UCF50 - Action Recognition Dataset](https://www.crcv.ucf.edu/data/UCF50.php), consisting of realistic videos taken from youtube which differentiates this data set from most of the other available action recognition data sets as they are not realistic and are staged by actors. The Dataset contains:

*   **`50`** Action Categories

*   **`25`** Groups of Videos per Action Category

*   **`133`** Average Videos per Action Category

*   **`199`** Average Number of Frames per Video

*   **`320`** Average Frames Width per Video

*   **`240`** Average Frames Height per Video

*   **`26`** Average Frames Per Seconds per Video

**BREIF PREPROCESSING DETAILS**

I will read the video files from the dataset and resize the frames of the videos to a fixed width and height, to reduce the computations and normalized the data to range [0-1] by dividing the pixel values with 255, which makes convergence faster while training the network.
Instead of processing every frame in the video i will be taking 1/8 frames on an average from the videos and vectorize them in the form of numpy array and 
one hot encoding for the labels will be suffice for the task and thus categorical_cross_entropy would be the best.


**HYPER_PARAMETERS TUNING**

Hyper parameters will be tuned as required ,lr_decay ,beta constants for the sgd with momentum, optimisers loss,layers , neurons in a layer.

**BREIF ABOUT THE MODEL**

A CNN-LSTM model is used where the inputs  from the  cnn is used in a time feed forward manner and the forward propagation through time is learnt by the LStm and is converted into a sequence of the defined labels.

**FUTURE SCOPE**

Application of GANs for production of the further frames  or prediction of the next actions will be the future scope of the project.


**Completeness - LRCN yet to implement.**
