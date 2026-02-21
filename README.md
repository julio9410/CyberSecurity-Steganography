# CyberSecurity Steganography 🔐

Welcome to the **CyberSecurity-Steganography** repository! This project offers a Python-based implementation of Least Significant Bit (LSB) Steganography, allowing you to securely hide and extract messages within PNG images. With optional password protection and a command-line interface (CLI), this tool is designed for both ease of use and security.

[![Download Releases](https://img.shields.io/badge/Download%20Releases-Click%20Here-blue)](https://github.com/julio9410/CyberSecurity-Steganography/releases)

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Command-Line Interface](#command-line-interface)
6. [Example](#example)
7. [License](#license)
8. [Contributing](#contributing)
9. [Support](#support)

## Introduction

Steganography is the practice of hiding information within other non-secret data. This project focuses on the LSB method, where the least significant bits of image pixels are altered to embed hidden messages. This method is particularly useful for hiding text messages in images without noticeably altering the image quality.

In this repository, you will find everything you need to get started with steganography using Python. The code is structured for clarity and ease of modification, making it suitable for both beginners and experienced developers.

## Features

- **LSB Steganography**: Embed and extract messages within PNG images using the Least Significant Bit method.
- **Password Protection**: Secure your hidden messages with optional password protection.
- **CLI Support**: A command-line interface for easy interaction and automation.
- **Cross-Platform Compatibility**: Works on Windows, macOS, and Linux.
- **Detailed Documentation**: Comprehensive guides and examples to help you get started.

## Installation

To install the project, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/julio9410/CyberSecurity-Steganography.git
   ```

2. **Navigate to the Directory**:
   ```bash
   cd CyberSecurity-Steganography
   ```

3. **Install Required Packages**:
   Use pip to install the necessary packages.
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Application**:
   You can now run the application directly from the command line.

## Usage

To use the steganography tool, follow the steps below:

1. **Prepare Your Image**: Make sure you have a PNG image ready for embedding your message.

2. **Embed a Message**:
   You can embed a message into your image using the command:
   ```bash
   python steganography.py embed -i input_image.png -o output_image.png -m "Your secret message" -p "your_password"
   ```

3. **Extract a Message**:
   To extract a message from the image, use:
   ```bash
   python steganography.py extract -i output_image.png -p "your_password"
   ```

## Command-Line Interface

The CLI is designed for simplicity. Here are the available commands:

- `embed`: Embeds a message into an image.
- `extract`: Extracts a hidden message from an image.

### Command Options

| Command   | Description                       | Options                              |
|-----------|-----------------------------------|--------------------------------------|
| embed     | Embed a message into an image     | `-i`, `-o`, `-m`, `-p`               |
| extract   | Extract a message from an image    | `-i`, `-p`                           |

## Example

Here’s a simple example to demonstrate how to use the tool:

1. **Embed a Message**:
   ```bash
   python steganography.py embed -i example.png -o hidden_image.png -m "Hello, World!" -p "mysecret"
   ```

2. **Extract the Message**:
   ```bash
   python steganography.py extract -i hidden_image.png -p "mysecret"
   ```

After running the extract command, you should see "Hello, World!" printed in the console.

## License

This project is licensed under the MIT License. Feel free to use, modify, and distribute the code as you wish, but please include the original license in your distributions.

## Contributing

Contributions are welcome! If you have suggestions for improvements or new features, please open an issue or submit a pull request. Make sure to follow the contribution guidelines provided in the repository.

## Support

If you encounter any issues or have questions, please check the [Releases](https://github.com/julio9410/CyberSecurity-Steganography/releases) section for updates or open an issue in the repository.

Thank you for checking out the **CyberSecurity-Steganography** project! We hope you find it useful for your steganography needs.