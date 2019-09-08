# 3D-Hand-Pose-Sequence-Data-Augmentation-using-GANs
The human hand plays a crucial role in conveying emotions and carrying out most day-to-day activities. Therefore numerous modern technologies - ranging from gesture control to autonomous driving - would benefit from the reliable recognition of certain hand actions. This can be done using a two-step approach, in which first hand poses are obtained from video frames and then the resulting sequences are classified in the 3D skeleton space. Existing techniques that aim to solve the second step are mostly based on deep learning methods. Given the high complexity and dimensionality of the human hand, these require large amounts of training data to achieve good performance. As the collection of precisely annotated hand pose data is time-consuming and expensive, data augmentation appears as an advantageous practice to increase the recognition accuracy for a given classifier.  

This thesis proposes a suitable WGAN-GP architecture for the generation of synthetic hand skeleton sequences with variable length. The recommended critic consists of a multi-layer perceptron with three hidden layers, while the generator is based on two RNNs and receives a start frame as input. Both networks are conditioned on the action class. The best performing model was trained on multiple classes simultaneously and selected based on the smallest generator loss. When its synthetic samples were used to augment the training set of a 1-layer LSTM classifier, the classification error on several subsets as well as on the complete dataset decreased. Quantitative results show that the chosen GAN-based data augmentation outperforms alternative standard methods. Furthermore, no clear correlation between the visual appearance of the generated samples and their resulting improvement on recognition accuracy was found. 
