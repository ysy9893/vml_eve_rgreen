# pix2pix_summary

- GAN: Conv-BatchNorm-ReLu
- Use L1 distance Not L2 (Euclidean dist) to encourage less blurring
- Generator: **UNet** w/ skip connections (concat low-level info to be shared between the input and output) w/o pooling w/dropouts
- Discriminator (Markovian discriminator) **PatchGAN:** model high-frequencies by restricting attention to the structure in local image patches. PatchGAN only penalizes structure at the scale of patches. (Classify if each NxN patch in an image is real or fake) Models Markov random field, assuming independence b/n pixels spearated by more than a patch diameter. (Hence, patchGAN as a form of texture/style loss.)
- Conditioned the discriminator.
- Provide noise only in the form of dropout
- Total Loss/Goal:
    
    ![Screen Shot 2022-05-18 at 3.03.41 PM.png](pix2pix_summary%20845b8e76a30c443e8980ab30f0de97ae/Screen_Shot_2022-05-18_at_3.03.41_PM.png)