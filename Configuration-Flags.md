###
config["split_dir"] = <split_dir_path> # The directory to load/save the train/val/test split files
config["data_file"] = "<base_dir>/fetal_data.h5",
config["model_file"] = "<base_dir>/fetal_net_model",
  "training_file": "./split2/training_ids.pkl",
  "validation_file": "./split2/validation_ids.pkl",


# For 3D prediction
config["patch_shape"] = (32, 32)  # x,y patch size
config["patch_depth"] = 16 # z patch size
config["truth_index"] = 0 # 
config["truth_size"] = 16