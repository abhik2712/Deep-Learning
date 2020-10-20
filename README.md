# Deep-Learning
Various Deep Learning Applications using Tensorflow and Keras API

## 1.Convolution Neural Networks(CNN)

### Dataset 1: Fashion MNIST

#### About the Dataset:

- We'll need TensorFlow Datasets, an API that simplifies downloading and accessing datasets, and provides several sample datasets to work with.
- The Fashion MNIST dataset, which contains 70,000 grayscale images in 10 categories. The images show individual articles of clothing at low resolution (28  ×  28 pixels), as seen here

<img width="500" alt="Screenshot 2020-10-20 at 7 30 17 PM" src="https://user-images.githubusercontent.com/31176045/96596906-da6b5500-130a-11eb-8506-6d7197f45639.png">


- The labels are an array of integers, in the range [0, 9]. These correspond to the class of clothing the image represents:

<img width="500" alt="Screenshot 2020-10-20 at 7 38 04 PM" src="https://user-images.githubusercontent.com/31176045/96597783-da1f8980-130b-11eb-840d-821fec7adb39.png">

#### Applying Convolutional NN Model

- The details of the model is shown below:
  <img width="1000" alt="Screenshot 2020-10-20 at 7 40 43 PM" src="https://user-images.githubusercontent.com/31176045/96598268-53b77780-130c-11eb-9547-109ba56067cc.png">
  
  
#### Experiments Performed and their outcome:

- **Consider single hidden layer**

| Dense Layers  | Train Accuracy | Test Accuracy |
| ------------- | -------------- | ------------- |
|    512        |    86.75       |     86.18     |
|    10         |    79.99       |     85.02     |

- **Consider single hidden layer and without normalising images**

| Dense Layers  | Train Accuracy | Test Accuracy |
| ------------- | -------------- | ------------- |
|    128        |    85.98       |     87.51     |

- **Consider two hidden layer**

| Dense Layers  | Train Accuracy | Test Accuracy |
| ------------- | -------------- | ------------- |
|    128        |    93.30       |     89.74     |

- The above case with two hidden layers is an example of **overfitting**.


### Dataset 2.1: Dogs and Cats

#### Goal : Classify whether image is of cat(label 1) or dog(label 0)

#### About the dataset:

- The dataset used is a filtered version of Dogs vs. Cats dataset from Kaggle (ultimately, this dataset is provided by Microsoft Research).
- In this project, we use the class **tf.keras.preprocessing.image.ImageDataGenerator** which will read data from disk. We therefore need to directly download Dogs vs. Cats from a URL and unzip it to the runtime environment.

#### Challenges and Solutions

- This dataset consists of images of different size but our model requires fixed size input, thus we resize our image to 150x150 pixel resolution.
- This dataset consists of colored images thus in our model we provide input_shape=(150,150,**3**) where the 3 refers to **RGB** channel of the color image.



