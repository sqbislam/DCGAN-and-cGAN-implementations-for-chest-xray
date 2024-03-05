# Description

#### - Deep Convolutional Generative Adversarial Networks (DCGAN)

- **Architecture**: Deep Convolutional Generative Adversarial Networks (DCGANs) leverage convolutional neural networks (CNNs) for both the generator and discriminator networks. This enables them to effectively generate high-resolution images by learning hierarchical representations of visual data.

- **Training Dynamics**: DCGANs are trained using a min-max game framework, where the generator aims to produce realistic images that can fool the discriminator, while the discriminator strives to distinguish between real and generated images. Through adversarial training, both networks improve iteratively, converging towards generating increasingly realistic outputs.

- **Feature Learning**: DCGANs learn to generate images by capturing and synthesizing complex features from input noise vectors. They exploit the hierarchical structure of convolutional networks to extract meaningful representations at different levels of abstraction, enabling the generation of diverse and visually appealing images.

#### - Conditional GAN (CGAN)

<img src="https://user-images.githubusercontent.com/52263269/181246936-54cf9e93-1ab2-4a1a-9896-8f5c241903d8.png" width="60%"></img>

- Conditional version of generative adversarial nets
  - In an unconditioned generative model, there is no control on modes of the data being generated.
  - In the Conditional GAN (CGAN), the generator learns to generate a fake sample with a specific condition or characteristics (such as a label associated with an image or more detailed tag) rather than a generic sample from unknown noise distribution.
  - Simply feeding the data y, and conditioning both the generator and discriminator
- Adversarial learning loss of CGAN

<img src="https://user-images.githubusercontent.com/52263269/181247747-39457171-bb0a-446f-bf51-92f9403d3025.png" width="80%"></img>

# Contents

#### - Generating Chest Xray Image with DCGAN and cGAN

- Generator
  - Input: z (100 dimension), Output: generated image
  - FC [256, 512, 1024]
- Discriminator
  - Input: image (generated or real), Output: fake/real
  - FC [1024, 512, 256]

# Dataset

#### - Chest Xrays

[https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)

# References

#### - CGAN Paper

```
@article{CGAN,
  title={Conditional Generative Adversarial Nets},
  author={Mehdi Mirza, Simon Osindero},
  journal = {arXiv},
  year={2014}
}

```

#### - DCGAN Paper

```
@misc{radford2016unsupervised,
      title={Unsupervised Representation Learning with Deep Convolutional Generative Adversarial Networks},
      author={Alec Radford and Luke Metz and Soumith Chintala},
      year={2016},
      eprint={1511.06434},
      archivePrefix={arXiv},
      primaryClass={cs.LG}
}

```
