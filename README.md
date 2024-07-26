- ENVIRONMENT: google Colab, Jupyter NoteBook.
- TGANet:

Input Image: The model processes a medical image input (e.g., endoscopic images).
Block 1 to Block 4: These blocks represent the foundational part of the network, where each block extracts features from the input image at different levels of abstraction.
Feature Enhancement Modules (FEM): Each block is followed by an FEM that helps to enhance the features extracted by the foundational blocks.
Concat: The outputs of the FEMs are concatenated to aggregate the enhanced features.
Decoder Blocks: The concatenated features are fed into a series of decoder blocks. Each decoder block helps to reconstruct high-resolution output by progressively increasing the resolution of the features.
Label Attention: Each decoder block incorporates a label attention mechanism that refines the feature maps based on label predictions at different levels.
Multi-Scale Feature Aggregation (MSFA): This component aggregates features from different levels to provide a final prediction mask for polyps.
Output: The final output is a prediction mask indicating the presence and location of polyps.
Feature Enhancement Module (FEM):

Input: Features from a foundational block serve as input to the FEM.
1x1 CBR (r=1): A convolutional layer with a 1x1 kernel size to adjust feature dimensions.
3x3 CBR with dilations (r=6, 12, 18): These layers use dilated convolutions to capture multi-scale context.
Channel Attention Module (CAM): Enhances the feature map by focusing on important channels.
Concatenation: Outputs from different convolutional layers are concatenated.
3x3 Conv + BN: A convolutional layer with batch normalization to combine the concatenated features.
Spatial Attention Module (SAM): Enhances spatial features.
Output: The enhanced feature map is the output for the next stage.
Decoder Block with Label Attention:

Input: Features from the FEM are input to the decoder block.
Upsample: The feature map is upsampled to a higher resolution.
Concat: The upsampled features are concatenated with features from previous stages.
1x1 CBR + 3x3 Conv + BN: A series of convolutional layers with batch normalization and ReLU activation.
Label Attention: This component uses label prediction features to refine the feature map.
CBAM (Convolutional Block Attention Module): Integrates channel and spatial attention mechanisms to improve feature representation.
Output: The refined feature map and label features are the output for further processing.
Embedding Fusion: Combines embedding features using byte-pair encoding to handle various attributes such as the number and size of polyps.
Connect Residual: Residual connections are used throughout the architecture to support gradient flow and enhance learning efficiency.
