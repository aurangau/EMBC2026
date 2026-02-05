# Supplementary Material for EMBC2026
Supplementary Material for IEEE EMBC 
**Structural Loss Functions Enhance Super-Resolution Performance with Mixed MRI and Non-Domain Training Data** <br />
Authors: <samp>{aurangau, friedrich.wetterling, anil.kokaram}@tcd.ie</samp>

## Abstract
Magnetic Resonance Imaging (MRI) is an important tool for detecting medical conditions. Although low-field MRI scanners enable quick acquisition, resulting images are low resolution and blurry and noisy, requiring sophisticated upsampling methods. Deep Learning (DL) methods offer cost efficient, quick and high quality solutions. However, the impact of training data on brain MRI restoration quality, directly affecting diagnostic reliability remain under-explored. We explored different combinations of MRI and natural world images as part of the training data for DL-based methods aimed at upsampling Low-Resolution MRI scans by factors of 2 and 4. We showed that training lightweight Deep Neural Networks (DNNs) using only MRI scans significantly improved overall restoration quality measured by Peak Signal-to-Noise Ratio (PSNR), but not sharpness, leading us to examine the role of loss functions for generating sharper restorations. We designed and trained a lightweight U-Net based Super-Resolution (SR) architecture with widely used losses, i.e. Mean Squared Error (MSE), Mean Absolute Error (MAE) and Structural Similarity (SSIM) and incorporated a sharpness loss Q, originally designed for deblurring, but not MRI SR. We showed that incorporating such losses that explicitly target sharpness, not only led to visibly sharper restorations, but also to gains in overall quality of upsampled MRI.


## Impact of Domain Specific Data on Training Performance
Table 1 shows the restoration capabilities, in terms of PSNR, SSIM, LPIPS and Q. The total number of images used was 27,547 crops of size 256 $\times$ 256. 

| Percent | PSNR | SSIM | 
| ------- | ---- | ---- | 
| 0       | A    |  C   |
