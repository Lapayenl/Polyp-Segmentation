- ENVIRONMENT: google Colab, Jupyter NoteBook.
TGANet:
![image](https://github.com/user-attachments/assets/98b0069d-b2e4-4334-be08-5a5e7f4d2ebe)
  TGANet is a neural network model designed for medical image processing, including endoscopic images. It consists of:
- Blocks 1-4: Extract features from the input image at different levels.
- Feature Enhancement Modules (FEM): Improve features using 1x1 convolution layers, 3x3 dilated convolutions with different dilation rates, Channel Attention Module (CAM), and Spatial Attention Module (SAM). The - result is an enhanced feature map.
-Decoder Blocks with Label Attention: Increase the resolution of the feature map and refine it by combining features from previous stages and using Label Attention along with Convolutional-block Attention Module (CBAM).
-Multi-Scale Feature Aggregation (MSFA) aggregates features from different levels to provide a final prediction of the presence and location of polyps.
