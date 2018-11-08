### Prediciting on mat files (Michael format):

```
python -m prod.predict_mat2 --input_mat <input_path>.mat \
                            --output_mat <output_path>.mat \
                            --overlap_factor 0.9 \
                            --config_dir <path_to_config>/ \
                            --preprocess window_1_99 \
                            --config2_dir isensee3d_new \
                            --preprocess2 window_1_99
```

overlap_factor - overlap between predicted patches (0-1, less overlap means faster prediction)
config_dir - path to folder containing the config file (also the normalization file if needed)
preprocess window_1_99 - make intensity windowing (percentile 1, percentile 99) pre-processing to the data

Flags to apply secondary prediction on ROI:
config2_dir
preprocess2

### Prediciting on nifti files:
```
python -m prod.predict_nifti2 --input_nii <path_to_nifti> \
                              --output_folder <output_folder> \
                              --overlap_factor 0.9 \
                              --config_dir <path_to_config> \ 
                              --preprocess window_1_99 \ 
                              --config2_dir <path_to_config2> \ 
                              --preprocess2 window_1_99
```

flags are the same as predicting on mat

### Prediciting on the dataset:
``` 
python -m brats.predict --config_dir <path_to_config>/ \
                        --overlap_factor 0.9 \
                        --split <val/test>
```
