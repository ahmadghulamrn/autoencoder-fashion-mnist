
# Autoencoder Image Reconstruction Project

Proyek ini merupakan implementasi autoencoder sederhana menggunakan dataset Fashion MNIST, di mana input dan output berupa citra grayscale 28x28.

## 📁 Dataset
Dataset yang digunakan: **Fashion MNIST** (dari `tensorflow.keras.datasets`)
- Jumlah data latih: 60.000
- Jumlah data uji: 10.000
- Ukuran gambar: 28x28 piksel
- Format: Grayscale

## 🧠 Arsitektur Autoencoder
Model autoencoder menggunakan layer konvolusional dan transpos-konvolusional:
- Encoder:
  - Conv2D(32, 3x3, ReLU)
  - MaxPooling2D(2x2)
  - Conv2D(64, 3x3, ReLU)
  - MaxPooling2D(2x2)
- Decoder:
  - Conv2DTranspose(64, 3x3, ReLU)
  - UpSampling2D(2x2)
  - Conv2DTranspose(32, 3x3, ReLU)
  - UpSampling2D(2x2)
  - Conv2DTranspose(1, 3x3, Sigmoid)

## 📉 Performa Model (Loss Curve)
Grafik loss selama 10 epoch training:

![Loss Curve](assets/loss_curve.png)

## 📷 Contoh Hasil Rekonstruksi
Berikut adalah hasil input dan output autoencoder:

| Input | Output |
|-------|--------|
| ![Input1](assets/input1.png) | ![Output1](assets/output1.png) |
| ![Input2](assets/input2.png) | ![Output2](assets/output2.png) |
| ![Input3](assets/input3.png) | ![Output3](assets/output3.png) |


---

