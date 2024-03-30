# Multi-Threaded-Parallel-Image-Convolution
A multi-threaded image convolution program implemented in C++

This project demonstrates a multi-threaded approach to performing image convolution operations using POSIX threads (pthreads) in C++. It aims to enhance performance by dividing the image processing workload across multiple threads.

#Installation
To compile the program, you will need a C++ compiler that supports C++11 or later and pthreads for threading support. A Makefile is included for convenience.

1.Clone this repository or download the source files.
2.Navigate to the project directory.
3.Run make to compile the program. This should produce an executable named papply_filter.

#Usage
To run the image convolution program, use the following command format:

./papply_filter <input_image_file> <mask_file> <output_image_file> <number_of_threads>

- <input_image_file>: Path to the input image file.
- <mask_file>: Path to the convolution mask file.
- <output_image_file>: Path to save the output (convolved) image.
- <number_of_threads>: The number of threads to use for processing.

Example: ./papply_filter input.txt mask.txt output.txt 4

#Input File Format

The input image and mask should be provided as text files in the following formats:

- Input Image File: The first line contains two integers representing the image dimensions (rows and columns). The subsequent lines contain the pixel values of the image.
- Mask File: The first line contains a single integer n, representing the size of the n x n mask. The next n lines contain the mask values.

#Features

- Utilizes multi-threading to improve the performance of image convolution operations.
- Supports custom convolution masks and variable thread counts.
