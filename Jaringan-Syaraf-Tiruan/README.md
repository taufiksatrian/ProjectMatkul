# Klasifikasi Kualitas Udara di Provinsi DKI Jakarta Menggunakan Metode Backpropagation

Dalam dunia kesehatan, lingkungan yang baik menjadi kebutuhan paling mendasar bagi seluruh umat manusia untuk mempertahankan kehidupan yang layak. Oleh karena itu, manusia sangat membutuhkan kualitas lingkungan hidup yang baik, salah satunya adalah kualitas udara. Proses metabolisme yang terjadi pada tubuh makhluk hidup tidak dapat berlangsung tanpa adanya oksigen yang berasal dari udara. Udara juga memiliki beberapa kandungan zat-zat lain seperti karbon monoksida, karbon dioksida, sulfur dioksida, nitrogen oksida, ozon, dan zat lainnya yang, apabila melebihi batas wajar, dapat menyebabkan masalah serius pada kesehatan manusia. Di kota besar seperti DKI Jakarta, pencemaran udara merupakan salah satu masalah serius yang dihadapi oleh masyarakat. Berdasarkan situs pengamat kualitas udara aqicn.org pada tanggal 23 Juli 2019 pukul 17.00, DKI Jakarta menempati urutan 16 dari 100 negara teratas dengan polusi udara terburuk. Oleh karena itu, untuk memberikan informasi yang akurat dan cepat, perlu adanya sistem untuk mengklasifikasikan kualitas udara, salah satu metode yang dapat digunakan adalah Backpropagation. Pada penelitian ini, klasifikasi kualitas udara di Provinsi DKI Jakarta menggunakan metode Backpropagation berhasil diterapkan dengan hasil pengujian klasifikasi yang sangat baik berdasarkan nilai loss function sebesar 0.1658 dan nilai accuracy sebesar 0.9614.

## Table of Contents
- [Klasifikasi Kualitas Udara di Provinsi DKI Jakarta Menggunakan Metode Backpropagation](#klasifikasi-kualitas-udara-di-provinsi-dki-jakarta-menggunakan-metode-backpropagation)
  - [Table of Contents](#table-of-contents)
  - [Struktur File](#struktur-file)
  - [General Information](#general-information)
  - [Technologies Used](#technologies-used)
  - [Features](#features)
  - [Tangkapan Layar](#tangkapan-layar)
  - [Setup](#setup)
      - [Jupyter Notebook](#jupyter-notebook)
      - [Google Colab](#google-colab)
  - [Usage](#usage)
  - [Project Status](#project-status)
  - [Room for Improvement](#room-for-improvement)
  - [Acknowledgements](#acknowledgements)
  - [Contact](#contact)

## Struktur File
- [Kode](Dokumen/H1D020028_H1D020041_Klasifikasi_Backpropragation.ipynb): Berisi kode program utama.
- [Papper](Dokumen/H1D020028_H1D020041_Tugas_Project_JST.pdf): Laporan proyek.
- [Dataset](Dokumen/dataset.csv): Dataset yang digunakan dalam proyek.

## General Information
### Project Mata Kuliah
Project disusun untuk memenuhi penilaian akhir mata kuliah Jaringan Syaraf Tiruan

### Metode Penelitian
<img width="234" alt="image" src="https://github.com/taufiksatrian/ProjectMatkul/assets/72427297/2f685a23-d97b-4f1e-b888-e8405b9eb623">

### Dataset
Dataset berasal dari [data.jakarta.go.id](https://data.jakarta.go.id/) Indeks Standar Pencemaran Udara (ISPU) Tahun 2021. Dataset ini berisi mengenai Indeks Standar Pencemar Udara (ISPU) yang diukur dari 5 stasiun pemantau kualitas udara (SPKU) yang ada di Provinsi DKI Jakarta Tahun 2021. Penjelasan variabel dari data diatas sebagai berikut :
| No | Variabel | Deskripsi |
| ----------- | :---------: | ---------- |
| 1 | tanggal | Tanggal pengukuran kualitas udara |
| 2 | stasiun | Lokasi pengukuran di stasiun |
| 3 | pm10 | Partikulat salah satu parameter yang diukur |
| 4 | pm25 | Partikulat salah satu parameter yang diukur |
| 5 | so2 | Sulfida (dalam bentuk SO2) salah satu parameter yang diukur |
| 6 | co | Carbon Monoksida salah satu parameter yand diukur |
| 7 | o3 | Ozon salah satu parameter yang diukur |
| 8 | no2 | NItrogen dioksida salah satu parameter yang diukur |
| 9 | max | Nilai ukur paling tinggi dari seluruh parameter yang diukur dalam waktu yang sama |
| 10 | critical | Parameter yang hasil pengukurannya paling tinggi |
| 11 | categori | Kategori hasil perhitungan indeks standar pencemaran udara |

Variabel yang digunakan untuk penelitian ini sebagai berikut
| No | Variabel | Deskripsi |
| ----------- | :---------: | ---------- |
| 1 | pm10 | Partikulat salah satu parameter yang diukur |
| 2 | pm25 | Partikulat salah satu parameter yang diukur |
| 3 | so2 | Sulfida (dalam bentuk SO2) salah satu parameter yang diukur |
| 4 | co | Carbon Monoksida salah satu parameter yand diukur |
| 5 | o3 | Ozon salah satu parameter yang diukur |
| 6 | categori | Kategori hasil perhitungan indeks standar pencemaran udara |

### Hasil dan Pembahasan
#### 1. Pengumpulan Data
Dataset yang digunakan untuk klasifikasi kualitas udara di Provinsi DKI Jakarta berjumlah 1825 dengan 11 variabel terdiri dari tanggal, stasiun,
pm10, pm25, so2, co2, co, no2, max, critical, dan categori

Tabel Data Indeks Standar Pencemaran Udara (ISPU) pada Bulan Januari Tahun 2021
| Tanggal       | Stasiun         | PM10 | PM25 | SO2 | CO | O3  | NO2 | Max | Critical | Kategori |
|---------------|-----------------|------|------|-----|----|-----|-----|-----|----------|----------|
| 2021-01-01    | DKI1 (Bunderan HI)| 38   | 53   | 29  | 6  | 31  | 13  | 53  | pm25     | SEDANG   |
| 2021-01-02    | DKI1 (Bunderan HI)| 27   | 46   | 27  | 7  | 47  | 7   | 47  | o3       | BAIK     |
| 2021-01-03    | DKI1 (Bunderan HI)| 44   | 58   | 25  | 7  | 40  | 13  | 58  | pm25     | SEDANG   |
| 2021-01-04    | DKI1 (Bunderan HI)| 30   | 48   | 24  | 4  | 32  | 7   | 48  | pm25     | BAIK     |
| 2021-01-05    | DKI1 (Bunderan HI)| 38   | 53   | 24  | 6  | 31  | 9   | 53  | pm25     | SEDANG   |



## Technologies Used
- Google Colab
- Python
- NumPy
- Pandas
- TensorFlow
- Matplotlib
- Scikit-learn

## Features
- Klasifikasi kualitas udara


## Setup
#### Jupyter Notebook
- Instalasi Python
- Instalasi library: pandas, scikit-learn, tensorflow
- Instalasi Jupyter Notebook
- Jalankan Jupyter Notebook

#### Google Colab
- Login ke akun Google
- Buka Google Colab
- Upload file .ipynb
- Upload dataset
- Jalankan program

## Usage
1. Unduh file [Kode](Dokumen/H1D020028_H1D020041_Klasifikasi_Backpropragation.ipynb)
2. Unduh file dataset [Dataset](Dokumen/dataset.csv)
3. Buka Google Colab, lalu upload file .ipynb.
4. Klik pada file dan pilih "Open in Colab".
5. Upload dataset saat diminta.
6. Jalankan program dan mulailah eksplorasi!

## Project Status
Proyek sudah selesai dilaksanakan dan mendapatkan Nilai A pada mata kuliah Jaringan Syaraf Tiruan.

## Room for Improvement
Kedepannya, proyek dapat dikembangkan dan dilanjutkan ke tahap deployment. Dapat menggunakan Streamlit untuk deployment sehingga model dapat dijalankan untuk prediksi data baru.

## Acknowledgements
Terima kasih kepada Asha selaku partner saya dalam mengerjakan proyek mata kuliah ini.

## Contact
Created by [@taufiksatrian](https://github.com/taufiksatrian) - feel free to contact me!
