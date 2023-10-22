# PL-SLAM
A version of PL-SLAM that stores the outputs and has proper run instructions. 

**Run instructions** 

After building the project: 
* cd build
* export DATASETS_DIR='/home/pl_slam/Documents/datasets/' -> The directory where your datasets are.
* ./plslam_dataset mh01easy/ -c '/home/pl_slam/Documents/pl_slam/config/config/config_euroc.yaml' -> Run. mh01easy/ is the directory to the dataset in the defined DATASET_DIR folder.
* 
**Trajectory**
  Trajectory results are stored in output.txt in the format x, y, z, roll, pitch, yaw.
  Only keyframes are stored.
  The times are not stored, but the relative frame index of each keyframe is stored in a keyframe_indices text file. The line is the corresponding keyframe and the value is its index relative to all frames from the dataset. From this you can do some easy associations to get the required times. NB: Indexing starts at 1!!!

  Hope this addition to PL-SLAM helps!
