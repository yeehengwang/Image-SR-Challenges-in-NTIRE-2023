# Image SR Challenges in NTIRE 2023

![Untitled](Image%20SR%20Challenges%20in%20NTIRE%202023/Untitled.png)

# **Real-Time Super-Resolution Challenge**

## *Important Date*

![Untitled](Image%20SR%20Challenges%20in%20NTIRE%202023/Untitled%201.png)

## *Description*

The goal of the NTIRE 2023 Real-Time Super-Resolution Challenge is to **upscale images in real-time at 60FPS** using deep learning models and commercial GPUs (RTX 3060, 3090).

The input images can be large patches or full-resoluion images, compressed using JPEG q=90.

**TWO TRACKS**

- **Track1** for upscaling from FHD 1080p to 4K resolution (**X2** factor)
- **Track2** for upscaling from HD 720p to 4K resolution (**X3** factor)

## *Demands*

- Satisfy **real-time processing** on RTX 3060 (12Gb) / RTX 3090 (24Gb)
- Metric:**fidelity** (PSNR, SSIM),FLOPs, Memory Consumption, Runtime per image (ms)(More details will be provided to participants via Github)
- Can **train the models using any publicly available open-sourced dataset**
- The **validation/test dataset consists on a brand-new dataset** that includes high-resolution high-quality filtered content from: digital art, videogames, photographies - **Please consider this variety** when training your models
- There is  a **SOTA real-time SR evaluation -** Only for the final phase**.**

![Untitled](Image%20SR%20Challenges%20in%20NTIRE%202023/Untitled%202.png)

# Single **Image Super-Resolution (x4) Bicubic Challenge Track1**

## ***Important dates***

![Untitled](Image%20SR%20Challenges%20in%20NTIRE%202023/Untitled%203.png)

## *Description*

The aim is to obtain a network design / solution capable to produce high quality results with the best **performance (e.g., PSNR).**

The task of restoration of rich details (high frequencies) in a high-resolution image for a single low-resolution input image based on a set of prior examples with low and corresponding high-resolution images.

NOTE:With the dataset the organizers will provide scripts to facilitate the reproducibility of the images and performance evaluation results after the validation server is online. More information is provided on the data page.

# **360° Omnidirectional Image Super-Resolution Challenge**

[GitHub - 360SR/360SR-Challenge: NTIRE 2023 Challenge on 360° Omnidirectional Image and Video Super-Resolution](https://github.com/360SR/360SR-Challenge)

## ***Important dates***

![Untitled](Image%20SR%20Challenges%20in%20NTIRE%202023/Untitled%204.png)

## *Introduction*

Aim to establish high-quality benchmarks for 360° image SR and expect to further highlight the challenges and research problems. This challenge can provide an opportunity for researchers to work together to show their insights and novel algorithms, significantly promoting the development of 360° image  SR tasks.

360° images/videos suffer from the **lower angular resolution problem** since they are captured by the fisheye lens with the same sensor size for capturing planar images. Although the whole 360° images/videos are of high resolution, the details are not satisfying.

360° images/videos are often transformed into 2D planar representations by preserving omnidirectional information in practice, like **equirectangular projection (ERP)** and **cube map projection (CMP).**

## *Description*

This challenge aims to reconstruct high-resolution (HR) 360° images/videos from degraded low-resolution (LR) counterparts.

Only the training and validation sets will be released **during the first phase (model construction period)**, and the HR and LR 360° image or video pairs are available for different tracks.

**Note that the participants can use additional data, and the model size is not restricted.**

**During the second phase (testing period)**, the testing set containing only LR 360° images/videos will be released.The super-resolved results should be submitted by the participants and then evaluated by the organizers with **the quantitative metrics**.

## *Datasets*

### **Flickr360**

This is a new 360° image dataset, which contains about 3150 ERP images with a resolution **larger than 5k**. Specifically, 3100 images are collected from Flickr, and the other 50 images are captured by Insta360° cameras.The image contents vary both indoors and outdoors. We first downsample the original images into **2k resolution (2048 x 1024), serving as HR images**. These HR images are further downsampled into **LR images**. The data partition is shown in the following table.

![Untitled](Image%20SR%20Challenges%20in%20NTIRE%202023/Untitled%205.png)

### Download

Google Drive：[https://drive.google.com/drive/folders/1lDIxTahDXQ5w5x_UZySX2NOes_ZoNztN](https://drive.google.com/drive/folders/1lDIxTahDXQ5w5x_UZySX2NOes_ZoNztN)

腾讯微云：[https://share.weiyun.com/6p2fsaxO](https://share.weiyun.com/6p2fsaxO)

### Metric

We evaluate the super-resolved 360° images by comparing them to the ground truth HR ERP images. To measure the **fidelity**, we adopt the widely used **Weighted-to-Spherically-uniform Peak Signal to Noise Ratio (WS-PSNR)** as the quantitative evaluation metric.

### **Scripts**

We provide some useful scripts:

- WS-PSNR evaluation
- sub-image cropping
- dataset loader

## *Demand*

1. We **do not** restrict competitors from using **additional training data**. If it is used, it is necessary to indicate the source and amount.
2. We **do not** restrict competitors from using **pretrained networks**. If it is used, it is necessary to provide details.
3. We **do not** restrict the **model size and running time**. Please provide them in the final submission.

# ****Light Field Image Super-Resolution Challenge****

[GitHub - The-Learning-And-Vision-Atelier-LAVA/LF-Image-SR at NTIRE2023](https://github.com/The-Learning-And-Vision-Atelier-LAVA/LF-Image-SR/tree/NTIRE2023)

## *Important Date*

![Untitled](Image%20SR%20Challenges%20in%20NTIRE%202023/Untitled%206.png)

## ***Description***

The objective of this challenge is to reconstruct HR LF images from their LR counterparts.Since both intensity and directions of light rays are recorded by LF cameras, the resolution of LF images can be enhanced by using these additional angular information. LF image super-resolution (SR), also known as LF spatial SR, aims at reconstructing high-resolution (HR) LF images from their low-resolution (LR) counterparts.

## *Datasets*

### Training Set**: *[[Baidu Drive](https://pan.baidu.com/s/1mYQR6OBXoEKrOk0TjV85Yw) (key:7nzy) or [OneDrive](https://stuxidianeducn-my.sharepoint.com/:f:/g/personal/zyliang_stu_xidian_edu_cn/EpkUehGwOlFIuSSdadq9S4MBEeFkNGPD_DlzkBBmZaV_mA?e=FiUeiv)]***

Follow the set in paper [DistgSSR](https://yingqianwang.github.io/DistgLF/) ,and uses the EPFL, HCInew, HCIold, INRIA and STFgantry datasets which totally consist of **144 scenes for training.**All the LF images in the training set have an angular resolution of 9x9. The participants can use these HR LF images as groundtruths, and use the [BasicLFSR toolbox](https://github.com/ZhengyuLiang24/BasicLFSR) to train their models.

*Datasets Structure*

![Untitled](Image%20SR%20Challenges%20in%20NTIRE%202023/Untitled%207.png)

**BasicLFSR is a PyTorch-based open-source and easy-to-use toolbox for Light Field (LF) image Super-Ressolution (SR). This toolbox introduces a simple pipeline to train/test your methods, and builds a benchmark to comprehensively evaluate the performance of existing methods.**

NOTE:**External training data or pretrained models are NOT allowed in this challenge.**

### Validation Set:***[[Baidu Drive](https://pan.baidu.com/s/1n6TPP7EJlkKPMn-0DkN10g) (key:lfsr) or [OneDrive](https://stuxidianeducn-my.sharepoint.com/:f:/g/personal/zyliang_stu_xidian_edu_cn/Es3gi3N9XuVPpm8a9pysMGcB2-Pxenr5zo0WZXRaz_SaaA?e=1I840e)]***

A new validation set consisting of 16 synthetic scenes rendered by the 3DS MAX software and 16 real-world images captured by a Lytro ILLUM camera.We downsampled original LF images in the validation set by a factor of 4, and provide **LR LF images** with an angular resolution of 5x5.

### Test Set:

A new test set consisting of 16 synthetic scenes rendered by the 3DS MAX software and 16 real-world images captured by a Lytro ILLUM camera. Only 4× bicubically downsampled LR LF images with an angular resolution of 5x5 will be provided.

NOTE:**It should be noted that the images in both the validation and the test sets (even the LR versions) cannot be used for training.**

## *Metrics*

We evaluate the submitted results by comparing them with the ground truth LF images.

To measure the fidelity, we use the **standard Peak Signal to Noise Ratio (PSNR)** and, complementarily, the **Structural Similarity (SSIM)** index as they are often employed in the literature. PSNR and SSIM implementations can be found in the [BasicLFSR toolbox](https://github.com/ZhengyuLiang24/BasicLFSR)
R***ank the submissions according to the average PSNR values.The SSIM metrics will not affect submission rankings but will be used to review the strengths and weaknesses of suggested methods in the final challenge report.***

## *Baseline*

**LF-InterNet** is used as a baseline model and the submitted results should be at least on par with LF-InterNet. The solutions with PSNR values **lower than LF-InterNet** will not be ranked in the leaderboard.

![Untitled](Image%20SR%20Challenges%20in%20NTIRE%202023/Untitled%208.png)

# **Efficient Super-Resolution Challenge**

## *Important Dates*

![Untitled](Image%20SR%20Challenges%20in%20NTIRE%202023/Untitled%209.png)

## *Description*

The aim is to devise a network that reduces one or several aspects such as **runtime, parameters, FLOPs, activations, and depth** of RFDN ([https://arxiv.org/pdf/2009.11551.pdf](https://arxiv.org/pdf/2009.11551.pdf)) while **at least maintaining PSNR of 29.00dB** on validation datasets.

NOTE:T**he final ranking and challenge winners we are weighing more the teams/participants improving in more than one aspect (runtime, parameters, FLOPs, activations, depths) over the provided reference solution.**

**Please refer to [1] (https://arxiv.org/pdf/2205.05675.pdf), [2] (https://arxiv.org/pdf/2009.06943), and [the testing code](https://github.com/ofsoundof/NTIRE2022_ESR) for more details.**

[1] Li, Yawei, et. al, "NTIRE 2022 challenge on efficient super-resolution: Methods and results." CVPR *Workshops,* 2022.

[2] Zhang, Kai, et al. "AIM 2020 challenge on efficient super-resolution: Methods and results." *ECCV Workshops,* 2020.

# ****Stereo Image Super-Resolution Challenge****

[GitHub - The-Learning-And-Vision-Atelier-LAVA/Stereo-Image-SR at NTIRE2023](https://github.com/The-Learning-And-Vision-Atelier-LAVA/Stereo-Image-SR/tree/NTIRE2023)

## *Important Dates*

![Untitled](Image%20SR%20Challenges%20in%20NTIRE%202023/Untitled%2010.png)

## *Description*

Aim at establishing a benchmark for stereo image SR, and aspire to highlight the specific challenges and research problems faced by stereo image SR.

**THREE TRACKS**

- **Track1**:[Fidelity & Bicubic](https://codalab.lisn.upsaclay.fr/competitions/10047)

The aim of this track is to obtain SR results with the highest ***fidelity score*** (i.e., *PSNR*) under **standard Bicubic degradation.**

**Only PSNR is used for ranking.**

- **Track2**:[Perceptual & Bicubic](https://codalab.lisn.upsaclay.fr/competitions/10048)

The aim of this track is to obtain SR results with the highest ***perceptual score*** (i.e., *LPIPS*) with promising stereo consistency under standard Bicubic degradation.

**The final score is calculated as:**

![Untitled](Image%20SR%20Challenges%20in%20NTIRE%202023/Untitled%2011.png)

- **Track3**:[Fidelity & Realistic](https://codalab.lisn.upsaclay.fr/competitions/10049)

The aim of this track is to obtain SR results with the highest ***fidelity score*** (i.e., *PSNR*) under **complex realistic degradations**.

**Only PSNR is used for ranking.**

## *Datasets*

### Training Set: ***[[download the training data](https://www.jianguoyun.com/p/DbtNUkIQstPqChiWv-wEIAA)]***

The 800 stereo images in training set of the **[Flickr1024 dataset](https://yingqianwang.github.io/Flickr1024/)** are used as the training set of this challenge.

**NOTE:**

- **External dataset is NOT allowed in this challenge.**
- **Models pretrained on other datasets are NOT allowed in this challenge.**

### Testing Set:***[[download the validation data](https://www.jianguoyun.com/p/DbtNUkIQstPqChiWv-wEIAA)]***

The 112 stereo images in the validation set of the [**Flickr1024 dataset](https://yingqianwang.github.io/Flickr1024/)** are used as the validation set of this challenge.

**NOTE: The validation set should be used for validation purpose only but cannot be used as additional training data.**

### ***Flickr1024 is a large-scale stereo image dataset which consists of 1024 high-quality image pairs and covers diverse senarios.***

![Untitled](Image%20SR%20Challenges%20in%20NTIRE%202023/Untitled%2012.png)