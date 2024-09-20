

# Image Augmentation Script

## Description
This Python script automates the process of augmenting images by performing a series of transformations such as rotation and flipping. The augmented images are saved in a folder called `HR_DATA` with different variations like rotations (90°, 180°, 270°) and flips (left-right and top-bottom).

## Table of Contents
- [Installation](#installation)
- [Execution Process](#execution-process)
- [Obtaining Results](#obtaining-results)
- [License](#license)

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/image-augmentation.git
   ```

2. **Install dependencies**:
   Ensure `Pillow` (the Python Imaging Library) is installed. You can install it via pip:
   ```bash
   pip install Pillow
   ```

3. **Setup directories**:
   Ensure that you have the `data` directory with the images to augment, and the script will create an `HR_DATA` directory to store the augmented images.
   ```bash
   mkdir data HR_DATA
   ```

## Execution Process

Follow these steps to run the image augmentation script:

1. **Prepare Input Images**:
   - Place all the images you want to augment in the `data/` folder. These images will be used as input for the augmentation process.

2. **Run the Script**:
   - Execute the Python script. The code will process all images inside the `data/` directory and save the augmented images to the `HR_DATA/` directory.
   ```bash
   python augment_images.py
   ```

3. **Script Details**:
   The script performs the following operations on each image:
   - Opens the image using the Python Imaging Library (`PIL`).
   - Rotates the image by 90°, 180°, and 270°.
   - Applies horizontal (left-right) and vertical (top-bottom) flips to the original and rotated images.
   - Saves the augmented images in the `HR_DATA/` directory.

## Obtaining Results

After running the script, the augmented images will be saved in the `HR_DATA/` folder. Here's how the results will be organized:

1. **Original Image**:
   - A copy of the original image is saved in the `HR_DATA/` folder with the same name as the original.

2. **Augmented Images**:
   - The augmented images are named based on the transformations applied:
     - **Rotation by 90°**: `<idx>_90.png`
     - **Rotation by 180°**: `<idx>_180.png`
     - **Rotation by 270°**: `<idx>_270.png`
     - **Flipped Horizontally (Left-Right) after Rotation**:
       - `<idx>_90_lr.png`, `<idx>_180_lr.png`, `<idx>_270_lr.png`
     - **Flipped Vertically (Top-Bottom) after Rotation**:
       - `<idx>_90_tb.png`, `<idx>_180_tb.png`, `<idx>_270_tb.png`

### Example Process:

For an image placed in `data/` named `image1.png`:

1. **Original**:
   - A copy of `image1.png` is saved in the `HR_DATA/` folder.

2. **Rotation**:
   - `image1_90.png` (rotated 90°)
   - `image1_180.png` (rotated 180°)
   - `image1_270.png` (rotated 270°)

3. **Flips**:
   - `image1_90_lr.png` (rotated 90° and flipped horizontally)
   - `image1_90_tb.png` (rotated 90° and flipped vertically)
   - `image1_180_lr.png` (rotated 180° and flipped horizontally)
   - `image1_180_tb.png` (rotated 180° and flipped vertically)
   - `image1_270_lr.png` (rotated 270° and flipped horizontally)
   - `image1_270_tb.png` (rotated 270° and flipped vertically)

All these files will be saved in the `HR_DATA/` folder for further use or analysis.

## License

This project is licensed under the MIT License.

---

This provides a clear, point-wise explanation of the execution process and how to collect the results after running the script. Let me know if you need any additional information!
