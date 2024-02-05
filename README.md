# Error-Detection-and-Correction-using-hamming-code-in-verilog-HDL
Try out here:
 
Encoder: https://www.edaplayground.com/x/5fZN
Decoder: https://www.edaplayground.com/x/Dbgd
Decoder with error: https://www.edaplayground.com/x/Zxa

# Hamming Code Encoder and Decoder
![image](https://github.com/Tabrez-dev/Error-Detection-and-Correction-using-hamming-code-in-verilog-HDL/assets/75200693/1394be69-a057-44f8-95dd-c58c89b62248)

![image](https://github.com/Tabrez-dev/Error-Detection-and-Correction-using-hamming-code-in-verilog-HDL/assets/75200693/8e28e88d-a5f5-4a31-ae55-a4c64de45918)
## Overview

This project implements a Hamming Code Encoder and Decoder in Verilog HDL. The Hamming Code is a linear error-correcting code used for detecting and correcting errors in data transmissions. The project consists of two main modules - `ham_encoder` for encoding data and `ham_decoder` for decoding and error correction.

## Key Concepts

### Hamming Code

The Hamming Code is a block error-correcting code that can detect and correct single-bit errors in data. It achieves this by adding redundant parity bits to the original data bits, forming a codeword. The parity bits are calculated based on specific rules, enabling the detection and correction of errors.

### ham_encoder Module

The `ham_encoder` module takes a 4-bit input data and generates a 7-bit Hamming Code. The parity bits are calculated based on the data bits. The encoding process involves XORing certain data bits to create parity bits, ensuring that the overall Hamming Code has the necessary error-detection and correction capabilities.

### ham_decoder Module

The `ham_decoder` module takes a 7-bit Hamming Code input, detects and corrects errors, and outputs the decoded 4-bit data along with error information. The decoding process involves checking parity bits and identifying the position of errors, if any. Single-bit errors can be corrected, while double-bit errors are detected.

## How to Use

1. **Encoder:**

   - Instantiate the `ham_encoder` module in your design.
   - Connect a 4-bit data input to the `data` port.
   - The encoded data is available at the `enc_ham_data` output.

2. **Decoder:**

   - Instantiate the `ham_decoder` module in your design.
   - Connect a 7-bit Hamming Code input to the `enc_ham_data` port.
   - Retrieve the decoded 4-bit data from the `data` output.
   - Check the `error` signal for error status.

## Simulation

To simulate the project:

1. Compile your Verilog files.
2. Run the simulation.
3. Check the output comments to verify the functionality.

## File Structure

- `ham_encoder.v`: Verilog file for the Hamming Code Encoder module.
- `ham_decoder.v`: Verilog file for the Hamming Code Decoder module.
- `testencoder.v`: Testbench for the Encoder module.
- `testdecoder.v`: Testbench for the Decoder module.



