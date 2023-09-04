# SBSPS-Challenge-10993-Slient-Speech-Recognition-Automatic-Lip-reading-Model-using-3D-CNN-and-GRU
Slient Speech Recognition : Automatic Lip reading Model using 3D CNN and GRU

![image](https://github.com/smartinternz02/SBSPS-Challenge-10993-Slient-Speech-Recognition-Automatic-Lip-reading-Model-using-3D-CNN-and-GRU/assets/74406604/76085a62-fe32-4ac2-abdb-3c08bab05b19)

## Silent Speech Recognition using Deep Learning



### Project Overview



#### Objective



The goal of this project is to develop a Silent Speech Recognition (SSR) system using a deep learning approach. The system aims to convert video frames of silent articulation into text, enabling a new form of human-machine interaction.



#### Technologies Used



- Python

- PyTorch

- Numpy



### Model Architecture



#### Convolutional Neural Networks (CNNs)



- **Layer 1**: 64 filters, kernel size 3x3, stride 1x1

- **Layer 2**: 128 filters, kernel size 3x3, stride 1x1



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

  ## YouTube Demo



[Watch the YouTube Demo Here]([https://www.youtube.com/link_here](https://www.youtube.com/watch?v=Yx9jtqwB5nQ)https://www.youtube.com/watch?v=Yx9jtqwB5nQ)

