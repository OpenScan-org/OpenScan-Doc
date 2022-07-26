# 3D Scan Quality

![benchy2](https://user-images.githubusercontent.com/57842400/180952908-b2f9c24c-ff4f-45c5-88a3-81d788e9ca20.jpg)

## Overview

all scans shown here are raw scans without any post-processing. Scaling was done using either a reference measurement or ICP fine registration using the free software [CloudCompare](https://www.danielgm.net/cc/)

## Scaling

An inherent challenge of photogrammetry 3d scanning is, that the resulting 3D models will not come with an accurate scale. Therefore, it is always(\*) necessary to scale the model using a reference measurement. Note, that this is an additional step, which is not needed for most other scanners.

(\*) the only way to circumvent this issue, is automatic scaling using either known camera positions and/or the use of markers.


## Mesh accuracy

![image (5)](https://user-images.githubusercontent.com/57842400/180953303-3a1acb96-48fe-45e4-ba63-06793a9a11b0.png)

![image](https://user-images.githubusercontent.com/57842400/180955295-b7aca6b8-cc03-41ad-8a8f-cf9362ae2365.png)


## Mesh Resolution

It is possible to resolve even finest features. In the following mesh you can see some surface patterns. Those vertical lines result from the printing process (MSLA) and correspond to the pixel size of the 3d printers screen.

![untitled](https://user-images.githubusercontent.com/57842400/180953193-eeb2c45b-7ca6-4349-9d44-a461deae9081.jpg)

## Texture 

![image (4)](https://user-images.githubusercontent.com/57842400/180952642-80116835-a82f-4c39-9b97-c5f2a1ac09c2.png)

## Comparing different cameras


* Left - OpenScan Mini with Pi Camera v2.1 (8mp)
* Right - OpenScan Mini with Arducam IMX519 (16mp) and autofocus
* 
![image (1)](https://user-images.githubusercontent.com/57842400/180953121-355afa76-2e25-45de-8287-d05b71a3a916.png)


## Comparison with other scanners


* Left - OpenScan Mini with Pi Camera v2.1 (8mp)
* Right - Thunk 3D Cooper M20

![Benchy Fuji vs Thunk](https://user-images.githubusercontent.com/57842400/180952879-106a5235-3fc3-49f9-9ed4-155d775703a4.png)

![Benchy Fuji vs Thunk histo](https://user-images.githubusercontent.com/57842400/180953091-08b1e68b-1a86-436e-b4c2-eed9c5208ff4.jpg)



