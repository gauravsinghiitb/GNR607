# PAN Fusion: Fusing Multispectral and Panchromatic Images Using the RGB-HSI Method

## Problem
Multispectral images often have lower spatial resolution compared to panchromatic (PAN) images. This discrepancy limits the usability of multispectral images in high-precision applications, where spatial resolution is critical. 

## Objective
The objective of this project is to create a method that fuses PAN and multispectral (MS) images to improve the spatial resolution of the MS images without compromising their spectral integrity. The fusion is performed using the RGB-HSI color model to incorporate both spatial and spectral information.

## Method Overview
The fusion process is based on the following steps:

1. **RGB to HSI Conversion**: Multispectral images are first converted from RGB to the HSI (Hue, Saturation, Intensity) color space.
    - **Hue (H)**: Represents color information.
    - **Saturation (S)**: Describes color intensity.
    - **Intensity (I)**: Represents brightness (spatial details).

2. **Panchromatic Image Integration**: The PAN image replaces the intensity (I) channel in the HSI space. The intensity channel controls the spatial details, so replacing it with the high-resolution PAN image improves the spatial sharpness.

3. **HSI to RGB Conversion**: After the PAN image has been integrated into the HSI space, the modified HSI data is converted back into RGB to produce the final fused image.

## Steps to Achieve Image Fusion

1. **Dataset Collection and Processing**: Collect and preprocess the multispectral (MS) and panchromatic (PAN) images.
2. **Convert the Multispectral Image to HSI**: Convert the input multispectral image from RGB to HSI color space.
3. **Replace the Intensity Channel with the PAN Image**: Replace the intensity (I) component of the HSI with the PAN image to enhance spatial resolution.
4. **Reconstruct the Image**: Convert the modified HSI data back into RGB.
5. **Convert the Resulting Image to 8-Bit Format**: Convert the fused image into an 8-bit format for proper display and analysis.

## Python Libraries Used

- **OpenCV**: For image reading, conversion, and processing.
- **NumPy**: For matrix operations and numerical computations.
- **Matplotlib**: For visualizing the images.

## Key Functions

- `rgb_to_hsi()`: Converts RGB image to HSI.
- `hsi_to_rgb()`: Converts HSI image back to RGB.
- `fuse_images()`: Main function to fuse multispectral and panchromatic images.

## Challenges

- **Memory Management**: Handling large images requires efficient memory management to avoid system slowdowns.
- **Large Image Size**: Processing large images can be computationally expensive and may require high-performance hardware.

## Results

The RGB-HSI fusion method effectively enhances the spatial resolution of multispectral images while preserving their spectral content. This fusion method is useful for applications that require high spatial resolution, such as:

- Land-use classification
- Change detection in satellite imagery
- Environmental monitoring

### Benefits

- **Improved clarity and sharpness** in the fused image.
- **Preserved spectral integrity** of the multispectral image.
- Useful for applications requiring high-resolution imagery.

### Limitations

- Computationally expensive for **very large images**.
- Potential **blurring** in certain areas, which may reduce fine detail when the spatial resolution is significantly enhanced.

## Example Usage

To use this method in your own project:

1. Place your PAN and MS images in the working directory.
2. Load the images using OpenCV.
3. Call the `fuse_images()` function to generate the fused image.
4. Display or save the resulting fused image.

## Authors

- ** @gauravsinghiitb 22B0668**
- **@sg0701 22B0667**

## Acknowledgments
- OpenCV  
- NumPy  
- Matplotlib
- QGIS
- usgs eartg explorer  

