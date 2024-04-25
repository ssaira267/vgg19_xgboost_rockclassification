# **Multimodal Learning by Combining FMS Image Representations With Wireline Logs Using XGBoost for Final Classification**
### This repository contributes to Chapter 6 of Saira Baharuddin's PhD thesis, entitled "Multimodal Learning for Carbonate Rock Classification Using Microresistivity Images and Wireline Logs".

## Brief Overview
This is my second approach as part of the multimodal learning for carbonate rock classification where I incorporate both FMS images and  wireline log data. However, since these two types of data are presented in different formats - visual representations for FMS images and tabular format for wireline log data - integrating them presents a challenge due to their disparate nature. To address this issue, I use VGG19 for feature extraction from FMS images followed by concatenation of the extracted features with the wireline logs. This new dataset was then used for carbonate rock classification using gradient-boosted decision tree (GBDT), XGBoost, as portrayed in figure below. This integration enables a comprehensive analysis of both visual and tabular data. The highest overall accuracy of the XGBoost model is 86% on the standard resolution dataset.

<p align="center">
    <img width="1000" alt="vgg19_xgboost" src="https://github.com/ssaira267/vgg19_xgboost_rockclassification/assets/57672761/bb552f8b-3467-48e1-802c-48bf18a2cc55">
  Network architecture of the ensemble transfer learning VGG19 model with XGBoost for rock classification
</p>

## Repository Contents
- Data: Sample datasets used for training and testing the models are publicly available on the following website: https://mlp.ldeo.columbia.edu/logdb/scientific_ocean_drilling. The dataset used are from Leg 194, holes 1194B, 1196A and 1199A. The .csv files inside the data directory serve as examples demonstrating how the data is arranged and used for this study. These files contain structured data in tabular format, where each row represents a sample or observation based on depth, and each column represents a feature or attribute of that sample. Due to the large file size of the FMS images, I am unable to upload the FMS images folder. However, the images are available on the website mentioned earlier. It's important to note that the FMS images have been cropped based on the depth intervals specified for the study.
- Notebooks: Python codes developed include data preprocessing, model training, model evaluation, and visualization of the results.
- Documentation: Additional resources and documentation that outline the methods used in this study.

## How to Use
To run the scripts in this repository:
1. Ensure that Python 3.8 (and above) and the necessary libraries (listed in requirements.txt) are installed.
2. Clone the repository to your local machine.
3. Navigate to the notebooks directory and run the desired notebook as follows:
  
```bash
  python notebook_name.py
```

## Dependencies 
- Dlisio
- Imbalanced-learn
- Livelossplot
- Matplotlib
- NumPy
- OpenCV-python
- pandas
- Scikit-learn
- Seaborn
- Tensorflow
- Tensorflow-Keras
- XGBoost

Please refer to 'requirements.txt' for a complete list of dependencies.

## Contact
For any queries related to this repository or the research, please contact:
- Saira Baharuddin                  - Email: s.baharuddin19@imperial.ac.uk
- Prof Cédric John (PhD Supervisor) - Email: cedric.john@qmul.ac.uk


