# SAR Image Colorization with GAN

This repository contains a PyTorch implementation of a Deep Convolutional GAN (DCGAN) for the task of SAR (Synthetic Aperture Radar) image colorization. The model learns to generate realistic color images from grayscale SAR inputs using adversarial training.

## 🧠 Model Architecture

### Generator
- Takes in 1-channel grayscale SAR image.
- Uses convolutional layers for encoding.
- Decodes using transposed convolution layers to generate a 3-channel RGB image.
- Includes dropout for regularization.

### Discriminator
- Takes in a 3-channel image.
- Uses convolutional layers to classify the image as real or fake.
- Final layer outputs a probability using Sigmoid activation.

## 📁 File Structure

```
├── generator.py        # Generator model definition
├── discriminator.py    # Discriminator model definition
├── main.py             # Entry point to start training
├── train.py            # (Expected) Training script with GAN training loop
```



## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/sar-colorization-gan.git
   cd sar-colorization-gan
   ```

2. Install dependencies:
   ```bash
   pip install torch torchvision
   ```

3. Add your SAR image dataset and update paths in `train.py`.

4. Run the training:
   ```bash
   python main.py
   ```

## 📌 Features

- Modular PyTorch implementation
- Dropout-enhanced generator for regularization
- Batch normalization for stable training
- Easily extendable for different image domains

## 🖼️ Output

After training, the generator should produce realistic colorized SAR images from grayscale inputs.

## 🧪 Future Improvements

- Add training metrics and loss visualization
- Introduce learning rate schedulers
- Improve generator with U-Net style skip connections

## 📜 License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

---

> Made with ❤️ using PyTorch.

