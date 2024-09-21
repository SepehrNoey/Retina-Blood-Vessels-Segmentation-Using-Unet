# Retina Blood Vessels Segmentation Using U-Net

This project aims to segment blood vessels in retina images using a U-Net model. We used a combination of the **DRIVE** and **HRF** datasets to enhance the model's generalization capabilities. The dataset was augmented using various image transformations such as `HorizontalFlip`, `VerticalFlip`, `ElasticTransform`, `GridDistortion`, and `OpticalDistortion` to further improve performance (augmentation logic can be found in [`data.py`](data.py)).

### Model Overview
- **Architecture**: [U-Net](https://www.geeksforgeeks.org/u-net-architecture-explained/)
- **Framework**: TensorFlow
- **Training**: The model was trained for **100 epochs** on a Kaggle P100 GPU.

### Sample Results
Three samples of the model output. The images from left to right are: input image, true mask, and predicted mask.

![01_test](https://github.com/user-attachments/assets/080a1bdc-39dd-4481-8f5b-95a3282d1412)
![02_test](https://github.com/user-attachments/assets/d8bcdb1f-665a-4b66-a57e-6e4b79f7e517)
![17_test](https://github.com/user-attachments/assets/f47dc233-b202-407e-a2ab-a684a3fcd10c)




### Dataset
The project combines two retina datasets:
- **DRIVE** (Digital Retinal Images for Vessel Extraction)
- **HRF** (High-Resolution Fundus Image Database)

Both datasets were augmented to increase the variety and complexity of training examples.

### Augmentation Techniques
We applied the following augmentation techniques:
- **Horizontal Flip**
- **Vertical Flip**
- **Elastic Transform**
- **Grid Distortion**
- **Optical Distortion**

This augmentation enhances the model's robustness by exposing it to various transformations of the retina images.
