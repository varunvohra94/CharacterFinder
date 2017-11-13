# Character Finder

## Prerequisites 
* Make sure you have the prerequisites for the Object Detection API installed. The directions for installations can be found [here](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/installation.md)
* Download the [training](https://www.dropbox.com/s/linj0vexpsfgju3/characters.zip?dl=1) and [evaluation](https://www.dropbox.com/s/057f3o1zsyd8k26/eval_images.zip?dl=1) images in this directory

Run the  following commands 
```
 unzip characters.zip
 unzip eval_images.zip
```
**Make sure the images are inside this folder** 

## Generating record files
* Run the following command 
` python change_csv.py `.
This will change the filneame attribute in csv to point to the correct location of the images located.
* After the csv points to the correct location, we can generate the record files
 ``` bash
# Generate training record
python --csv_input train.csv --output_path train.record --label_map_path characters_label_map.pbtext 
``` 
``` bash
# Generate evaluation record
python --csv_input eval.csv --output_path eval.record --label_map_path characters_label_map.pbtext 
```

* ** This only creates training and evaluation records for one character - Santa. If you want to train on more characters, follow these [instructions](#abcd) first **

## Training
For training you need to construct an object-detection training pipeline. 
* You can use any of the config files present in object\_detection/samples/configs as basis
* 

<a name="abcd"></a>
