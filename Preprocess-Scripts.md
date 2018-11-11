Currently the scripts are hardcoded, so open and edit the path's as required.

### window_data.py 
Apply intensity windowing to a dataset

### convert_mats.py (Not very stable, need to validate it does what you wants)
Convert *.mat (Michael's Format) files to a nifti dataset.

### cut_relevant_areas.py
Cut ROI from nifti dataset to create a new dataset with only ROI.

### brats.preprocess.convert_brats_data(in_folder, out_folder)
Do N4BiasFieldCorrection to the data.
You need to download N4BiasFieldCorrection.(exe for Windows) from ANTs website to you system and add it to your path accordingly before calling the script. 