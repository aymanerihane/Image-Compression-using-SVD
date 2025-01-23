# SVD-Based Image Compression

This repository implements **image compression** using **Singular Value Decomposition (SVD)**, a linear algebra technique to reduce the dimensionality of an image while retaining its essential features. This approach demonstrates how to reconstruct images with fewer singular values, balancing compression and quality.

---

## Features

- **Load and preprocess images**: Supports input in grayscale or processes individual color channels for color images.
- **SVD decomposition and reconstruction**: Decomposes the image matrix and reconstructs it using a reduced number of singular values.
- **Visualization**: Displays the original and compressed images side by side to analyze the quality trade-off.
- **Quality vs Compression Trade-off**: Allows experimentation with varying numbers of singular values to observe effects on size and quality.

---

## Getting Started

### Prerequisites

- Python 3.7+
- Libraries:
  - `numpy`
  - `matplotlib`
  - `Pillow` (for image handling)

Install required packages using pip:
```bash
pip install numpy matplotlib pillow
```

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/aymanerihane/svd-image-compression.git
   ```
2. Navigate to the project directory:
   ```bash
   cd svd-image-compression
   ```

---

## Usage

1. Place your image file in the project directory (e.g., `image.png`).
2. Run the script:
   ```bash
   python svd_compression.py
   ```
3. Follow the prompts to:
   - Specify the image path.
   - Choose the number of singular values to retain for compression.
4. The compressed image and a side-by-side comparison will be displayed and saved in the output directory.

---

## Example

### Original Image
![Original Image](./image.png)

### Compressed Image (100 Singular Values)
![Compressed Image](./outputs/compressed_image_100k.png)

---

## How It Works

1. **Load Image**: The image is read as a matrix of pixel values (grayscale or color).
2. **Apply SVD**: Decomposes the matrix into three components:
   - U (left singular vectors)
   - Σ (singular values)
   - V^T (right singular vectors)
3. **Reconstruct Image**: Recombine the matrices using a reduced number of singular values to approximate the original image.
4. **Save and Visualize**: Outputs the compressed image and displays the comparison.

---

## Folder Structure

```
svd-image-compression/
|-- image.png          # Example input image
|-- svd_v2.py       # Main script
|-- outputs/
    |-- compressed_image_100k.png # Output compressed image
|-- README.md                # Documentation
```

---

## Contributions

Contributions are welcome! Feel free to open an issue or submit a pull request.

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

## Acknowledgments

- Linear algebra concepts from **[NumPy Documentation](https://numpy.org/doc/)**.
- Image handling inspired by **Pillow** tutorials.

