# Image Processing – Comparison of APNet (original CNN architecture) with some classic and modern CNN architectures
#### Abstract—This paper discusses our attempt at creating a new CNN architecture for the purpose of image processing, and comparing its performance with classic and modern architectures on different datasets such as MNIST, Fashion-MNIST and CIFAR100. 
#### Keywords—CNN, image processing, principal component analysis, convolution, pooling, APNet
## I.	Introduction
In this work, we have carefully studied and implemented some classic and modern network architectures in order to understand their working as well as motivation. In our observation, the classic models tend to train fast and keep a relatively simple pipeline. The general idea was to increase layers, or “go deeper” in order to achieve better performance. Modern CNN algorithms take a different approach. They involve using one of two approaches. One is the inclusion of residual layers to solve the degradation problem that arises from the increase in the depth of the neural network. The other involves aggregating the outcomes of parallelly performing convolutions at different scales. We attempt to create an architecture that derives from the best characteristics of both schools of thought. Our original architecture implements the modern ideology but at a smaller scale hence retaining the simplicity and speed of the classic models.
## II.	Related Work
We have studied and attempted to implement the following CNN architectures for comparison with our own original architecture: LeNet-5, AlexNet, VGG-16, GoogleNet(Inception).
## III.	Exploratory Data Analysis
We have chosen three common datasets: MNIST, Fashion-MNIST and CIFAR-100.
### A.	Data Distribution
The first step in Data Exploration is to load the data, and to examine train-test split in the dataset and dimensions of the data. Then we generate a histogram plot of the data distribution across all the labels in the dataset. Once we make sure that the data is approximately evenly distributed, we can assume that it is good for training since it is a balanced dataset. 
### B.	Data Visualization
Next we proceed to look at the first few training data points to get an idea of what the images in our dataset look like. This is very important considering the task is that of image processing. Visual representations always aid in better understanding of performance and also problems. 
### C.	Principal Component Analysis
A common method for reducing the number of dimensions or features per observation in large datasets is principal component analysis (PCA). Principal component analysis (PCA) is a popular dimension reduction technique for analyzing large datasets containing a high number of dimensions/features per observation.
### D. Data Pre-processing
After performing an exploratory data analysis on each dataset and gaining an understanding of what type of image data we’re dealing with, we now need to pre-process the loaded data.
## IV.	Architectures
The report submitted explains our understanding of the architectures mentioned in Section II. Inspired by the simplicity and speed of training architectures such as LeNet-5, and by the filter concatenation strategy and channel-wise normalization of the Inception architecture, we have experimented with a custom architecture of our own.
## V.	Code Implementation
For a brief overview on the code implementation, please refer to the slide deck. For a more detailed explanation of the code implementation, please refer to the code files attached.
## VI.	Training Cycle
We tune the various hyperparameters for our models and finally run each one on all the datasets. This helps us to compare the performance and the working behind each architecture. We analyze our findings to then create an architecture of our own which we termed APNet. The hyperparameters tuned were: 
* number of epochs
* learning rate
* momentum
## VII.	Results & Analysis
The results of running every architecture on each of the datasets have been tabulated in the report. The training accuracy, validation accuracy, and testing accuracy have been reported for comparison. The graphs shown in the figures represent the model performance during training time. We can see the variation of training/validation losses through the epochs to determine stability and how closely the model is fitting to the optimum function. We can observe the trends in training/validation accuracies to know if our model is on track or if it is overfitting the train data.
## VIII.	Conclusion
Our APNet architecture, along with the LeNet-5, comes very close to the performance of the VGG-16 on the MNIST dataset, overtaking the deeper models like AlexNet and GoogLeNet in this particular experiment. AlexNet, LeNet-5 and APNet are closely tied at second place after VGG’s performance on the Fashion-MNIST dataset. APNet also beats LeNet-5 and VGG-16 on the CIFAR-100 dataset. We can see that APNet takes more epochs than the other architectures to converge on the minima, but given that its training is incredibly fast, this shouldn’t be an issue. The dropout layer helps additionally with APNet not overfitting the training data. The performance of APNet is consistently good on both MNIST and Fashion-MNIST datasets.
## IX.	Future Scope of Work
APNet is a very lightweight architecture, with lots of possibilities to make it deeper. The empirical results already look promising on the MNIST and Fashion-MNIST datasets. There is scope to add more convolution layers. We could implement dimension reduction prior to the concatenation stage. Adding an additional fully-connected layer and splitting the dropout ratio between the two layers could help further increase performance. Future research into its architecture and behavior can lead to a stable deep CNN architecture and possibly eventually outperform some other well-known networks.
