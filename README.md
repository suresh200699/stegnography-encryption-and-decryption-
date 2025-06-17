# stegnography-encryption-and-decryption-

# Image Steganography with XOR Encryption

![Steganography Demo](demo.gif) *(Example visualization - add your own)*

A Python implementation of steganography that hides secret messages in images using XOR encryption for added security. This project demonstrates how to embed and extract text from images while maintaining visual integrity.

## Features

- **Image-based Steganography**: Hide messages within image pixels
- **XOR Encryption**: Basic encryption using a key for added security
- **ASCII Conversion**: Convert between characters and ASCII values
- **Visualization**: Display original and modified images using Matplotlib

## Prerequisites

- Python 3.8+
- Required packages:
  ```bash
  pip install opencv-python numpy matplotlib

#usage
1.load an image
image_path = "path/to/your/image.jpg"
x = cv2.imread(image_path)

2.set secret message and key
key = "123"  # Your encryption key
text = "secret"  # Your message

3.run the encryption
# Converts text and key to ASCII values
text_ascii = [d[ch] for ch in text]
key_ascii = [d[ch] for ch in key]

# Embeds message in image using XOR
x_enc = x.copy()
# ... (embedding logic from notebook)

4.save and view file
cv2.imwrite("encrypted.jpg", x_enc)
plt.imshow(cv2.cvtColor(x_enc, cv2.COLOR_BGR2RGB))

5.decryption
# Extract and decrypt the message
# ... (decryption logic from notebook)
print(decrypt)  # Should output your original message


##file Structure
steganography-project/
├── Steganography(code).ipynb  # Main Jupyter notebook
├── requirements.txt           # Python dependencies
├── images/
│   ├── input.jpg              # Sample input image
│   └── encrypted.jpg          # Output with hidden message
└── README.md                  # This file
