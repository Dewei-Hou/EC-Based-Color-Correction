# Color Correction for Multiple Images via Error Compensation-Based Fusion Approach
"Color Correction for Multiple Images via Error Compensation-Based Fusion Approach" by Kuo-Liang Chung and Te-Wei Hou.

## Introduction
![flowchart](https://github.com/user-attachments/assets/24eb70bb-28d9-49fd-8006-f3d13647a7e3)


Color correction for multiple images.

An example of our algorithm effects is demonstrated below:
![alt text](sample.png)


## Dependencies
+ C++ 17
+ OpenCV 4.7.0
+ OpenMP (optional)

## Environments
+ Intel Core i5-12400 CPU clocked at 2.5 GHz, 16 GB RAM
+ Microsoft Windows 11 64-bit operating system
+ Microsoft Visual Studio 2022

## Configuration & Run Tests
The project can be configured by CMake with the given CMakeLists.txt file.
Four input directories are required for program execution:
+ "aligned_result": The aligned images obtained after applying an existing method. The image file "XX__warped_img.png" represents the aligned image for XX.
+ "overlap" : The overlapping areas of the aligned images in "aligned_result". The image file "XX__YY__overlap.png" represents the overlapping area between images XX and YY. ("YY__XX__overlap.png" is the same as "XX__YY__overlap.png").
+ "correspondence" : The matching feature points of the aligned images in "aligned_result". The CSV file "XX__YY_inliers.csv" contains the x-y coordinates of the matching feature points on images XX and YY.
+ "img_masks" : The masks of the images after alignment. The image file "mask_XX.png" represents the mask for the aligned image "XX__warped_img.png".

Two output directories are required for saving the color corrected results:
+ "Ours": The color corrected images of "aligned_result" are saved in this directory.
+ "result": The color corrected aligned multiple images of "Ours" is saved in this directory.

All 30 testing multiple images and the qualitative quality results are available at https://drive.google.com/drive/u/3/folders/1avBu1zL5PUl8SsLXG1Ot4XWGgcLRKw4t

## Contact
If you have any questions, please email us via

Te-Wei Hou: deweihou123@gmail.com

Kuo-Liang Chung: klchung01@gmail.com
