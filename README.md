# MULTITHREADED-FILE-COMPRESSION-TOOL

COMPANY: CODTECH IT SOLUTION

NAME: SAURABH KUMAR

INTERN ID: CT04DF95

DOMAIN: C++

DURATION: 4 WEEKS

MENTOR: NEELA SANTOSH 

# Description

Multithreaded File Compression Tool in C++ Using RLE
This C++ program is a file compression and decompression utility that applies the Run-Length Encoding (RLE) algorithm to compress data. It reads content from a text file, compresses or decompresses it based on the user's choice, and writes the result to an output file. The tool is designed to be efficient and could be further extended to a multithreaded environment for large files and high-performance requirements.

Overview of RLE (Run-Length Encoding)
Run-Length Encoding is a simple and lossless data compression method. It works by replacing sequences of repeated characters with a single character followed by the count of its repetitions.

Example:

Original String: "aaabbcc"

Compressed: "a3b2c2"

Decompressed back: "aaabbcc"

The RLE algorithm is most effective on data with many repeating characters and is often used in simple image compression, text storage, and telemetry logs.

Program Functionality
The tool supports two core operations:

Compression

Decompression

The user is first prompted to choose one of the two operations. Then, they provide the names of the input and output files. The program processes the file contents accordingly and writes the result to the output file.

Compression Function – compressRLE()
The compressRLE() function compresses the input string using the RLE algorithm. It iterates through the string and counts consecutive repeated characters. When it encounters a different character, it stores the character and the count.

Example operation:

Input: "aaaaabbbbcc"

Output: "a5b4c2"

The function constructs the output string using a loop and appends each compressed segment using to_string() to convert the count into a string.

Decompression Function – decompressRLE()
The decompressRLE() function reconstructs the original string from the RLE-compressed version. It reads each character and then parses the digits that follow (which represent the repetition count). Using stoi(), it converts the string digits into an integer and appends that many characters to the result.

This function also handles multi-digit numbers correctly (e.g., a12).

File Handling
The program uses C++ standard file streams:

ifstream to read the input file.

ofstream to write to the output file.

The entire file is read into a string using istreambuf_iterator, which allows efficient reading of large files.

After processing, the output is saved, and the program confirms the operation.

Multithreading Potential
While the current implementation is single-threaded, this design is well-suited for multithreading enhancements, especially when processing large files. Here's how multithreading could be applied:

Chunking: The input file can be divided into multiple segments (chunks), each processed in a separate thread using RLE.

Parallel Compression: Multiple threads can compress different parts of the file simultaneously, improving performance on multi-core processors.

Thread Synchronization: A shared output buffer or synchronized file writer would be required to combine the compressed segments correctly.

A multithreaded approach would significantly improve processing speed for large datasets and is highly relevant in modern applications where time and efficiency are critical.

Use Cases
Log file compression

Reducing size of configuration or telemetry files

Educational purposes to demonstrate basic compression and file I/O in C++

As a base for building more advanced compression formats (e.g., LZW, Huffman)

Benefits and Limitations
Benefits:

Easy to understand and implement

Lossless compression

Works well for repetitive data

Limitations:

Not efficient for data with little repetition

Output size can increase if data is not compressible

Basic form not optimized for binary data

Conclusion
This file compression tool in C++ offers a simple but effective way to compress and decompress files using the RLE algorithm. With the potential for multithreaded optimization, it can serve as a foundation for more advanced and performance-oriented compression tools. The program also demonstrates important programming concepts including file handling, string manipulation, algorithm design, and conditional logic—making it an ideal project for both practical use and educational purposes.

# OUTPUT 1
![Image](https://github.com/user-attachments/assets/d021a5e7-c7ae-4bdd-b656-fb5296ad2719)

# OUTPUT 2
![Image](https://github.com/user-attachments/assets/e74404cb-9973-47e4-a58a-97cbd9582b06)
