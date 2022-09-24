

There are 4 files for Torch, Torch+AE, Keras, and Keras+AE models. (Torch = PyTorch, AE = AutoEncoder)<br>
The most complicated file which is Keras+AE will be explained here and the rest can be understood easily. <br>
<br><br>
1- Import packages and see if the computing environment is compatible using Cuda or GPU<br>
2- Recreate the classical approach for photometric modeling to create results to be compared with the ANN results at the end <br>
3- Data loading and cleaning loads "fits" data and sets limits to filter the data we can use<br>
4- Data normalization rescales data between 0 and 1 <br>
5- Data preparation sets data in features and labels<br>
6- Print out file IDs to see how many "fits" files we have<br>
7- Split data randomly into training (90%) and validation (10%). Choose 1000 (or less for small images) random pixels from each image <br>
8- Calculate classical model (ROLO) MSE <br>
9- Print training and validation data row counts<br>
10- Create Autoencoder setting the number of features we want to generate, the number of hidden layers, the number of neurons in each layer, etc<br>
11- Check to see how many new features were created and how many are there in total after merging with the original ones <br>
12- Check the correlation between features and remove the highly correlated ones<br>
13- Use PCA to choose the best 3 informative features to be used in the ANN<br>
14- Set up the neural network using Keras. the activation function is relu and only in the output use sigmoid<br>
15- Check the MSE and compare it to the classical ROLO model MSE to see the percentage of improvement<br>
<br>
Please check the screenrecord video to see the code demonstration. 
<br>
I have added some data files in reduced_phocubes folder so that you can run and test the codes yourself too. <br>
