# Character Finder

## Prerequisites 
* Make sure you have the prerequisites for the Object Detection API installed. The directions for installations can be found [here](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/installation.md)
* Download the [training](https://www.dropbox.com/s/linj0vexpsfgju3/characters.zip?dl=1) and [evaluation](https://www.dropbox.com/s/057f3o1zsyd8k26/eval_images.zip?dl=1) images in this directory

Run the  following commands 
```
 unzip characters.zip
 unzip eval_images.zip
```

## Generating record files
* Run the following command 
` python change_csv.py `
This will change the filneame attribute in csv to point to the correct directory of the images located

