# Installation:

0. Recommended: create new conda environment (conda create -n myenv python=3)
    * Enter environment: conda activate myenv
1. Download the repository: git clone https://github.com/GalDude33/UNET_3D.git
2. Install dependencies: 
    * Install Tensorflow & Keras
    * pip install -r requirements.txt

# Usage:

### Training 
Change the configuration inside "brats/train_fetal.py"

`$ python -m brats.train_fetal --config_dir <config_dir>`

Where <config_dir> is the folder containing the training configurations (or will be creatad to)

### Write prediction images from the validation data
In the training above, part of the data was held out for validation purposes. 
To write the predicted label maps to file:
```
$ python -m brats.predict --config_dir <config_dir>
```
The predictions will be written in the ```<config_dir>/prediction``` folder along with the input data and ground truth labels for comparison.
