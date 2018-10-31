###
`config["split_dir"] = <split_dir_path> # The directory to load/save the train/val/test split files`

### For 3D prediction
`config["3D"] = True`

### For 2D prediction
`config["3D"] = False`

### Input params
`config["patch_shape"] = (96, 96)  # (x size, y size)  `<br>
`config["patch_depth"] = 64 # (z size)  `<br>
`config["truth_index"] = 0 # (slice index to start prediction)  `<br>
`config["truth_size"] = 64 # (number of slices to predict)  `<br>
`model_name = 'isensee'  # or 'unet'  `<br>

### Training params - increase batch_size for small models (2D) and decrease for big models (3D)
`config["batch_size"] = 8  `<br>
`config["validation_batch_size"] = 8 # most of times should be equal to "batch_size"  `<br>
`config["patches_per_epoch"] = 800  # patches_per_epoch / batch_size = steps per epoch  `<br>

