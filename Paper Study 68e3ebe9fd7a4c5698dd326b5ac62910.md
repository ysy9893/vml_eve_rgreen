# Paper Study

[Rendering](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/Rendering%20e61234380d8e46ae9f82afa31090547f.md)

---

import pdb 

pdb.set_trace()

n : next

l: show current code

c: continue until next set trace

---

---

---

---

## Table

- **Pix2Pix Isola et al. [[project](https://phillipi.github.io/pix2pix/)][[notes](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/pix2pix%208376070f7da54a6bb1a9bc73805df563.md)] —-1**
    - GAN: Conv-BatchNorm-ReLu
    - Use L1 distance Not L2 (Euclidean dist) to encourage less blurring
    - Generator: **UNet** w/ skip connections (concat low-level info to be shared between the input and output) w/o pooling w/dropouts
    - Discriminator (Markovian discriminator) **PatchGAN:** model high-frequencies by restricting attention to the structure in local image patches. PatchGAN only penalizes structure at the scale of patches. (Classify if each NxN patch in an image is real or fake) Models Markov random field, assuming independence b/n pixels spearated by more than a patch diameter. (Hence, patchGAN as a form of texture/style loss.)
    - Conditioned the discriminator.
    - Provide noise only in the form of dropout
    - Total Loss/Goal:
        
        ![Screen Shot 2022-05-18 at 3.03.41 PM.png](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/Screen_Shot_2022-05-18_at_3.03.41_PM.png)
        
- **CycleGAN Zhu et al. [[project](https://junyanz.github.io/CycleGAN/)][[notes](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/CycleGAN%20(Unsupervised)%20d62c159362424283a87f650643492498.md)]**
    - The model
        
        ![Untitled](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/Untitled.png)
        
    - Goal:
        
        ![Untitled](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/Untitled%201.png)
        
        ![Untitled](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/Untitled%202.png)
        
    - Loss Breakdown:
        - Adversarial Loss
            
            ![Untitled](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/Untitled%203.png)
            
        - Cycle Consistency Loss
            
            ![Untitled](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/Untitled%204.png)
            
            - Forward cycle consistency + backward cycle consistency
                - with large enough capacity, a network can map the same
                set of input images to any random permutation of images in
                the target domain, where any of the learned mappings can
                induce an output distribution that matches the target distribution. Thus, adversarial losses alone cannot guarantee that the learned function can map an individual input xi to a desired output yi.
                - To further reduce the space of possible mapping functions, the authors argue functions should be cycle consistent.
    
- GAN Goodfellow et al. [[notes](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/GAN%207ec9ed49b4314d75a25f075cfb41207a.md)]
    
    ![Untitled](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/Untitled%205.png)
    
    ![Untitled](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/Untitled%206.png)
    
- DCGAN Radford et al. [project][notes]
- StarGAN Choi et al. [[project](https://github.com/yunjey/stargan)][notes]
    
    
- MUNIT Huang et al. [[project](https://github.com/NVlabs/MUNIT)] —-3
- FUNIT Liu et al. [[project](https://nvlabs.github.io/FUNIT/)]
- SPADE Park et al. [[project](https://nvlabs.github.io/SPADE/)]`
- **AdaIN Huang et al. [[project](https://openaccess.thecvf.com/content_ICCV_2017/papers/Huang_Arbitrary_Style_Transfer_ICCV_2017_paper.pdf)][[video](https://www.youtube.com/watch?v=IIRxJvW6bE4)] —-2**
- Perceptual Loss Johnson et al. [[project](https://cs.stanford.edu/people/jcjohns/eccv16/)]
- TUNIT [[project](https://github.com/clovaai/tunit)]
- ProGAN Karras et al. [[project](https://github.com/tkarras/progressive_growing_of_gans)]
- StyleGAN Karras et al. [[project](https://github.com/NVlabs/stylegan)]
- LPIPS [[link](https://richzhang.github.io/PerceptualSimilarity/)]
- Real-Time User-Guided Image Colorization [[project](https://richzhang.github.io/ideepcolor/)][[video](https://www.youtube.com/watch?v=rp5LUSbdsys)]
- Everybody Dance Now [[projet](https://carolineec.github.io/everybody_dance_now/)]
- NeRF Mildenhall et al. [[project](https://www.matthewtancik.com/nerf)][[notes](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/NeRF%2060dba35e6d914ba59e0a6fb46935af70.md)]

---

[pix2pix](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/pix2pix%208376070f7da54a6bb1a9bc73805df563.md)

[CycleGAN (Unsupervised)](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/CycleGAN%20(Unsupervised)%20d62c159362424283a87f650643492498.md)

[DCGAN](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/DCGAN%20c591c03863df4b1eb873f3948bb1e263.md)

[MUNIT](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/MUNIT%20f8f7473d96ee4cc4b4a8ea80dfc9e9a5.md)

[GAN](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/GAN%207ec9ed49b4314d75a25f075cfb41207a.md)

[NeRF](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/NeRF%2060dba35e6d914ba59e0a6fb46935af70.md)

[starGAN](Paper%20Study%2068e3ebe9fd7a4c5698dd326b5ac62910/starGAN%207866cd2463f34d4e809bfa5e234518f2.md)