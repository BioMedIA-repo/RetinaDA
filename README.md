
# RetinaDA

## Project Overview

This project aims to process image files to generate usable patches; perform a series of image processing operations on images, including rotation, flipping, and cropping. The processed images will be saved in the specified output directory.

## Paper Links

Paper describing this work has been published in Frontiers of Computer Science (FCS) special column “Code & Data”.
Cited as:  Fei GUO, Shaojia YANG, Rui GE, Wenjuan LI, Aihong LU, Rongzhen FENG, Wu FANG, Qiangguo JIN. RetinaDA: a diverse dataset for domain adaptation in retinal vessel segmentation. Front. Comput. Sci., 2025, 19(8): 198917 https://doi.org/10.1007/s11704-024-41114-1

## Feature Description

1. **Format Conversion**: Convert images from GIF or TIF formats to PNG format.
2. **Image Processing**:
   - Rotation: Randomly rotate images by 0 to 360 degrees.
   - Flipping: Randomly decide whether to flip the image along the vertical axis.
   - Cropping: Randomly crop the image based on the center point of the image.

## Source Directory

This directory contains the code, file of outputs, and documentation for image processing.

### Files

- [LICENSE](./LICENSE/): Specify the usage permissions of developers or organizations using the code.
- [README.md](./README.md/): Contains a basic introduction to this project.
- [Sub_image.py](./Sub_image.py/): Process image files to generate usable patches.
### Subfolders

- [RentinaDA](./RentinaDA/): Contains the processed images.


## Usage Instructions

### Environment Requirements

- Python 3.x
- NumPy
- OpenCV
- Pillow
- cv2

### Steps to Run

1. Set the `input_dir1` and `input_dir2` variables to point to the directories containing the images to be processed, where the center point will be generated based on the path of `input_dir1`; image files are preferred.
2. Set the `output_dir1` and `output_dir2` variables to point to the directories for saving the processed images.
3. Run the code to automatically process the images in the specified directories and save them to the output directories.

### Code Structure

- `convert_to_png`: Convert GIF or TIF format images to PNG format.
- `is_convertible`: Check if the image is in GIF or TIF format.
- `process_image`: Perform rotation, flipping, and cropping on the image.
- `get_file_name_without_extension`: Get the file name without the extension.
- `files1` and `files2`: Construct dictionaries containing file names and paths.
- `centers`: Store the center coordinates of each image.
- `common_files`: Obtain the common file names in two input directories.

### Parameter Description

- `execution_count`: The number of times the image processing is executed.
- `current_index`: Used to name the output directory.
- `photo_index`: Used to name the output files.
- `size_range`: The minimum and maximum size range for cropping images.

## Output Directory Structure

The output directory is named in the format `YourImagePath\YourImageName_{current_index}`, where `current_index` will be counted automatically, and the patches generated from the same original image will be numbered. Each output directory will contain the processed images.

## Result Dataset
The data structure should be like this:

	/Retina
		/CHASDB
			/1st_manual
				/Image_01L_1
				/Image_01L_2
				...
			/images
				...
		/DRIVE
			/1st_manual
			    ...
			/images
				...
		... 




## Precautions

- Ensure that the image formats in the input directory are correct and that the output directory has enough space to store the processed images.
- Replace `YourImagePath` and `YourImageName` in the script with the actual path and name.
- Adjust `size_range` and `execution_count` in the script as needed.

## Version History

- Initial version: October 17, 2024

## Contact Information

If you have any questions or need further assistance, please contact us via [Contact Information](mailto:1052886267@qq.com).
