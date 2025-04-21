# 🕵️‍♂️ LSB Steganography

This project implements **Least Significant Bit (LSB) Steganography** using Python. It allows you to hide and extract secret messages within image files—particularly PNG images—by manipulating the least significant bits of the pixels, a method undetectable to the naked eye.

## 🔍 What is Steganography?

**Steganography** comes from the Greek words:
- **Steganos** – "Covered"
- **Graphie** – "Writing"

It is the practice of concealing messages within other non-secret, ordinary files (like images, audio, or video), so that only the intended recipient knows of the message’s existence.

## 🧠 LSB Technique Explained

In LSB steganography, the last bit (or bits) of a byte in an image’s pixel data are altered to encode the hidden message. This is effective because the change is minor enough to not visibly affect the image.

For example, in an 8-bit grayscale image:
- Each pixel = 8 bits.
- Changing the last bit alters the pixel value by at most **1**—visually undetectable.

### Example:

Suppose we want to hide the letter "A" (`ASCII: 10000001`) into the following grayscale pixel data:


Original pixels (in binary):
```
11110011
11011011
10110110
11011100
11011111
11010111
00100110
01000011
```

After hiding "A":
```
Modified pixels:
11110011
11011010
10110110
11011100
11011110
11010110
00100110
01000011
```

## 💡 Features

- 🖼️ Hide messages in grayscale or RGB PNG images.
- 🔐 Optional password protection.
- 🔍 Steganalysis notes included.

## 📜 Usage

Run the `stego` script with the appropriate flags:

### Embed a message:
```bash
./stego -f <filename.png> -e "<secret_message>" -p <password (optional)>
```

### Extract a message:
```bash
./stego -f <secretfile.png> -x -p <password>
```

⚠️ **Note:** Even if no password was used while embedding, the `-p` flag is still required during extraction.

## 🧪 Supported Steganography Types

While this project focuses on **Image Steganography**, here are the broad categories:

- 📷 **Image Steganography**
- 🎧 **Audio Steganography**
- 🎞️ **Video Steganography**
- 📄 **Text Steganography**

## 🖼️ Image Types

- 🟦 Black & White
- ⚪ Grayscale (8 bits per pixel)
- 🌈 RGB (24 bits per pixel)

> In RGB images, each pixel contains three components (Red, Green, Blue), and LSB manipulation can occur in any or all of them.

## 🔬 Steganalysis

**Steganalysis** is the art of detecting hidden messages in stego media.

- 📉 **Histogram Analysis** can help detect LSB manipulation.
- ❌ **Lossy Compression** (like JPEG) can destroy hidden data.
- ✅ Always use **lossless formats** (like PNG) for LSB-based techniques.

## 📂 Files in this Repository

- `stego.py` – Main Python script for LSB embedding and extraction.
- `README.md` – This file.
