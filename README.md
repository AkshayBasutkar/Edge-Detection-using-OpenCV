# Edge-Detection-using-OpenCV
This Python code applies **Canny** and **Marr-Hildreth** edge detection to an image, then displays the original and processed images using **Matplotlib** for comparison. It uses **OpenCV** for image processing and **NumPy** for numerical operations.


# Edge Detection using Canny and Marr-Hildreth

This repository contains a Python script that performs edge detection on an input image using two different techniques: **Canny Edge Detection** and **Marr-Hildreth Edge Detection**. The results of both methods are visualized alongside the original image for easy comparison.

## Features
- Loads an image from a file and converts it to grayscale.
- Applies **Canny Edge Detection** to highlight edges in the image.
- Applies **Marr-Hildreth Edge Detection** using the Laplacian filter.
- Displays the original image, the edge-detection results, and the final output images in a 2x3 grid format for comparison.
- Uses **Matplotlib** to visualize and compare the results.

## Requirements

Before running the script, ensure you have the following Python libraries installed:

- **OpenCV**: For image processing.
- **NumPy**: For numerical operations.
- **Matplotlib**: For visualization.

You can install the required libraries using `pip`:

```bash
pip install opencv-python numpy matplotlib
```

## Usage

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/yourusername/edge-detection.git
   ```

2. Place the image you want to process (e.g., `img.jpg`) in the project directory.

3. Run the script `edge_detection.py`:

   ```bash
   python edge_detection.py
   ```

4. The script will process the image and display the results in a grid, including:
   - The original image.
   - The Canny edge detection result.
   - The output of the Canny method overlaid on the original image.
   - The Marr-Hildreth edge detection result.
   - The output of the Marr-Hildreth method overlaid on the original image.

## How It Works

1. **Image Loading & Preprocessing**:
   - The input image is read using OpenCV’s `cv2.imread()`.
   - The image is converted to grayscale using `cv2.cvtColor()` to simplify edge detection.

2. **Canny Edge Detection**:
   - The Canny algorithm is applied using `cv2.Canny()`. It detects edges by finding areas of rapid intensity changes in the image.

3. **Marr-Hildreth Edge Detection**:
   - The Laplacian of the grayscale image is calculated using `cv2.Laplacian()`.
   - The absolute values of the Laplacian are taken to highlight edges and then scaled to 8-bit values with `cv2.convertScaleAbs()`.

4. **Visualization**:
   - The images are displayed using **Matplotlib**. A 2x3 grid is used to show:
     - The original image.
     - The edge detection results (Canny and Marr-Hildreth).
     - The original image with the detected edges overlaid.

## Example Output

The output will look like this:

```
| Original Image | Canny Edge Detection | Canny Output Image |
|----------------|----------------------|--------------------|
| Marr-Hildreth Edge Detection | Marr-Hildreth Output Image |                |
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- This project uses **OpenCV** for image processing and **Matplotlib** for visualization.
- Special thanks to the creators of the Canny and Marr-Hildreth edge detection algorithms.

---

Feel free to modify or extend this code for your own edge detection tasks!
