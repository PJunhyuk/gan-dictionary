# GAN-DICTIONARY

### 3D-GAN

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
    > [VAE-GAN](https://github.com/PJunhyuk/gan-dictionary#vae-gan) [Larson et al., 2016], TL-Network [Girdhar et al., 2016]

- - -

### VAE-GAN

#### PAPER
[Autoencoding beyond pixels using a learned similarity metric](https://arxiv.org/abs/1512.09300)

> Submitted on 31 Dec 2015 (last revised 10 Feb 2016)  
> Anders Boesen Lindbo Larsen, Søren Kaae Sønderby, Hugo Larochelle, Ole Winther

#### CODE
- Tensorflow: [tf-vaegan](https://github.com/JeremyCCHsu/tf-vaegan)  

#### DISCRIPTION

###### Structure

###### Result

###### Extension

- - -

### DiscoGAN

#### PAPER
[Learning to Discover Cross-Domain Relations with Generative Adversarial Networks](https://arxiv.org/abs/1703.05192)

> Submitted on 15 Mar 2017 (last revised 15 Mar 2017)  
> Taeksoo Kim, Moonsu Cha, Hyunsoo Kim, Jung Kwon Lee, Jiwon Kim

#### CODE
- PyTorch(Official): [DiscoGAN](https://github.com/SKTBrain/DiscoGAN)  
- PyTorch: [DiscoGAN-pytorch](https://github.com/carpedm20/DiscoGAN-pytorch)
- Tensorflow: [DiscoGAN](https://github.com/ChunyuanLI/DiscoGAN)
- Chainer: [chainer-DiscoGAN](https://github.com/dhgrs/chainer-DiscoGAN)

#### ETC
- Summary(Official, Korean): [SK T-Brain Research](https://tinyurl.com/mt333g3)
- Presentation material(Korean) by Il Gu Yi in Modulabs: [DeepLAB_Paper_library_DiscoGAN](http://www.modulabs.co.kr/DeepLAB_Paper_library/15071)

#### DISCRIPTION
- DiscoGAN can discovery cross-domain relation without pair-labeling dataset.  
- DiscoGAN can handle mode collapse and oscillation problem.  

###### Structure
- Generator G_AB: Image in style A -> Image in style B  
- Generator G_BA: Image in style B -> Image in style A  
- Discriminator D_A: X_A & X_BA (L_D_A)
- Discriminator D_B: X_B & X_AB (L_D_B)
- Cycle 1: X_A -> G_AB -> X_AB -> G_BA -> X_ABA  
- Cycle 2: X_B -> G_BA -> X_BA -> G_AB -> X_BAB  
- L_const_A = X_A & X_ABA  
- L_const_B = X_B & X_BAB  
- L_D_A = X_A & X_BA  
- L_D_B = X_B & X_AB


###### Result
- Generate image in new type with similar style of original image  
    - Car to car
        > Using rendered images of 3D car models with varying azimuth angles, predicts the azimuth angle of a car  

    - Face Conversion
        > Sharing almost all features  
        
        - Translation of gender
            > Female face to male face with similar mood  

        - Translation of hair color and eyeglasses  
            > Blond hair to black hair with same face  

        - Translation of face
    - Chair to Car, Car to Face
        > Sharing only one features  

        - Images with similar orientation  
    - Edges to Photos  
        > Paint in sketch image  

    - Handbag to Shoes, Shoes to Handbag  
        > Generate handbag image with similar style of original shoe image  

###### Extension

- - -

### Pose Guided Person Image Generation

#### PAPER
[Pose Guided Person Image Generation](https://arxiv.org/abs/1705.09368)

> Submitted on 25 May 2017 (last revised 19 Jun 2017)  
> Liqian Ma, Xu Jia, Qianru Sun, Bernt Schiele, Tinne Tuytelaars, Luc Van Gool  

#### CODE
None

#### ETC
None

#### DISCRIPTION

###### Structure
- Generator at Stage-1(G1): concat of Condition Image & Target pose -> coarse result
- Generator at Stage-2(G2): concat of Condition Image & coarse result (-> difference map + coarse result) -> refined result
> skip connection in Generators
- Discriminator at Stage-2(D): Real pair(Target Image & Condition Image) & Fake pair(refined result & Condition Image)

###### Result
- Generate person's whole body image with target pose

###### Extension
-

- - -

### Auto-Encoding Variational Bayes

#### PAPER
[Auto-Encoding Variational Bayes](https://arxiv.org/abs/1312.6114)

> Submitted on 20 Dec 2013 (last revised 1 May 2014)
> Diederik P Kingma, Max Welling

#### DISCRIPTION

- - -

## Main Reference

- [really-awesome-gan](https://github.com/nightrome/really-awesome-gan)  
- [the-gan-zoo](https://github.com/hindupuravinash/the-gan-zoo)

- - -

## Datasets

### [Large-scale Fashion (DeepFashion) Database](http://mmlab.ie.cuhk.edu.hk/projects/DeepFashion.html)
> A large-scale clothes database
- Pose Guided Person Image Generation: The DeepFashion (In-shop Clothes Retrieval Benchmark) datset

### [Market-1501 Dataset](http://www.liangzheng.org/Project/project_reid.html)
> Collected in front of a supermarket in Tsinghua University
- Pose Guided Person Image Generation