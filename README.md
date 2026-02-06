# Supplementary Material for EMBC2026
Supplementary Material for IEEE EMBC 
**Structural Loss Functions Enhance Super-Resolution Performance with Mixed MRI and Non-Domain Training Data** <br />
Authors: <samp>{aurangau, friedrich.wetterling, anil.kokaram}@tcd.ie</samp>

## Abstract
Magnetic Resonance Imaging (MRI) is an important tool for detecting medical conditions. Although low-field MRI scanners enable quick acquisition, resulting images are low resolution and blurry and noisy, requiring sophisticated upsampling methods. Deep Learning (DL) methods offer cost efficient, quick and high quality solutions. However, the impact of training data on brain MRI restoration quality, directly affecting diagnostic reliability remain under-explored. We explored different combinations of MRI and natural world images as part of the training data for DL-based methods aimed at upsampling Low-Resolution MRI scans by factors of 2 and 4. We showed that training lightweight Deep Neural Networks (DNNs) using only MRI scans significantly improved overall restoration quality measured by Peak Signal-to-Noise Ratio (PSNR), but not sharpness, leading us to examine the role of loss functions for generating sharper restorations. We designed and trained a lightweight U-Net based Super-Resolution (SR) architecture with widely used losses, i.e. Mean Squared Error (MSE), Mean Absolute Error (MAE) and Structural Similarity (SSIM) and incorporated a sharpness loss Q, originally designed for deblurring, but not MRI SR. We showed that incorporating such losses that explicitly target sharpness, not only led to visibly sharper restorations, but also to gains in overall quality of upsampled MRI.


## Impact of Domain Specific Data on Training Performance
Table 1 shows the restoration capabilities, in terms of PSNR, SSIM. The total number of images used was 27,547 crops of size 256 $\times$ 256. 

| Percent | PSNR | SSIM |
| ------- | ---- | ---- |
| 0       | 35.09 | 0.96 |
| 10      | 35.10 | 0.96 | 
| 20      | 35.12 | 0.96 | 
| 30      | 35.14 | 0.96 |
| 40      | 35.29 | 0.97 |
| 50      | 35.45 | 0.97 |
| 60      | 35.09 | 0.96 |
| 70      | 35.11 | 0.96 |
| 80      | 35.04 | 0.96 |
| 90      | 34.96 | 0.96 |
| 100     | 35.74 | 0.97 |

As can be seen from the above table, as the percentage of MRI images increases, so do quality metrics such as PSNR and SSIM. Table 2 gives a more detailed overview of the use of MRI data with respect to sharpness metrics such as $Q$.

| Percent | PSNR | SSIM | LPIPS | $Q$ |
| ------- | ---- | ---- | ----- | --- |
| 0       | 35.09 | 0.96 | 0.08 | 0.12 |
| 10      | 35.10 | 0.96 | 0.08 | 0.12 |
| 50      | 35.45 | 0.97 | 0.07 | 0.12 | 
| 100     | 35.74 | 0.97 | 0.07 | 0.12 | 


