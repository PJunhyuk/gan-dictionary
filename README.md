## 3D-GAN

#### PAPER
[Learning a Probabilistic Latent Space of Object Shapes via 3D Generative-Adversarial Modeling](https://arxiv.org/abs/1610.07584)

> Submitted on 24 Oct 2016 (last revised 4 Jan 2017)  
> Jiajun Wu, Chengkai Zhang, Tianfan Xue, William T. Freeman, Joshua B. Tenenbaum  

#### CODE
- Tensorflow: [tf-3dgan](https://github.com/meetshah1995/tf-3dgan)
- Release: [3dgan-release](https://github.com/zck119/3dgan-release)

#### ETC
- Official Website: [3D Generative Adversarial Network](http://3dgan.csail.mit.edu/)
- Official Video: [Learning a Probabilistic Latent Space of Object Shapes via 3D Generative-Adversarial Modeling](https://www.youtube.com/watch?v=mfx7uAkUtCI)

#### DISCRIPTION

###### Structure
- Generator: Latent vector -> Shape in 3D Voxel Space
- Discriminator: Shape in 3D Voxel Space -> Generated or real?

###### Result
- Generate Randomly Sampled Shapes from Latent vector

###### Extension
- 3D Shape Classification
- Single Image 3D Reconstruction - with Variational image encoder
    > Variational image encoder maps an image to a latent vector for 3D object reconstruction / latent vector to 3D object by 3D-GAN  
    > VAE-GAN [Larson et al., 2016], TL-Network [Girdhar et al., 2016]

- - -

## VAE-GAN

#### PAPER
[Autoencoding beyond pixels using a learned similarity metric](https://arxiv.org/abs/1512.09300)

> Submitted on 31 Dec 2015 (last revised 10 Feb 2016)  
> Anders Boesen Lindbo Larsen, Søren Kaae Sønderby, Hugo Larochelle, Ole Winther

#### CODE
- Tensorflow: [tf-vaegan](https://github.com/JeremyCCHsu/tf-vaegan)  

#### ETC

#### DISCRIPTION

###### Structure

###### Result

###### Extension