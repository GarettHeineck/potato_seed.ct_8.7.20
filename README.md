# potato_seed.ct_8.7.20
 
## Project information
### 1. This project demonstrates how to use R to quantify potato seeds imaged on a flatbed scanner.  
   1. Three example half-sib potato seed lots were images.
   1. These are saved as JPGs in the 'original images' folder.

| Original Image | 
|------------|
![Example Oringal Image](https://github.com/GarettHeineck/potato_seed.ct_8.7.20/blob/master/original_img/PA99N2-1__Innovator__4.jpg)


### 2. A simple data sheet is included in the 'results' folder.  
   1. The data sheet contains important information to validate the computer output.
   1. Variables were collected manually on the number of seeds in each image.
   
   
### 3. Several training data csv files are included in the 'training data' folder.  
   1. Collectively, these mixes (csv files) make up the training palette for this project.
   1. The training palette is used to fit random forest models.
   1. The training palette can be expanded or shrunk by adding or subtracting mixes.
   1. New mixes can be made easily in ImageJ using the original images (SEE MODULE ON MAKING TRAINING DATA).
   1. Mixes can be subtracted by removing the files after downloading or using R.


## Setup
1. Start by downloading the ZIP file with all documents.
1. Save these documents in a folder called 'grass.leaf_rust.detection_2.26.19'
1. NOTE: if you do not use this file name it will take a little more work to run the R script.
1. Open the R file in R studio.
1. Go through each required package and download or update packages if needed.
1. Update R if you have not done so recently.
1. In the R file go to line 41 and change the object file path to wherever your 'potato_seed.ct_8.5.20' folder is located.
1. The script should run and conduct the following tasks:
   1. Create new folders within 'potato_seed.ct_8.5.20'.
   1. Build two random forest models to detect seeds.
   1. Operate image analysis using the models and EBImage functions.
   1. Output and save a summary data file.
   1. Conduct a few basic visualizations in ggplot.


## Result of Step 1

| Cropped and Masked Image | 
|------------|
![Cropped and Masked Image](https://github.com/GarettHeineck/potato_seed.ct_8.7.20/blob/master/S1_foreground_classify/S1_PA99N2-1__Innovator__4.jpg)


## Result of Step 2
| Adaptive Thresholding and RGB Overlay | 
|------------|
![Adaptive Thresholding and RGB Overlay](https://github.com/GarettHeineck/potato_seed.ct_8.7.20/blob/master/S2_foreground_overlay/S2_PA99N2-1__Innovator__4.jpg)


## Result of Step 3
| Watershed Transformation | 
|------------|
![Watershed Transformation](https://github.com/GarettHeineck/potato_seed.ct_8.7.20/blob/master/S3_foreground_watershed/S3_PA99N2-1__Innovator__4.jpg)


## Validation
| Linear Regression (n=4) | 
|------------|
![Watershed Transformation](https://github.com/GarettHeineck/potato_seed.ct_8.7.20/blob/master/results/potato%20seed%20count_01.jpeg)
