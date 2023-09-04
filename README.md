# SBSPS-Challenge-10993-Slient-Speech-Recognition-Automatic-Lip-reading-Model-using-3D-CNN-and-GRU
Slient Speech Recognition : Automatic Lip reading Model using 3D CNN and GRU

## YouTube Demo



[Watch the YouTube Demo Here](https://www.youtube.com/watch?v=Yx9jtqwB5nQ)

![image](https://github.com/smartinternz02/SBSPS-Challenge-10993-Slient-Speech-Recognition-Automatic-Lip-reading-Model-using-3D-CNN-and-GRU/assets/74406604/76085a62-fe32-4ac2-abdb-3c08bab05b19)

## Silent Speech Recognition using Deep Learning



### Project Overview



#### Objective



The goal of this project is to develop a Silent Speech Recognition (SSR) system using a deep learning approach. The system aims to convert video frames of silent articulation into text, enabling a new form of human-machine interaction.



#### Technologies Used



- Python

- PyTorch

- Numpy



## 4. Model Architecture

The model for this project is a Sequential deep learning model that employs Conv3D layers, Bidirectional LSTM layers, and Dense layers for Silent Speech Recognition. Here's a detailed breakdown of the architecture:

### Convolutional 3D Layers

#### First Conv3D Layer
- **Filters**: 128
- **Kernel Size**: 3x3x3
- **Activation**: ReLU
- **Padding**: Same
- **Input Shape**: (75, 46, 140, 1)
- **Followed by**: MaxPooling3D with a pool size of (1, 2, 2)

#### Second Conv3D Layer
- **Filters**: 256
- **Kernel Size**: 3x3x3
- **Activation**: ReLU
- **Padding**: Same
- **Followed by**: MaxPooling3D with a pool size of (1, 2, 2)

#### Third Conv3D Layer
- **Filters**: 75
- **Kernel Size**: 3x3x3
- **Activation**: ReLU
- **Padding**: Same
- **Followed by**: MaxPooling3D with a pool size of (1, 2, 2)

### Time-Distributed Flatten Layer
- Flattens the 3D output to 2D before sending it to the LSTM layers

### Bidirectional LSTM Layers

#### First Bidirectional LSTM Layer
- **Units**: 128
- **Kernel Initializer**: Orthogonal
- **Return Sequences**: True
- **Dropout**: 0.5

#### Second Bidirectional LSTM Layer
- **Units**: 128
- **Kernel Initializer**: Orthogonal
- **Return Sequences**: True
- **Dropout**: 0.5

### Dense Layer
- **Units**: 41
- **Kernel Initializer**: He Normal
- **Activation**: Softmax





#### Gated Recurrent Unit (GRU)



- 256 hidden units



#### Fully Connected Layer



- Output size: vocabulary size (39)



### Data Preprocessing



#### Video Frame Preprocessing



- Frame size: 75x360

- Grayscale conversion



#### Text Sequence Preprocessing



- Text sequence length: Varied (padded to 19 for alignment)

- Vocabulary size: 39



### Implementation Details



#### Challenges and Solutions



##### Mismatch in Tensor Sizes



- **Issue**: The batch size of the output tensor after forward propagation did not match the batch size of the ground truth text sequences.

- **Solution**: Reviewed and debugged each layer to ensure consistent transformation of batch sizes.



##### Padding and Truncation



- **Issue**: Text sequences were not aligned with the video frame sequences.

- **Solution**: Padding and truncation were applied to text sequences to match the sequence length of the video frame output.



### Future Work



- Investigate other architectures such as LSTM and Transformer models.

- Include more complex features such as facial expressions.

- Optimize the model for real-time interaction.


