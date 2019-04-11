# Online-Real-time-Action-Detection
We start our work basd on this paper: [Online Real-time Multiple Spatiotemporal Action Localisation and Prediction](https://arxiv.org/pdf/1611.08563)


## Dataset
- the Dataset is [UCF24](http://www.thumos.info/download.html) with [revised annotaions](https://github.com/gurkirt/corrected-UCF101-Annots) released with this [paper](https://arxiv.org/pdf/1611.08563)
- To simulate the same training and evaluation setup like the paper we use extracted `rgb` images from videos along with optical flow images (both `brox flow` and `real-time flow`) computed for the UCF24 dataset provided by  [google drive link](https://drive.google.com/file/d/1o2l6nYhd-0DDXGP-IPReBP4y1ffVmGSE/view?usp=sharing).
- **Based to my work on Google Colab,you just need to copy the below code as it is and run it.**
```Shell
# Create project forder and dataset folder
!mkdir Action_Detection
%cd Action_Detection
!mkdir Dataset
%cd ..

# Download the dataset
# Note: to download the dataset you should add it to your drive first 
from google.colab import drive
drive.mount('/content/gdrive')
!cp /content/gdrive/My\ Drive/Colab_Notebooks/ucf24.tar.gz /content/Action_Detection/Dataset

# Extract the datasetfile 
%cd Action_Detection/Dataset/
!gunzip ucf24.tar.gz
!tar -xf ucf24.tar
!rm ucf24.tar
```
