# Video-Frame-Extraction

### Introduction
The Key Frame Extraction Project is a Python-based tool for extracting KEY FRAMES from a given video. It uses a combination of techniques, including **Frame Differencing**, **Clustering**, and **Laplacian Variance**, to identify important/significant frames in a video.

### Requirements
Make sure you have the following dependencies installed:

All the required libraries are mentioned in requirement.txt file:
* OpenCV
* hdbscan==0.8.24
* matplotlib==3.1.1
* numpy==1.17.1
* scikit-image==0.16.2
* scikit-learn==0.21.3
* scipy==1.3.2
* seaborn==0.9.0
* sklearn==0.0
* opencv-contrib-python==4.1.1.26

Use **`pip install -r requirement.txt`** to install all the requirements.

### Usage
To run the code refer [RUN_Key Frame Extraction.ipynb](./RUN_Key Frame Extraction.ipynb) file.

`python candidate_frames_folder.py --input_videos <path_to_video_file> --output_folder_video_image <output_folder_for_candidate_frames> --output_folder_video_final_image <output_folder_for_key_frames>`

Replace **<path_to_video_file>**, **<output_folder_for_candidate_frames>**, and **<output_folder_for_key_frames>** with specific **video file path** and **desired output folder paths**.

### Current Setting of Parameters
* window_len = 10
* max_frames_in_chunk = 2500
* LUV Color Space (for frame difference calculation)
* smoothening window type = 'hanning'
* Pre-Processing Step for HDBSCAN Algorithm: DCT Transformation for Feature Extraction
* distance metric = 'manhattan'
* min_cluster_size = 2
* min_samples = 2

### Output
* Candidate Key Frames will be saved in the directory whose path is given by: **<output_folder_for_candidate_frames>**
* Clusters will also be displayed in this folder: **<output_folder_for_candidate_frames>**

* Final Key Frames Extracted will be saved in the directory whose path is given by: **<output_folder_for_key_frames>**

### For Further details refer documentation: [Video_Frame_Extraction DOC](https://docs.google.com/document/d/1S1bIYTfvK84UzY4s0dCdA1Dii6uPkgVSGVyc6BMzwKA/edit?usp=sharing)

### Sample Videos and the extracted Final Key Frames: [Final_Key_Frames](https://drive.google.com/file/d/13SypyI84yJiNszVKXeUHQPpdkmTvu-uO/view?usp=drive_link)
