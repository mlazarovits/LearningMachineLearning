---
title: "7/31/19 Paper Discussion: Batch Normalization"
---

This week Micah led us in a discussion [this paper](../../../assets/papers_summer19/batch_normalization.pdf) on batch normalization (BN), which is a technique used in machine learning to speed up learning accurately. The way batch normalization works is by renormalizing the distribution of the data after it passes through a layer in a neural network. This distrubtion depends on the parameters of the network, so small changes to the distribution will be amplified downstream. This process is called internal covariate shift, and batch normalization works to minimize this. This helps with optimization of network performance by normalizing the distribution. In "Batch Normalization," Ioffe and Szegedy cite papers by LeCun, et. al. (1998) and Wiesler & Ney (2011) to assert that "the network converges faster if its inputs are whitened," transformed to have mean of zero and unit variance. This is what BN achieves "at every training step or some interval" for mini-batches of data. Mini-batches are used so that "the statistics used for normalization can fully participate in the gradient backpropagation." Thus, the information learned in the BN layer can be backpropagated throughout the network. One issue with BN is that it changes the data, not just the distribution. To counteract this, "we make sure that the transformation inserted in the network can represent the identity transform."

{% capture fig_img %}
![Foo]({{"/assets/images/BN_meeting.jpg" | relative_url}})
{% endcapture %}

<figure>
	{{fig_img | markdownify | remove: "<p>" | remove: "</p>"}}
	<figcaption>Micah leading out discussion in batch normalization.</figcaption>
</figure>

The paper provides two examples of improved performance with BN networks. The first is training a deep neural network (DNN) on identifying handwritten digits from the MNIST dataset. As seen from Figure 1a, "the batch-normalized network enjoys the higher test accuracy." Distributions of the data at the {15, 50, 85}th percentiles also demoonstrate how BN regularizes the distribution of data over training steps. The second example of BN performance is demonstrated with a convolutional neural network (CNN). Figure 2 shows that the BN networks reached the same level of accuracy as the networks without BN in much fewer steps (about half or even smaller fractions).