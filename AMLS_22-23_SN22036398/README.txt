Hi, here are the instructions on how to use the code：

The following is an explanation of the project's organisation, the role of each file, the library functions used and the cautions

First a brief overview of the organisation of the code.
Within each code, a main function is included that encapsulates the sub-functions needed to run the code. 
The code in tasks A1, A2 and B1 have the same organisational logic, while the ones in task B2 are slightly different and will be described separately.
In tasks A1, A2 and B1, the library functions are first imported, followed by the pre-processing of the label file and the data file, which is then divided into a training set and a cross-validation set, followed by the construction of the model and the adjustment of parameters, followed by the feeding of the test set into the model and the final prediction results. 
In task B2, the basic principle is the same as above, except that semi-supervised learning is used and a decision tree model is constructed to eliminate the images wearing sunglasses, and the remaining images are then processed as described above.

Secondly, the role of each file will be introduced.
There are two files in the A1 folder, "A1_Logistic_Regression.ipynb" and "A1_Support_Vector_Machine.ipynb". These are the code files for solving task A1 using a logistic regression model and a support vector machine model respectively.
Similarly, there are two files in the A2 folder, "A2_Logistic_Regression.ipynb" and "A2_Support_Vector_Machine.ipynb ipynb". These files correspond to the two codes that solve task A2 using logistic regression and support vector machine algorithms respectively.
There are also two files in the B1 folder, "B1_Convolutional_Neural_Network.ipynb" and "B1_Fully_Connected_Neural_Network. ipynb". They correspond to the code for task B1 using a convolutional neural network and a fully connected neural network respectively.
There are three files in the B2 folder, namely "B2_Convolutional_Neural_Network.ipynb", "B2_Fully_Connected_Neural_Network. ipynb" and 'Semi_supervised_learning_labels.csv'. They correspond to the code for solving task B2 using a convolutional neural network and a fully connected neural network, respectively, as well as the labels for the semi-supervised learning used in the code in order to remove the sunglasses. It is important to note that the "Semi_supervised_learning_labels.csv" file is not an intermediate product generated during the data processing, but only five hundred labels that were manually tagged for semi-supervised learning.
The Datasets folder is empty and "main.ipynb" is the file that calls the code in each of the other folders.

Thirdly, the library functions used in each model will be described.
In Task A1:
File "A1_Logistic_Regression.ipynb" : numpy, pandas,matplotlib.pyplot, skimage.io, skimage.color, time, expit in scipy.special, KFold in sklearn.model_selection, PCA in sklearn.decomposition
File "A1_Support_Vector_Machine.ipynb" : numpy, pandas, matplotlib.pyplot, skimage.io, skimage.color, scipy.special, time, SVC in sklearn.svm, KFold in sklearn.model_selection, PCA in sklearn.decomposition

In Task A2:
File "A2_Logistic_Regression.ipynb": Same as the file "A1_Logistic_Regression.ipynb"
File "A2_Support_Vector_Machine.ipynb ipynb": Same as the file "A1_Support_Vector_Machine.ipynb"

In Task B1:
File "B1_Convolutional_Neural_Network.ipynb" : numpy, cv2, pandas, matplotlib.pyplot, skimage.io, time, Sequential in tensorflow.keras.models, Dense,Dropout,Conv2D,MaxPooling2D,Flatten in tensorflow.keras.layers, TensorBoard,ModelCheckpoint in tensorflow.keras.callbacks, load_model in tensorflow.keras.models
File "B1_Fully_Connected_Neural_Network. ipynb" : Added  PCA in sklearn.decomposition to document "B1_Convolutional_Neural_Network.ipynb"

In Task B2:
File "B2_Convolutional_Neural_Network.ipynb" : Added tree in sklearn, RandomForestClassifier in sklearn.ensemble, KFold in sklearn.model_selection to document "B1_Convolutional_Neural_Network.ipynb"
File "B2_Fully_Connected_Neural_Network. ipynb" :  Added tree in sklearn, RandomForestClassifier in sklearn.ensemble, KFold in sklearn.model_selection to document "B1_Fully_Connected_Neural_Network. ipynb"

Finally, a note of caution is given below.
The code should be run using jupyter notebook.
By running the file main.ipynb you can get a run result like this, "Task**: Accuracy of ** is **". It will tell you the results of all the models used for each task.
Relative paths are used in the code, so there is no need to do anything else to run main.ipynb.
However, if you find that the program does not work, try going to each individual file and replacing the relative path with an absolute path.

By the way, I sincerely thank you for your review and work and wish you and your family a Happy New Year!
Best wishes!