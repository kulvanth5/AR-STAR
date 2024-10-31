In this work, we enhance the performance of a multi-stage convolutional RNN by modifying the STAR cell’s activation function. The network aims to classify Satellite Image Time Series (SITS) data of ZeuriCrop dataset from cantonments of Switzerland captured and labelled in 2019, which was proposed in https://arxiv.org/pdf/2102.08820

Below is the image of modification of the STAR cell. Figure 1 shows the original and the Figure 2 shows the modified cell structure.

![image](https://github.com/user-attachments/assets/7666923c-ace0-4678-8e24-5c387fcd6acd)

The Attention-based ReLU effectively highlights critical aspects of feature distinction within the data. By amplifying positive features, it accentuates components associated with desired outputs, making them more accessible to the network’s decision process. Meanwhile, suppressing negative features reduces noise, preventing weak or irrelevant signals from influencing the model. This change enables the STAR cell to better capture temporal patterns and improves model focus on essential information. Overall, it supports the network’s resilience against the gradient vanishing issue that affects deep RNNs.

Experimentally, this adjustment resulted in a noticeable boost in model performance, observing a 4% increase in the F1 score, from 52% to 56%, 6% increase in precision from 60% to 66%. This improvement reflects a stronger balance of precision and recall, crucial for effectively handling complex data. Such results confirm the effectiveness of Attention-based ReLU in enhancing feature discrimination within the model. By refining the STAR cell's activation, we demonstrate that targeted modifications can significantly advance performance in RNN-based architectures.
