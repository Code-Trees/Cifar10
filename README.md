# Cifar10

Here we have Cifar 10 data set .
Objective
To start witth i am trying to Build a model with Less parameters possible and can get max accuracy.

I have already built a  frame work what i can use to run  my model and tune parameters.

The Module looks like this:

Strixbee/model:
	cifar10_model1.py
	cifar10_model_scrap.py
	custom_layer.py

Strixbee/utils:
	data_iter.py
	data_transforms.py
	gpu.py
	normalize_utils.py
	optimizer_utils.py
	plots.py
	train_test.py

Strixbee/
	main.py
	Cifar10_resnet_19th.ipynb
	LICENSE
	Pytorch-package-hierarchy.jpg
	README.md


Level1:

Cifar10_Model1.ipynb

Thought Processes:

1> To make the architecture ready first(A skeleton).
2> Basic Normalization.
3> No droupout.
4> SGD and ReduceLRonplateau

Observation:
1> In 50 epochs max trainning accuracy was  97.37 % and max testing accuracy was 78. %. Till 5 epochs Train and test model was fine. Later it started overfitting and gap between train and test started increasing.

2> Training curve is looking smooth. But pushing forward it might reach a 100 % accuracy. After that we might not be able to push the model to test accuracy.

3> We Reached 77+ test accuracy in 7 th epoch . It might have get stucked in minima or there might not be good learning for model or the data in test is tough / Not a correct representation of Train. Can be enything 

4> Model is using Total params: 83,368 . Trainable params: 83,368

Target:
5> Let's make  the model lighter and make it more learnable by removing MaxPool with 3x3 with stride of 2.It might increase model parameters. But can lean more pattern.


Level2:

Cifar10_Model2.ipynb

Observation:
1> In 50 epochs max trainning accuracy was  98.50 % and max testing accuracy was 78.78 %. Till 6 epochs Train and test model was fine. Later it started overfitting and gap between train and test started increasing.

3> We Reached 77+ test accuracy in 12 th epoch . It might have get stucked in minima or there might not be good learning for model or the data in test is tough / Not a correct representation of Train. Can be enything 

4> Model is using heavy parameters.

Target:
1> Let's add regularization to generalize the model. 
Let's add Droupout, Cutout, etc..


Level3:

Cifar10_Model3.ipynb