# Klasifikasi Kualitas Udara di Provinsi DKI Jakarta Menggunakan Metode Backpropagation

Dalam dunia kesehatan, lingkungan yang baik menjadi kebutuhan paling mendasar bagi seluruh umat manusia untuk mempertahankan kehidupan yang layak. Oleh karena itu, manusia sangat membutuhkan kualitas lingkungan hidup yang baik, salah satunya adalah kualitas udara. Proses metabolisme yang terjadi pada tubuh makhluk hidup tidak dapat berlangsung tanpa adanya oksigen yang berasal dari udara. Udara juga memiliki beberapa kandungan zat-zat lain seperti karbon monoksida, karbon dioksida, sulfur dioksida, nitrogen oksida, ozon, dan zat lainnya yang, apabila melebihi batas wajar, dapat menyebabkan masalah serius pada kesehatan manusia. Di kota besar seperti DKI Jakarta, pencemaran udara merupakan salah satu masalah serius yang dihadapi oleh masyarakat. Berdasarkan situs pengamat kualitas udara aqicn.org pada tanggal 23 Juli 2019 pukul 17.00, DKI Jakarta menempati urutan 16 dari 100 negara teratas dengan polusi udara terburuk. Oleh karena itu, untuk memberikan informasi yang akurat dan cepat, perlu adanya sistem untuk mengklasifikasikan kualitas udara, salah satu metode yang dapat digunakan adalah Backpropagation. Pada penelitian ini, klasifikasi kualitas udara di Provinsi DKI Jakarta menggunakan metode Backpropagation berhasil diterapkan dengan hasil pengujian klasifikasi yang sangat baik berdasarkan nilai loss function sebesar 0.1658 dan nilai accuracy sebesar 0.9614.

<img width="1200" alt="image" src="https://github.com/taufiksatrian/ProjectMatkul/assets/72427297/f1749bc0-3829-48ca-b1ab-c0978fdd162e">

## Table of Contents
- [Klasifikasi Kualitas Udara di Provinsi DKI Jakarta Menggunakan Metode Backpropagation](#klasifikasi-kualitas-udara-di-provinsi-dki-jakarta-menggunakan-metode-backpropagation)
  - [Table of Contents](#table-of-contents)
  - [Struktur File](#struktur-file)
  - [General Information](#general-information)
  - [Technologies Used](#technologies-used)
  - [Features](#features)
  - [Setup](#setup)
  - [Usage](#usage)
  - [Project Status](#project-status)
  - [Room for Improvement](#room-for-improvement)
  - [Acknowledgements](#acknowledgements)
  - [Contact](#contact)

## Struktur File
- [Kode](Dokumen/H1D020028_H1D020041_Klasifikasi_Backpropragation.ipynb): Berisi kode program utama.
<a href="Dokumen/H1D020028_H1D020041_Klasifikasi_Backpropragation.ipynb" title="Kode program" target="_blank">
  <img src="https://github.com/taufiksatrian/ProjectMatkul/assets/72427297/7a697f33-8cfa-4dbb-8d33-b8d876ef28c2" alt="Kode program" style="width: 500px">
</a>

- [Papper](Dokumen/H1D020028_H1D020041_Tugas_Project_JST.pdf): Laporan proyek.
<a href="Dokumen/H1D020028_H1D020041_Tugas_Project_JST.pdf" title="Laporan proyek" target="_blank">
  <img src="https://github.com/taufiksatrian/ProjectMatkul/assets/72427297/ea78bb2f-0965-4494-b5d4-b4115b269d47" alt="Laporan proyek" style="width: 500px">
</a>

- [Dataset](https://data.jakarta.go.id/dataset/indeks-standar-pencemaran-udara-ispu-tahun-2021): Dataset yang digunakan dalam proyek.
<a href="https://data.jakarta.go.id/dataset/indeks-standar-pencemaran-udara-ispu-tahun-2021" title="Dataset" target="_blank">
  <img src="https://github.com/taufiksatrian/ProjectMatkul/assets/72427297/39c98f03-2e79-4681-b47d-766fd3fe30c9" alt="Dataset" style="width: 500px">
</a>

## General Information
### Project Mata Kuliah
Project disusun untuk memenuhi penilaian akhir mata kuliah Jaringan Syaraf Tiruan Semester 5 Tahun 2022

### Metode Penelitian
<img width="1200" alt="image" src="https://github.com/taufiksatrian/ProjectMatkul/assets/72427297/f8ef604d-bfc6-4677-b09e-bcc5a9ccc155">

### Dataset
Dataset berasal dari [data.jakarta.go.id](https://data.jakarta.go.id/) Indeks Standar Pencemaran Udara (ISPU) Tahun 2021. Dataset ini berisi mengenai Indeks Standar Pencemar Udara (ISPU) yang diukur dari 5 stasiun pemantau kualitas udara (SPKU) yang ada di Provinsi DKI Jakarta Tahun 2021. Penjelasan variabel dari data diatas sebagai berikut :
| No | Variabel | Deskripsi | 
| ----------- | :---------: | ---------- | 
| 1 | tanggal | Tanggal pengukuran kualitas udara |
| 2 | stasiun | Lokasi pengukuran di stasiun |
| 3 | pm10 | Partikulat salah satu parameter yang diukur | 
| 4 | pm25 | Partikulat salah satu parameter yang diukur | 
| 5 | so2 | Sulfida (dalam bentuk SO2) salah satu parameter yang diukur 
| 6 | co | Carbon Monoksida salah satu parameter yand diukur | 
| 7 | o3 | Ozon salah satu parameter yang diukur | 
| 8 | no2 | NItrogen dioksida salah satu parameter yang diukur |
| 9 | max | Nilai ukur paling tinggi dari seluruh parameter yang diukur dalam waktu yang sama | 
| 10 | critical | Parameter yang hasil pengukurannya paling tinggi | 
| 11 | categori | Kategori hasil perhitungan indeks standar pencemaran udara | 


### Hasil dan Pembahasan
#### 1. Pengumpulan Data
Dataset yang digunakan untuk klasifikasi kualitas udara di Provinsi DKI Jakarta berjumlah 1825 dengan 11 variabel terdiri dari tanggal, stasiun,
pm10, pm25, so2, co2, co, no2, max, critical, dan categori

Tabel Data Indeks Standar Pencemaran Udara (ISPU) Jakarta 2021
| Tanggal       | Stasiun         | PM10 | PM25 | SO2 | CO | O3  | NO2 | Max | Critical | Kategori |
|---------------|-----------------|------|------|-----|----|-----|-----|-----|----------|----------|
| 2021-01-01    | DKI1 (Bunderan HI)| 38   | 53   | 29  | 6  | 31  | 13  | 53  | pm25     | SEDANG   |
| 2021-01-02    | DKI1 (Bunderan HI)| 27   | 46   | 27  | 7  | 47  | 7   | 47  | o3       | BAIK     |
| 2021-01-03    | DKI1 (Bunderan HI)| 44   | 58   | 25  | 7  | 40  | 13  | 58  | pm25     | SEDANG   |
| 2021-01-04    | DKI1 (Bunderan HI)| 30   | 48   | 24  | 4  | 32  | 7   | 48  | pm25     | BAIK     |
| 2021-01-05    | DKI1 (Bunderan HI)| 38   | 53   | 24  | 6  | 31  | 9   | 53  | pm25     | SEDANG   |

#### 2. Preprocessing Data
Tahap Preprocessing Data yang pertama adalah dengan Data Selection dengan menyeleksi variabel yang dapat digunakan untuk pemodelan menjadi 6 variabel

Tabel Dataset Hasil Data Selection
| PM10 | PM25 | SO2 | CO | O3  | Kategori |
|------|------|-----|----|-----|----------|
| 38   | 53   | 29  | 6  | 31  | SEDANG   |
| 27   | 46   | 27  | 7  | 47  | BAIK     |
| 44   | 58   | 25  | 7  | 40  | SEDANG   |
| 30   | 48   | 24  | 4  | 32  | BAIK     |
| 38   | 53   | 24  | 6  | 31  | SEDANG   |

Data Cleaning dengan menghapus data yang hilang (missing value), hasil data cleaning yaitu dataset berkurang menjadi 1517 data

Tabel Dataset Hasil Data Cleaning
| Variabel | Jumlah Non-Null |
|------|------|
| PM10 | 1517 |
| PM25 | 1517 |
| S02 | 1517 |
| CO | 1517 |
| O3 | 1517 |
| Kategori | 1517 |

Data Transformation menggunakan metode normalisasi Min-Max dan menggunakan Label Encoder untuk memberikan label pada data output

Tabel Dataset Hasil Data Transformation
| pm10      | pm25      | so2       | co        | o3        | no2       | categori   |
|-----------|-----------|-----------|-----------|-----------|-----------|------------|
| 0.140244  | 0.248447  | 0.3375    | 0.097561  | 0.160839  | 0.161290  | 1          |
| 0.073171  | 0.204969  | 0.3125    | 0.121951  | 0.272727  | 0.064516  | 2          |
| 0.176829  | 0.279503  | 0.2875    | 0.121951  | 0.223776  | 0.161290  | 1          |
| 0.091463  | 0.217391  | 0.2750    | 0.048780  | 0.167832  | 0.064516  | 2          |
| 0.140244  | 0.248447  | 0.2750    | 0.097561  | 0.160839  | 0.096774  | 1          |

#### 3. Split Data
Split Data atau membagi dataset menjadi data training dan data testing diperlukan sebelum melakukan pemodelan. Hasil dari split data dengan perbandingan data training dan testing 80:20 menggunakan ‘test_size’ sebesar 0.2 serta menggunakan ‘random_state’ sebesar 42 untuk menginisialisasi data secara acak, menghasilkan data training dengan jumlah data 1213 dan data testing dengan jumlah data 304.

<p align="center">
  <img width="400" alt="image" src="https://github.com/taufiksatrian/ProjectMatkul/assets/72427297/ae4377db-7d46-47c7-8978-e1fdeee2be34">
</p>


#### 4. Pembangunan Model Backpropagation
Pembangunan model menggunakan model backpropagation dengan model arsitektur Sequential. Input layer menggunakan fungsi aktivasi ReLU dengan jumlah units 6. Satu hidden layer menggunakan fungsi aktivasi ReLU dengan jumlah units 30. Output layer menggunakan fungsi aktivasi Softmax dengan jumlah units 3. Model backpropagation dibangun melalui beberapa tahap compile. Tahap compile menggunakan optimizer 'adam' untuk learning rate, loss function 'sparse_categorical_crossentropy' untuk klasifikasi multi-class, dan metrics 'accuracy' untuk menilai kinerja model.

Gambar Arsitektur Model

<p align="center">
  <img width="200" alt="image" src="https://github.com/taufiksatrian/ProjectMatkul/assets/72427297/fdaa2872-d9c4-42cf-9734-68cb5ec99f76">
</p>

#### 5. Pengujian Model Backpropagation
Pengujian model backpropagation telah memberikan hasil yang sangat baik, terindikasi dari nilai loss dan accuracy pada data training dan testing yang optimal. Selain itu, hasil yang diperoleh menunjukkan ketidakmunculan gejala overfitting, menandakan kemampuan generalisasi yang baik dari model.

Tabel Hasil Pengujian 
| Parameter Pengujian | Data Training | Data Testing |
|--------------|---------------|--------------|
| Loss         | 0.1832        | 0.1658       |
| Accuracy     | 0.9413        | 0.9614       |

Hasil pengujian dengan Loss dan Accuracy
<div style="display: flex; justify-content: space-between;">
  <p align="center">
    <img width="400" alt="image" src="https://github.com/taufiksatrian/ProjectMatkul/assets/72427297/525a52bf-cc3c-4114-85ff-2d6516ec6ea3">
    <img width="400" alt="image" src="https://github.com/taufiksatrian/ProjectMatkul/assets/72427297/bed352fe-aa21-478a-b55f-6cffb8cae107">
  </p>
</div>

Selanjutnya, hasil pengujian model dievaluasi menggunakan Confusion Matrix untuk mendapatkan wawasan lebih mendalam tentang kinerja model pada tugas klasifikasi. Confusion Matrix memberikan gambaran yang detail mengenai sejauh mana model mampu mengklasifikasikan data ke dalam kategori yang benar.

Hasil pengujian dengan Confusion Matrix

<p align="center">
  <img width="400" alt="image" src="https://github.com/taufiksatrian/ProjectMatkul/assets/72427297/76a28b15-7f87-415d-8306-74118b09b67b">
</p>

Data Klasifikasi Kualitas Udara di Provinsi DKI Jakarta 2021 

<p align="center">
  <img width="400" alt="image" src="https://github.com/taufiksatrian/ProjectMatkul/assets/72427297/086fa2c1-2935-41c3-a059-a798fdea6dbd">
</p>

### Kesimpulan
Klasifikasi kualitas udara di Provinsi DKI Jakarta menggunakan **metode Backpropagation** berhasil diterapkan dengan hasil klasifikasi yang sangat baik berdasarkan **nilai loss function sebesar 0.1658** dan **nilai accuracy sebesar 0.9614**.

**Kategori "Sedang"**:
Jumlah data yang masuk ke dalam kategori ini paling dominan, yaitu sebanyak 1147 observasi.
Kesimpulan: Kualitas udara pada kategori "Sedang" memiliki frekuensi tertinggi, menunjukkan bahwa sebagian besar waktu di Provinsi DKI Jakarta pada tahun 2021, kualitas udara berada dalam kategori ini.

**Kategori "Tidak Baik"**:
Jumlah data pada kategori "Tidak Baik" adalah 245 observasi.
Kesimpulan: Meskipun kategori "Tidak Baik" memiliki frekuensi yang lebih rendah dibanding kategori "Sedang", tetapi jumlahnya cukup signifikan. Hal ini menunjukkan bahwa ada periode tertentu di mana kualitas udara memburuk dan masuk ke dalam kategori "Tidak Baik".

**Kategori "Baik":**
Jumlah data pada kategori "Baik" adalah 125 observasi.
Kesimpulan: Kategori "Baik" memiliki frekuensi yang lebih rendah, menunjukkan bahwa kondisi kualitas udara yang baik terjadi pada sebagian kecil waktu.

Secara umum, kualitas udara di Provinsi DKI Jakarta pada tahun 2021 didominasi oleh kategori "Sedang", tetapi juga terdapat periode tertentu dengan kualitas udara yang memburuk (kategori "Tidak Baik") dan waktu yang lebih terbatas dengan kualitas udara yang baik (kategori "Baik").

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
