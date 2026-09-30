# computer-vision-Bitplane-Slicing

## Overview

This project demonstrates **Bit Plane Slicing**, an image processing technique used to separate a grayscale image into its individual bit planes. Each pixel in an 8-bit grayscale image is represented by 8 bits, and bit plane slicing extracts each of these bits to analyze the contribution of different bit levels to the image.

## Objective

- Read a grayscale image.
- Extract all 8 bit planes (0–7).
- Visualize the original image and its bit planes.
- Understand how image information is distributed across different bits.

## Technologies Used

- Python
- OpenCV (cv2)
- NumPy
- Matplotlib

## Requirements

Install the required libraries:

```bash
pip install opencv-python numpy matplotlib
```

## Project Structure

```text
Bit-Plane-Slicing/
│
├── bit_plane_slicing.ipynb
├── image16.jpg
├── output.png
└── README.md
```

## Methodology

1. Load the image in grayscale mode.
2. Extract individual bit planes using bitwise operations.
3. Convert extracted bits into visible images.
4. Display the original image and all bit planes.

### Bit Plane Extraction Formula

```python
bit_plane = (img >> k) & 1
```

where:

- `img` = grayscale image
- `k` = bit position (0 to 7)

## Code Snippet

```python
for k in range(8):
    bit_plane = (img >> k) & 1
    visible_plane = bit_plane * 255
```

## Output

The program displays:

- Original grayscale image
- Bit Plane 0 (Least Significant Bit)
- Bit Plane 1
- Bit Plane 2
- Bit Plane 3
- Bit Plane 4
- Bit Plane 5
- Bit Plane 6
- Bit Plane 7 (Most Significant Bit)

### Output Image

![Bit Plane Slicing Output](output.png)

## Results

The higher-order bit planes, especially **Bit Plane 7 and Bit Plane 6**, contain more of the major visual structure of the image, while lower-order bit planes mainly contain finer image information.

## Applications

- Image Compression
- Image Enhancement
- Watermarking
- Pattern Recognition
- Medical Image Analysis
- Digital Forensics

## Conclusion

Bit Plane Slicing is a useful image processing technique for analyzing the significance of different bits in an image. It helps in understanding image representation and is widely used in image compression, enhancement, and digital image analysis.

## Author

**M. Avinash**
