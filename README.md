# SVD-Image-Compression

This repository contains Python code that implements various linear algebra algorithms and techniques for image compression.

# Table of Contents
1. Compressing Images using Singular Value Decomposition (SVD)
2. Rayleigh Iteration Method and Power Iteration Method
3. Batch Compression of Images
4. Dependencies
5. Usage

# 1: Compressing Images using Singular Value Decomposition (SVD)
The compress_image function takes an image file path and compresses it using Singular Value Decomposition (SVD). It separates the color channels (R, G, B), performs SVD for each channel, keeps only the specified number of components, and reconstructs the compressed image. The function also calculates and displays the original and compressed images, along with the compression ratio and relative error.

Example usage:

python
Copy code
compress_image('/path/to/image.jpg', num_components=50)
# 2: Rayleigh Iteration Method and Power Iteration Method
This section includes implementations of the Rayleigh Iteration Method and the Power Iteration Method for finding eigenvalues and eigenvectors of a matrix.

Example usage:

python
Copy code
np.random.seed(100)
A = np.random.random((3, 3))
U, S, Vt = svd(A)

print("U :", U)
print("S :", S)
print("Vt :", Vt)
# 3: Batch Compression of Images
The code in this section compresses multiple images in batch using the compress_image function with varying numbers of components. It displays the original and compressed images for each iteration, along with the compression ratio and relative error.

Example usage:

python
Copy code
for i in range(2, 50, 5):
    compress_image('/path/to/image.jpg', i)
# Dependencies
The code relies on the following libraries:

NumPy
PIL (Pillow)
Matplotlib
Install these dependencies using:

bash
Copy code
pip install numpy pillow matplotlib
# Usage
Clone the repository.
Install the dependencies.
Run the Python scripts to execute the algorithms and compress images.
