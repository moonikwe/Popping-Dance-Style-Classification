# Popping Dance Style Classification Through Inception V3 Feature Extraction and LSTM Classification

This program classifies Popping Dance Styles through using Inception V3 for feature extraction and LSTM for classification, as proposed by Harvey (2017) in his blog, Five Video Classification Methods.
This metholodogy was applied to my own dataset composed of 1310 Popping Dance style videos under 14 classes. 

See this link for the full details of the said blog https://medium.com/@harvitronix/five-video-classification-methods-implemented-in-keras-and-tensorflow-99cad29cc0b5

The whole methodology for method #4 (as adopted in this project) is seen in the same link. Refer to this for his github repository Popping-Dance-Style-Classification

## Requirements

Keras>=2.0.2
numpy>=1.12.1
pandas>=0.19.2
tqdm>=4.11.2
matplotlib>=2.0.0
Pillow>=2.1.0
h5py>=2.7.0

see requirements.py

ffmpeg <https://www.ffmpeg.org/>
VideoPad <http://www.nchsoftware.com/videopad/index.html>

## How to Use
This code requires you have Keras 2 and TensorFlow 1 or greater installed. Please see the requirements.txt file. To ensure you're up to date, run:

`pip install -r requirements.txt`

Download the dataset in the `data` folder. Download the data from <https://drive.google.com/open?id=170nlQKM58cw_h-GKBa6YoxzHJLFNnS_i> and copy it to `data` folder

Still in the `data` folder, `unrar e 14PDSC.rar`

Create folders with `mkdir train && mkdir test && mkdir sequences && mkdir checkpoints`

Now, move videos to appropriate folders and extract frames:

`python 1_move_files.py`

`python 2_extract_files.py`

Go to the main folder. Extract feature with `extract_features.py`

To train run `train.py`. The model is defined at `models.py`

To see progress while training, run `tensorboard --logdir=data/logs`

To validate, run `validate_rnn.py`

## Results
The model resulted to a 93% accuracy and 26% loss.

## References



## Methodology Citation

Harvey, M. (2017). Five video classification methods implemented in Keras and TensorFlow [Blog Post]. Retrieved from https://blog.coast.ai/five-video-classification -methods-implemented-in-keras-and-tensorflow-99cad29cc0b5


