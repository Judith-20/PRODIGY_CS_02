# Image Encryption Tool

This Python application provides a graphical user interface (GUI) to encrypt and decrypt image files using a simple pixel manipulation technique. The tool is built using `Tkinter` for the GUI and `Pillow` for image handling.

## Features

- Encrypts `.jpg`, `.jpeg`, and `.png` image files using XOR operation and pixel manipulation.
- Decrypts previously encrypted image files using the same key.
- Saves the encrypted and decrypted images in the same directory as the script with appropriate suffixes (`_encrypted`, `_decrypted`).
- Displays the selected file name and shows feedback upon success or failure of operations.

## Requirements

- Python 3.x
- The following Python libraries:
  - `tkinter` (usually included with Python)
  - `Pillow` (for image handling)

To install `Pillow`, run:

```bash
pip install pillow
```

## How It Works
The tool modifies the pixels in the selected image using the following steps:

- Encryption:

1. XORs each pixel value with the given key.
2. Adds 5 to each pixel value (mod 256) to further obfuscate the image.
3. Saves the modified image as encrypted_image.png.


- Decryption:

1. Reverses the pixel manipulation by first subtracting 5 (mod 256).
2. XORs the pixel values again with the same key.
3. Saves the restored image as decrypted_image.png.


## Usage
1. Run the script:
``` bash
python image_encryption.py
```
2. Select an image file (.jpg, .jpeg, .png) to encrypt or decrypt.

3. Enter a numeric key in the "Enter Key" field.

4. Click on the "Encrypt Image" or "Decrypt Image" button to perform the desired operation.

5. The processed image will be saved in the same folder as the script with the appropriate suffix.

## User Interface
The GUI consists of:

- **Enter Key Field:** Input an integer key for encryption and decryption.
- **Encrypt Image Button:** Encrypts the selected image.
- **Decrypt Image Button:** Decrypts the previously encrypted image.
- **File Display:** Shows the file name of the selected image.


## Example
1. **Encrypting an Image:**
- Select an image file and enter a key (e.g., 123).
- The tool will encrypt the image and save it as encrypted_image.png.

2. **Decrypting an Image:**
- Select the previously encrypted image and enter the same key.
- The tool will decrypt the image and save it as decrypted_image.png.


### Notes:
- Update the script file path or any other necessary paths in the instructions.
- Include screenshots if needed for further clarity!
