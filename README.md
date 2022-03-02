# Object_Detection_First-setup

Link files :
============

https://pastebin.com/YDgbqzTx - Reference file

https://github.com/tensorflow/models/tree/v1.13.0  ###  Download Repo
 
http://download.tensorflow.org/models/object_detection/faster_rcnn_inception_v2_coco_2018_01_28.tar.gz ###  Download Repo
 
 
https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf1_detection_zoo.md ### Model Zoo Link , Reference file
 
https://drive.google.com/file/d/12F5oGAuQg7qBM_267TCMt_rlorV-M7gf/view?usp=sharing ### Dataset & utils Download



Steps :
============

# Create a folder "tfod" and unzip all files and rename them properly
cd C:\Users\Sasmitabhoi\Documents\DL_CV_NLP\Object_Detection\tfod

# Creating virtual env using conda
conda create -n your_env_name python=3.6.10 -y
conda create -n tfod python=3.6.10 -y
 
conda activate your_env_name
conda activate tfod
 
# pypi 
pip install pillow lxml Cython contextlib2 jupyter matplotlib pandas opencv-python tensorflow==1.14.0

# From Research Folder
cd C:\Users\Sasmitabhoi\Documents\DL_CV_NLP\Object_Detection\tfod\models\research
 
python setup.py install #install object detection

# conda package manager
conda install -c anaconda protobuf -y

# windows ( I am telling , please use proto and convert all protos to python )

protoc object_detection/protos/*.proto --python_out=.

# Check  manually if .protos files are converted to .py files or not
cd object_detection\protos
dir

## Open Jupyter notebook
cd ..

jupyter notebook object_detection_tutorial.ipynb  ( Currently you are in "tfod\models\research\object_detection" location ) 

	# Jupyter notebook will open , insert a code cell and try "!conda env list"
 
	# Run other cells
 
	# You shall get halt in below code .
 
			from utils import label_map_util
			from utils import visualization_utils as vis_util
			
	# File -> Close & Halt
 
	# Copy "object_detection_tutorial.ipynb" from "tfod\models\research\object_detection" folder to "tfod\models\research" folder .
 
cd ..

jupyter notebook ( Currently you are in "tfod\models\research" location ) 	

	# Change the code as below .
 
			from object_detection.utils import label_map_util
			from object_detection.utils import visualization_utils as vis_util		
			
## Refer file from Location  : 

C:\Users\Sasmitabhoi\Documents\DL_CV_NLP\Object_Detection\tfod\models\research\object_detection\data\mscoco_label_map.pbtxt			

