# speech_classification

# 🐾 Klasifikasi Suara Hewan menggunakan CNN

Proyek ini bertujuan untuk membangun dan melatih model Convolutional Neural Network (CNN) untuk mengklasifikasikan suara dari lima jenis hewan: Sapi (moo), Kucing (meow), Anjing (woof), Kambing (mbee), dan Burung (tweet).

Notebook ini memandu langkah-langkah mulai dari persiapan dataset, pra-pemrosesan audio, ekstraksi fitur, definisi arsitektur CNN, pelatihan model, hingga evaluasi dan pengujian klasifikasi langsung.

## Daftar Isi

1.  [Instalasi & Impor Library](#instalasi--impor-library)
2.  [Persiapan Dataset](#persiapan-dataset)
3.  [Pra-pemrosesan Audio & Ekstraksi Fitur](#pra-pemrosesan-audio--ekstraksi-fitur)
4.  [Visualisasi Data](#visualisasi-data)
5.  [Arsitektur Model CNN](#arsitektur-model-cnn)
6.  [Pelatihan Model](#pelatihan-model)
7.  [Evaluasi Kinerja Model](#evaluasi-kinerja-model)
8.  [Uji Coba Klasifikasi Langsung](#uji-coba-klasifikasi-langsung)

## Cara Menjalankan Notebook

1.  **Buka di Google Colab**: Anda dapat membuka notebook ini langsung di Google Colab.
2.  **Jalankan Sel Secara Berurutan**: Ikuti langkah-langkah dalam notebook dan jalankan setiap sel secara berurutan.
3.  **Unggah Dataset**: Pada bagian "Persiapan Dataset", Anda akan diminta untuk mengunggah file `data.zip` yang berisi dataset suara hewan Anda. Pastikan struktur folder di dalam zip sesuai dengan penjelasan di notebook (`data/[KelasHewan]/[namafile].wav`).

## 1. Instalasi & Impor Library

Menginstal library Python yang diperlukan seperti `sounddevice`, `soundfile`, `librosa`, `torch`, `matplotlib`, `scipy`, dan `scikit-learn`. Juga menginstal `portaudio19-dev` yang diperlukan oleh `sounddevice`.

## 2. Persiapan Dataset

Mengunggah dan mengekstrak file `data.zip`. Notebook akan memverifikasi struktur folder dataset yang diekstrak.

## 3. Pra-pemrosesan Audio & Ekstraksi Fitur

Mengubah file audio mentah menjadi fitur MFCC yang siap untuk diolah oleh model CNN. Langkah-langkah seperti Voice Activity Detection, padding/cropping, normalisasi, dan ekstraksi MFCC dilakukan di sini. Dataset kemudian dibagi menjadi data training dan testing.

## 4. Visualisasi Data

Memvisualisasikan bentuk gelombang audio (sebelum dan sesudah pra-pemrosesan) dan spektogram MFCC untuk memahami representasi data yang akan digunakan.

## 5. Arsitektur Model CNN

Mendefinisikan arsitektur model CNN sederhana yang terdiri dari lapisan konvolusi, pooling, dan lapisan fully connected untuk klasifikasi.

## 6. Pelatihan Model

Melatih model CNN menggunakan data training. Proses pelatihan melibatkan penggunaan fungsi loss `CrossEntropyLoss` dan optimizer `Adam`. Akurasi pada data training dan testing dipantau selama pelatihan.

## 7. Evaluasi Kinerja Model

Mengevaluasi performa akhir model pada data testing menggunakan metrik seperti akurasi, precision, recall, dan F1-score yang ditampilkan dalam classification report. Model yang telah dilatih juga disimpan.

## 8. Uji Coba Klasifikasi Langsung

Memungkinkan pengguna untuk mengunggah file audio baru dan menggunakan model yang telah dilatih untuk memprediksi kelas suara hewan dari file tersebut.

---

**Catatan**: Dataset yang digunakan dalam notebook ini adalah dataset simulasi/tiruan untuk tujuan demonstrasi. Untuk aplikasi dunia nyata, diperlukan dataset suara hewan yang lebih besar dan bervariasi.
