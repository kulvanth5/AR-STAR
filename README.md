In this work, we propose a novel solution with the Attention-based Rectified Linear Unit Stackable Recurrent Cell (AR-STAR), a model specifically designed to effectively identify and classify underrepresented crop types, even when limited data is available. By incorporating Attention mechanisms within a STAckable Recurrent framework, AR-STAR enhances the model's ability to focus on critical patterns, ensuring better generalization to rare classes as well.

We demonstrate the efficacy of our approach on a leading benchmark ZeuriCrop dataset from cantonments of Switzerland captured and labelled in 2019, which was proposed in https://arxiv.org/pdf/2102.08820. Mustards, Beets, Summer Rapeseed, Tobacco, Buckwheat, Pumpkin and Winter Rapeseed are the few under-represented classes in this dataset.

Below is the figure of the proposed AR-STAR cell

![image](https://github.com/user-attachments/assets/7666923c-ace0-4678-8e24-5c387fcd6acd)

The Attention-based ReLU effectively highlights critical aspects of feature distinction within the data. By amplifying positive features, it accentuates components associated with desired outputs, making them more accessible to the network’s decision process. Meanwhile, suppressing negative features reduces noise, preventing weak or irrelevant signals from influencing the model. This change enables the STAR cell to create a clear distinction b/w the features and  capture temporal and spatial patterns in most essential way. It is also computationally less intensive than other activation functions.

Experimentally, AR-STAR observed a noticeable boost in its performance, a 4% increase in the F1 score, from 52% to 56%, 6% increase in precision from 60% to 66% over the existing state-of-the-art model on this dataset. These improvements in class-wise metrics are the testimonials of our claims that AR-STAR can handle class imbalance in real-world datasets.
