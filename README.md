# Deteksi Penyakit Tanaman dengan CNN

Proyek ini bertujuan untuk mengklasifikasikan penyakit pada tanaman berdasarkan gambar daun menggunakan model Convolutional Neural Network (CNN) yang dibuat dengan TensorFlow. Dataset berisi gambar dari berbagai kategori penyakit dan daun sehat.

## Kategori Penyakit yang Dideteksi
- Anthracnose
- Bacterial Canker
- Cutting Weevil
- Die Back
- Gall Midge
- Healthy (Sehat)
- Powdery Mildew
- Sooty Mould

## Struktur Direktori Dataset
Dataset awal diekstrak dari file ZIP dan kemudian dibagi menjadi tiga bagian:

```
/content/dataset_split/
├── train/
├── val/
└── test/
```

## Langkah-langkah Menjalankan Proyek Ini

### 1. Clone Proyek
Clone repositori ini ke Google Colab atau sistem lokal kamu:
```bash
git clone <URL_REPOSITORI_KAMU>
```

### 2. Unggah Dataset ke Google Drive
Pastikan dataset ZIP (`monggo.zip`) berada di direktori Google Drive kamu, misalnya:
```
/drive/MyDrive/mesin/clasification_dataset/monggo.zip
```

### 3. Jalankan Kode di Google Colab
Gunakan file notebook Colab dan ikuti urutan langkah berikut:

- Mount Google Drive
- import library yg dibutuhkan bisa di cek di requirments.txt
- Ekstrak file ZIP
- Bagi dataset ke train/val/test
- Lakukan augmentasi dan load data dengan `ImageDataGenerator`
- Bangun model CNN
- Latih model selama beberapa epoch
- Evaluasi dan visualisasikan hasil

### 4. Menyimpan dan Mengekspor Model
Model disimpan dalam 3 format:
- TensorFlow.js (`tfjs_model`)
- TensorFlow Lite (`tflite`)
- SavedModel (`saved_model`)

Model bisa digunakan untuk keperluan web, Android, atau inference lanjutan.

### 5. Inference (Prediksi Gambar Baru)
Gunakan fungsi `predict_disease(img_path, model, class_labels)` untuk melakukan prediksi terhadap gambar daun baru. Hasil prediksi akan menampilkan label serta confidence-nya dalam bentuk persen.

## Instalasi Tambahan (Jika Perlu)
Untuk ekspor model ke TensorFlow.js:
```bash
pip install tensorflowjs==4.12.0
```

## Hasil Model
Model menghasilkan akurasi validasi dan test yang dapat divisualisasikan melalui grafik akurasi dan loss. Model juga diuji dengan confusion matrix dan classification report.

---

Jika kamu ingin mengembangkan proyek ini lebih lanjut, misalnya dengan menambah data atau meningkatkan performa model, silakan fork dan kontribusikan!

📁 Folder hasil ekspor model akan berada di misalnya:
```
/drive/MyDrive/mesin/tfjs_model/
/drive/MyDrive/mesin/tflite/
/drive/MyDrive/mesin/saved_model/
```

---

Terima kasih sudah menggunakan proyek ini! 🌱

