# Classifying Images as Dogs or Cats - Convolutional Neural Network(CNN) 
![image](https://github.com/AdityaMetkar/Cat-Dog-CNN-Classifier/assets/133694021/6958af9b-34c5-49f1-bfd2-00b4a6ff488c)

## Procedure
> For a detailed step-by-step Guide, follow the attached notebook

1. First we load the dataset consisting of images of cats and dogs with installing dependencies.<br>
   Libraries used are  `TensorFlow | OpenCV | Numpy | Matplotlib | Sklearn`.

2. We filter unwanted images with corrupted files or extensions and Preprocess the rest by GrayScaling them.
3. We create Labels for our dataset, in this case `[0:Cats,1:Dogs]`. This can be achieved by
   - Manual iteration over dataset
   - Using inbuilt Keras Pipeline
4. We divide the preprocessed dataset into train, test, validation sets to feed into our Neural Network
5. We generate the CNN Architecture using the `Sequential() API` of Tensorflow.
     <h5>Model Summary</h5>

    <table>
      <tr>
        <th>Layer</th>
        <th>Layer Type</th>
        <th>Output Shape</th>
      </tr>
      <tr>
        <td>1</td>
        <td>Conv2D</td>
        <td>(None, 254, 254, 32)</td>
      </tr>
      <tr>
        <td>2</td>
        <td>MaxPooling2D</td>
        <td>(None, 127, 127, 32)</td>
      </tr>
      <tr>
        <td>3</td>
        <td>Conv2D</td>
        <td>(None, 125, 125, 64)</td>
      </tr>
      <tr>
        <td>4</td>
        <td>MaxPooling2D</td>
        <td>(None, 62, 62, 64)</td>
      </tr>
      <tr>
        <td>5</td>
        <td>Dropout</td>
        <td>(None, 62, 62, 64)</td>
      </tr>
      <tr>
        <td>6</td>
        <td>Conv2D</td>
        <td>(None, 60, 60, 128)</td>
      </tr>
      <tr>
        <td>7</td>
        <td>MaxPooling2D</td>
        <td>(None, 30, 30, 128)</td>
      </tr>
      <tr>
        <td>8</td>
        <td>Flatten</td>
        <td>(None, 115200)</td>
      </tr>
      <tr>
        <td>9</td>
        <td>Dense</td>
        <td>(None, 128)</td>
      </tr>
      <tr>
        <td>10</td>
        <td>Dense</td>
        <td>(None, 64)</td>
      </tr>
      <tr>
        <td>11</td>
        <td>Dense</td>
        <td>(None, 1)</td>
      </tr>
    </table>
6. We train the model on the training data and plot the Performance Metrics.
   
7. Finally we can test the model on new data that the model has never seen to check the performance.
<p>
  <img src="https://github.com/AdityaMetkar/Cat-Dog-CNN-Classifier/assets/133694021/91a921da-8fb1-47d7-ab95-556eaf6d4ece" height='50%' width='40%'>
  <img src="https://github.com/AdityaMetkar/Cat-Dog-CNN-Classifier/assets/133694021/667a1e44-3769-4473-8e16-e88439c9c732" height='50%' width='40%'>
</p>

