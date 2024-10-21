# PRODIGY_CS_02
# Simple BMP Image Encryption Tool
This is a Python tool for encrypting and decrypting BMP image files using a basic RGB pixel manipulation technique. The program reads a BMP image, applies encryption or decryption by adjusting the RGB values of each pixel based on a user-provided key, and saves the modified image as a new file.

Features
Supports BMP image format.
Encrypts or decrypts images by modifying pixel values.
Uses a simple, reversible encryption method with a user-defined key.
Requirements
Python 3.x
How It Works
The tool performs the following steps:

Reading the Image: The BMP image is read into memory, extracting the pixel values (R, G, B) for each pixel.
Encryption/Decryption:
For encryption, the RGB values of each pixel are incremented by the key value (mod 256).
For decryption, the RGB values are decremented by the key value (mod 256).
Saving the Image: The modified image is saved as either encrypted_image.bmp or decrypted_image.bmp.
Usage
Clone or download the project files.

Ensure that the BMP image you want to process is named input_image.bmp and placed in the same directory as the script.

Run the script using the command line:

bash
Copy code
python image_encryption.py
You will be prompted to choose an operation:

Enter E to encrypt the image.
Enter D to decrypt the image.
The encrypted or decrypted image will be saved in the same directory as:

encrypted_image.bmp for encrypted images.
decrypted_image.bmp for decrypted images.
Example
After running the script, the output might look like this:

mathematica
Copy code
Simple Image Encryption Tool
Choose operation (E)ncrypt or (D)ecrypt: E
Image encrypted and saved as 'encrypted_image.bmp'.
Code Structure
Pixel Class: Represents an individual pixel with RGB values.
read_image(): Reads the BMP file and extracts pixel data.
write_image(): Writes pixel data to a new BMP file.
process_image(): Encrypts or decrypts pixel data using a simple key-based operation.
main(): Provides user interaction and executes the chosen operation.
Encryption Method
The encryption is performed by adding a key to each pixel's red, green, and blue (RGB) values. The decryption works by subtracting the same key. The operations are performed modulo 256 to ensure the values stay within valid RGB limits (0-255).

Notes
The tool currently supports only 24-bit BMP files (uncompressed, no alpha channel).
Padding is handled automatically for BMP row alignment (each row in a BMP file must be a multiple of 4 bytes).
Future Improvements
Add support for other image formats (e.g., PNG, JPEG).
Implement more advanced encryption techniques.
Add error handling for unsupported file formats.
