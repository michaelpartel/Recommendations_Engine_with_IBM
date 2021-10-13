## Recommendations_Engine_with_IBM
Udacity Data Science Nanodegree - Recommendation Engines project

### Overview
This project works with the articles hosted with IBM and analyzes user interactions to create 
recommendations to users for content to view. This is performed via Rank and Collaborative-based
recommendations and evaluated via SVD. Code has been leveraged from the class instructor / lessons, 
and from the Peer/Mentor discussion boards.

### ToC
1. [Libraries](#libraries)
2. [File Descriptions](#files)
3. [Recommendations_with_IBM](#project)
4. [Results](#results)

### Libraries <a name="libraries"></a>
The following libraries were utilized:
* Pandas
* Numpy
* cv2
* sklearn
* tqdm

Version requirements:
  opencv-python==3.2.0.6
  h5py==2.6.0
  matplotlib==2.0.0
  numpy==1.12.0
  scipy==0.18.1
  tqdm==4.11.2
  keras==2.0.2
  scikit-learn==0.18.1
  pillow==4.0.0
  ipykernel==4.6.1
  tensorflow==1.0.0

### File Descriptions <a name="files"></a>
* dog_app.ipynb: Primary Jupyter Notebook project file containing all code. Can be run as-is.
* extract_bottleneck_features.py: provided code to extract bottleneck features.
* bottleneck_features
  - DogResnet50Data.npz: bottleneck features for use with the ResNet50 model
  - DogVGG16Data.npz: bottleneck features for use with the VGG16 model
* haarcascades:
  - haarcascade_frontalface_alt.xml: provided OpenCV2 face detector
* images:
  - assorted jpeg images of dogs and humans
* requirements:
  - assorted O/S requirements to run the jupyter notebook.
* saved_models:
  - models saved during execution in hdf5 format

### Summary <a name="project"></a>
The project file is based on the following structure:
    Step 0: Import Datasets
    Step 1: Detect Humans
    Step 2: Detect Dogs
    Step 3: Create a CNN to Classify Dog Breeds (from Scratch)
    Step 4: Use a CNN to Classify Dog Breeds (using Transfer Learning)
    Step 5: Create a CNN to Classify Dog Breeds (using Transfer Learning)
    Step 6: Write your Algorithm
    Step 7: Test Your Algorithm

### Results <a name="results"></a> 
The ResNet50 model, when using transfer learning over 20 epochs, provided 79.9% accuracy and
could identify all but one of the sample images correctly. This is likely to be due to artifacts
present in the image which prevented sufficient features from being identified.
