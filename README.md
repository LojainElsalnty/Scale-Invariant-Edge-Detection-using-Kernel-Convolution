# 📐 Scale-Invariant Edge Detection using Kernel Convolution  

## 📌 Overview  
This project focuses on **scale-invariant edge detection**, where different kernel sizes are applied to an image to analyze their impact on feature detection accuracy. The edge detection method is based on first-derivative convolution using **x and y directional kernels**. The results include a **magnitude map** and a **kernel size map**, which provide insights into how different kernel sizes affect edge sharpness.  

## 🔍 How It Works  
The edge detection process involves:  
1. **Generating Partial Differential Kernels**:  
   - The kernel structure follows a pattern of `{ -1, 0, 1 }` values.  
   - **X-direction kernel**: Middle row contains 0s, top half is -1, and bottom half is 1.  
   - **Y-direction kernel**: Middle column contains 0s, left half is -1, and right half is 1.  
2. **Applying Multiple Kernel Sizes**:  
   - Kernels of size **3x3 to 13x13** (in odd increments) are applied at each pixel.  
   - Convolution is performed for both x and y directions.  
3. **Computing Edge Magnitude**:  
   - Magnitude at each pixel is calculated as:  
     \[
     \text{Magn}(I(i,j)) = \sqrt{(I_x)^2 + (I_y)^2}
     \]  
4. **Applying Thresholding**:  
   - A cutoff threshold **t** is applied to filter weak edges.  
5. **Output Generation**:  
   - **Magnitude Map**: Displays the edge strength across the image.  
   - **Kernel Size Map**: Shows the most effective kernel size for each pixel.  

## 🚀 Technologies  
- Python  
- NumPy  
- OpenCV  

## 📅 Course  
**DMET 901 – Computer Vision (Winter 2024)**  

## 🎯 University  
**German University in Cairo**  

## 📜 Assignment Details  
- **Due Date**: December 3rd, 2024, 11:59 PM  
- **Assignment #2** for Computer Vision course.  

## 🛠️ Implementation  
To implement this edge detection method, create a function with the following inputs:  
- `I`: The input image.  
- `s`: Maximum kernel size (odd values from `3x3` to `s x s`).  
- `t`: Cutoff threshold for edge detection.  

The function should output:  
1. **Magnitude Map** (M)  
2. **Kernel Size Map** (S)  

## 📷 Example Output  
An example visualization of the magnitude and kernel size maps will be included after implementation.  

---

This repository provides an **experimental approach to edge detection** and allows for analysis of **kernel-dependent feature detection** in images. 🚀  
