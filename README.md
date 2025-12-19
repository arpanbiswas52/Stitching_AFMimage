
# A bi-channel Aided Stitching of Atom Force Microscopy Images 

**Huanhuan Zhao**, Ruben Millan-Solsona, Marti Checa, Spenser R. Brown, Jennifer L. Morrell-Falvey, Liam Collins, **Arpan Biswas** 

 	
Zhao, H., Millan-Solsona, R., Checa, M. et al. A bi-channel aided stitching of atomic force microscopy images. Sci Rep 15, 41897 (2025). https://doi.org/10.1038/s41598-025-25855-y


### Abstract
Microscopy is an essential tool in scientific research, enabling the visualization of structures at micro- and nanoscale resolutions. However, the field of microscopy often encounters limitations in field-of-view (FOV), restricting the amount of sample that can be imaged in a single capture. To overcome this limitation, image stitching techniques have been developed to seamlessly merge multiple overlapping images into a single, high-resolution composite. The images collected from microscope need to be optimally stitched before accurate physical information can be extracted from post analysis. However, the existing stitching tools either struggle to stitch images together when the microscopy images are feature sparse or cannot address all the transformations of images when performing image stitching. To address, in this paper, we propose a two-channel aided feature-based image stitching method and showcased on Atomic Force Microscopy (AFM) generated biofilm images as experimental data. The topographical channel image of AFM data captures the morphological details of the sample, and a stitched topographical image is desired for researchers. We utilize the amplitude channel of AFM data to maximize the matching features and to estimate the position of the original topographical images. We see the proposed two-channel aided stitching method outperforms the traditional direct stitching approach in AFM topographical image stitching task. Furthermore, we found that the differentiation of the topographical images along the x-axis provides similar feature information to the amplitude channel image, which generalizes our approach when the amplitude images are not available. Here we demonstrated the application on AFM, but similar could be employed of optical microscopy with brightfield and fluoresce channels. We believe this proposed workflow can serve as a valuable augmentation strategy for microscopy image stitching tasks and will benefit the experimentalist to avoid erroneous analysis and discovery due to incorrect stitching.

![image](https://github.com/user-attachments/assets/5cd9fadd-c037-4a04-9cf2-9bbfd6e1840f)

Proposed approach of feature-based bi-channel aided image stitching of microscopy images. Here fig. (a) shows the traditional single-channel stitching of stack of overlapped microscopy images of interest (eg. topographical images) where (b) shows the bi-channel stitching of the topographical images via our proposed approach of using physical information from optimal second imaging channel (Eg. amplitude image). 

### Description
This repository includes links, code, scripts, and data to generate the figures in a paper. 

### Data
The samples used in this study correspond to **Pantoea sp. YR343**. The dataset was collected from AFM images, acquired using the DriveAFM system from Nanosurf, as described in [1]. More information on the dataset is provided in the main paper and notebook. The raw dataset is provided in **Data** folder [here](https://github.com/arpanbiswas52/Stitching_AFMimage/tree/main/data). 

### Usage
There are two jupyter notebook files in the **src** folder, [AFM_image_preprocessing.ipynb](https://github.com/arpanbiswas52/Stitching_AFMimage/blob/main/src/AFM_image_preprocessing.ipynb) is used to generate flattened topographical images, amplitude images, and differential images. [AFM_stitching_V2.ipynb](https://github.com/arpanbiswas52/Stitching_AFMimage/blob/main/src/AFM_stitching_V2.ipynb) is used to stitch the images together. To test the code with the AFM images used in the paper, the user needs to:
- Step 1: Install environment using `pip install -r requirements.txt`.  [requirements.txt](https://github.com/arpanbiswas52/Stitching_AFMimage/blob/main/requirements.txt) contains the necessary libraries for executing the notebook.
- Step 2: Download the datasets from the **Data** folder [here](https://github.com/arpanbiswas52/Stitching_AFMimage/tree/main/data) and unpack it within the same folder as [AFM_stitching_V2.ipynb](https://github.com/arpanbiswas52/Stitching_AFMimage/blob/main/src/AFM_stitching_V2.ipynb). 
- Step 3: Run the [AFM_stitching_V2.ipynb](https://github.com/arpanbiswas52/Stitching_AFMimage/blob/main/src/AFM_stitching_V2.ipynb) notebook. 
- If you are using your own data, you can either preprocess it using [AFM_image_preprocessing.ipynb](https://github.com/arpanbiswas52/Stitching_AFMimage/blob/main/src/AFM_image_preprocessing.ipynb) or prepare the flattened images and second channel images by yourself. Remember to change the input path to your own data path when running [AFM_stitching_V2.ipynb](https://github.com/arpanbiswas52/Stitching_AFMimage/blob/main/src/AFM_stitching_V2.ipynb).




### Support

The authors acknowledge the use of facilities and instrumentation at the UT Knoxville Institute for Advanced Materials and Manufacturing (IAMM) and the Shull Wollan Center (SWC) supported in part by the National Science Foundation Materials Research Science and Engineering Center program through the UT Knoxville Center for Advanced Materials and Manufacturing [DMR-2309083](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2309083&HistoricalAwards=false). AFM imaging was performed at the Center for Nanophase Materials Sciences (CNMS), which is a US Department of Energy, Office of Science User Facility at ORNL.

<img width="400px" src="https://mrsec.org/sites/default/files/MRSEC%20logo_clear%20background.png">


### Reference
[1]Millan-Solsona, R., Brown, S.R., Zhang, L. et al. Analysis of biofilm assembly by large area automated AFM. npj Biofilms Microbiomes 11, 75 (2025). https://doi.org/10.1038/s41522-025-00704-y


