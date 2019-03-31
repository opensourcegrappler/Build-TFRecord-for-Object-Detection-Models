# Build a Tenforflow record file for object detection models

## Labelling Data

Label your images using a tool such as the
[labelImg](https://github.com/tzutalin/labelImg) tool.

### Dependencies

Install the Tensorflow models repository inside the top level of this
project. (This project builds on example code from this Tensorflow
Models project, Thanks!)

* [TensorFlow Models](https://github.com/tensorflow/models)
- Follow the installation instructions for that project in the object
detection directory.

## Use

* Update the '''LABEL_DICT''' with the class labels for your project.
* Build your tfrecord file with:

    python make_tfrecord.py --data_path=./path/to/data --output_path=mytfrecord.record

*Note: The data_path should contain both the images and the xml files
 with the bounding box information. Only bounding box type labelling
 is supported.*