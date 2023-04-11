# roads_fields_classification
the purpose of the task is to classify road and field images </br>

the dataset is composed of 45 field images and 108 road images, as we can notice the dataset is tiny for a training a classifier.  </br>

So I decided to use data augmentation in order to be able to train a classifier on those images and for the model I used a pretrained ResNet 18 (I tested other models but I get better results using this model). </br> 

the model is composed from resnet + two fully connected layers which are trained on the new task, the last layer is one neuron layer with sigmoid as transfer function( I also tested softmax but had better results using sigmoid).   </br>  

also for preventing overfitting I used early stopping: if the val loss does not decrease afer X epochs, the training is stopped and we use the weights with the best validation loss.   </br>

for test, the model was able to classify correctly all the images in the given dataset + some images from the internet.</br>

more details in the notebook. </br>

the link to the weights file which will be used for test [here](https://drive.google.com/file/d/18OcCE6fMlK1uUUA31Hjt-H1woBwlRzLD/view?usp=sharing)
