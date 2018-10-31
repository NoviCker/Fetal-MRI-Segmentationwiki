###
config["split_dir"] = <split_dir_path> # The directory to load/save the train/val/test split files

# For 3D prediction
config["3D"] = True

# For 2D prediction
config["3D"] = False

config["patch_shape"] = (96, 96)  # (x size, y size)
config["patch_depth"] = 64 # (z size)
config["truth_index"] = 0 # (slice index to start prediction)
config["truth_size"] = 64 # (number of slices to predict)
model_name = 'isensee'  # or 'unet'

# Training params - increase batch_size for small models (2D) and decrease for big models (3D)
config["batch_size"] = 8
config["validation_batch_size"] = 8 # most of times should be equal to "batch_size"
config["patches_per_epoch"] = 800  # patches_per_epoch / batch_size = steps per epoch

