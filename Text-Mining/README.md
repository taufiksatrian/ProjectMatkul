# Analisis Sentimen Kepercayaan Masyarakat Terhadap Polisi Republik Indonesia Menggunakan Metode Klasifikasi Naive Bayes dan K-Nearest Neighbor (KNN)

Kepuasan masyarakat terhadap kinerja Kepolisian Negara Republik Indonesia (Polri) merupakan bagian penting, salah satu indikator penentu keberhasilan Polri. Baik buruknya Polri tidak hanya ditentukan ukuran yang ditetapkan secara internal, namun juga ditentukan oleh kepuasan masyarakat terhadap kinerja Polri. Tingkat kepercayaan masyarakat terhadap kinerja Polri telah menunjukkan peningkatan dari tahun ke tahun, ditunjukkan oleh beberapa hasil survei yang dilakukan, baik oleh lembaga survei eksternal (Indo Barometer dan Litbang Kompas) maupun Puslitbang Polri, menunjukkan beberapa layanan kepolisian yang dirasakan publik masih kurang. Analisis sentimen adalah text mining yang menganalisis dan mengekstraksi informasi yang bersifat subjektif dan dapat membantu pihak yang membutuhkan. Penelitian ini bertujuan untuk mengetahui opini masyarakat terhadap polisi di Twitter berdasarkan tiga klasifikasi, yaitu positif, netral, dan negatif. Metode Naive Bayes dan KNN dipilih karena tingkat akurasi yang tinggi, mudah untuk dipahami, dan memiliki cepat dalam mengklasifikasi data. Pemodelan klasifikasi Naive Bayes dengan feature extraction model BOW mendapatkan score accuracy sebesar 0.96, precision sebesar 0.96, recall sebesar 0.96, dan F1 Score sebesar 0.95. Pada hasil penelitian ini menunjukkan bahwa model Naive Bayes mampu melakukan klasifikasi sentimen analisis kepercayaan masyarakat terhadap polisi pada Twitter ditunjukkan dari hasil evaluasi yang baik.

<img width="1200" alt="image" src="https://github.com/taufiksatrian/ProjectMatkul/assets/72427297/ef1cdfde-41bb-4989-9ddb-b57a1c003856">

## Table of Contents
- [Analisis Sentimen Kepercayaan Masyarakat Terhadap Polisi Republik Indonesia Menggunakan Metode Klasifikasi Naive Bayes dan K-Nearest Neighbor (KNN)](#analisis-sentimen-kepercayaan-masyarakat-terhadap-polisi-republik-indonesia-menggunakan-metode-klasifikasi-naive-bayes-dan-k-nearest-neighbor-knn)
  - [Table of Contents](#table-of-contents)
  - [File](#file)
  - [General Information](#general-information)
  - [Technologies Used](#technologies-used)
  - [Features](#features)
  - [Setup](#setup)
  - [Usage](#usage)
  - [Project Status](#project-status)
  - [Room for Improvement](#room-for-improvement)
  - [Acknowledgements](#acknowledgements)
  - [Contact](#contact)
 

## File
- [Kode](https://github.com/taufiksatrian/ProjectMatkul/blob/main/Text-Mining/Analisis%20Sentimen%20Kepercayaan%20Masyarakat%20Terhadap%20Polisi%20Republik%20Indonesia%20Menggunakan%20Metode%20Naive%20Bayes.ipynb): Berisi kode program utama.
<a href="https://github.com/taufiksatrian/ProjectMatkul/blob/main/Text-Mining/Analisis%20Sentimen%20Kepercayaan%20Masyarakat%20Terhadap%20Polisi%20Republik%20Indonesia%20Menggunakan%20Metode%20Naive%20Bayes.ipynb" title="Kode program" target="_blank">
  <img src="https://github.com/taufiksatrian/ProjectMatkul/assets/72427297/28737704-b273-4e1e-b2f1-b7a7a50142a6" alt="Kode program" style="width: 500px">
</a>

- [Papper](https://github.com/taufiksatrian/ProjectMatkul/blob/main/Text-Mining/H1D020028_H1D020046_TEXT%20MINING_PROJEK%20AKHIR.pdf): Laporan project.
<a href="https://github.com/taufiksatrian/ProjectMatkul/blob/main/Text-Mining/H1D020028_H1D020046_TEXT%20MINING_PROJEK%20AKHIR.pdf" title="Laporan project" target="_blank">
  <img src="https://github.com/taufiksatrian/ProjectMatkul/assets/72427297/cf1f8ca4-d1c9-4443-806c-4af8afb8cccc" alt="Laporan project" style="width: 500px">
</a>


## General Information
### Project Mata Kuliah
Project disusun untuk memenuhi penilaian akhir mata kuliah Text Mining Semester 5 Tahun 2022

### Latar Belakang
Kepuasan masyarakat terhadap kinerja Kepolisian Negara Republik Indonesia (Polri) merupakan bagian penting, salah satu indikator penentu keberhasilan Polri. Baik buruknya Polri tidak hanya ditentukan ukuran yang ditetapkan secara internal, namun juga ditentukan oleh kepuasan masyarakat terhadap kinerja Polri. Tingkat kepercayaan masyarakat terhadap kinerja Polri telah menunjukkan peningkatan dari tahun ke tahun, ditunjukkan oleh beberapa hasil survei yang dilakukan, baik oleh lembaga survei eksternal (Indo Barometer dan Litbang Kompas) maupun Puslitbang Polri, menunjukkan beberapa layanan kepolisian yang dirasakan publik masih kurang.

### Tujuan
Penelitian ini bertujuan untuk mengetahui opini masyarakat terhadap polisi di Twitter berdasarkan tiga klasifikasi, yaitu komentar positif, netral, dan negatif. Metode NBC dan KNN dipilih karena tingkat akurasi yang tinggi, mudah untuk dipahami, dan memiliki cepat dalam mengklasifikasi data. Penelitian ini diharapkan mampu menjelaskan langkah-langkah secara terstruktur dalam mengimplementasikan metode NBC dan K-Nearest Neighbor (KNN) dalam mengklasifikasi teks. Analisis Sentimen Masyarakat terhadap polisi berdasarkan Opini dari Twitter Menggunakan Metode Naive Bayes Classifier (NBC) dan K-Nearest Neighbor (KNN) melakukan klasifikasi sentimen analisis terhadap komentar atau cuitan dari masyarakat terhadap polisi. Komentar tersebut diambil melalui Twitter dengan beberapa tahapan, yaitu pengumpulan data, preprocessing data, Labeling, Feature extractions menggunakan model BOW dan TF-IDF klasifikasi text dan evaluasi.

### Metode Penelitian


### Dataset
Dataset berisi kumpulan data tweet dari Twitter yang dikumpulkan menggunakan metode crawling. Dataset ini mencakup informasi seperti tanggal, username, dan teks tweet yang dapat digunakan untuk pemahaman lebih lanjut terkait topik atau isu yang sedang dibahas di platform Twitter.

### Hasil dan Pembahasan
#### 1. Pengumpulan Data
Hasil crawling data dengan memasukkan kata kunci polisi dan mensetting jumlah data sebanyak 1000 tweet menggunakan library
snscrapper pada python.

Tabel Hasil Crawling Data
| Datatime                   | Username      | Text                                                                                                                                   |
|-----------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------|
| 2022-10-31 23:59:50+00:00  | Polsek_Pdr442 | Sambang obyek vital Bhabinkamtibmas AIPTU Siswanto berikan himbauan kamtibmas dan tetap menerapkan protokol kesehatan. ...              |
| 2022-10-31 23:59:04+00:00  | joekampret1   | Ini arah kudeta boss Knp Polri dan TNI diem sja Sebelum mereka bergerak, tangkap dulu orang2 nya. Tindakan humanis gk cocok bwt mereka. ...   |
| 2022-10-31 23:58:45+00:00  | el_f4hm1      | @GrangerKeren @GratisTerbaik @CCICPolri @DivHumas_Polri Brapa % yg meninggal atau KIPI berat dibanding yg hidup dan sehat?.                   |
| 2022-10-31 23:58:44+00:00  | Ky46W1        | @tvOneNews Bisa kasih contoh dong dri bapakÂ² kepolisian @DivHumas_Polri ...                                                              |
| 2022-10-31 23:58:12+00:00  | NunoenkZidan  | @olvaholvah @DivHumas_Polri @ListyoSigitP @KomnasPerempuan @KomnasHAM Pantesan gk ngelawan ternyata d pukulin kakanya krn gk nungguin ...       |
| ... | ... | ... |
| 2022-10-31 14:38:10+00:00  | NTMC_Info     | Pantauan Langsung Arus Lalu Lintas Hari Ini Bersama Briptu Anizha pukul 20.00 wib, Senin 31 Oktober 2022 melalui CCTV NTMC Polri. ...         |
| 2022-10-31 14:38:03+00:00  | inilahdotcom   | Brigjen Hendra Kurniawan Dipecat Polri, Dianggap Berbuat Tercela Terkait Kasus Brigadir J ...                                            |
| 2022-10-31 14:37:47+00:00  | Adh1stya      | @UtangJpu @DivHumas_Polri                                                                                                             |
| 2022-10-31 14:37:39+00:00  | jiggle2222    | @kylantower @sayainiultramen @mazzini_gsp Sementara brigjen hendra seorang pati polri mengaku tidak tahu skenario fs tidak ada tuh ...         |
| 2022-10-31 14:37:34+00:00  | parsya21      | "Untuk menjaga kepercayaan masyarakat, Polri perlu melakukan perbaikan institusi secara menyeluruh," -- Puan Maharani ...                |

#### 2. Preprocessing

Tabel Hasil Preprocessing
| Keterangan | Tweets |
| ------------- | ------ |
| Data Awal | @humaspoldajbr Mohon buat @PolhukamRI @DPR_RI @DivHumas_Polri .....perjelas payung hukum,supaya warga sekitar,tetangga , masyarakat setempat punya hak untuk mendobrak rumah tetangga jika terjadi indikasi kekerasan dan keanehan di rumah tersebut.supaya warga tidak takut.dan care pada sekitar. |
| Data Cleaning | mohon buat perjelas payung hukum,supaya warga sekitar tetangga masyarakat setempat punya hak untuk mendobrak rumah tetangga jika terjadi indikasi kekerasan dan keanehan di rumah tersebut supaya warga tidak takut dan care pada sekitar |
| Data Tokenizing | ['mohon', 'buat', 'perjelas', 'payung', 'hukum', 'supaya', 'warga', 'sekitar', 'tetangga', 'masyarakat', 'setempat', 'punya', 'hak', 'untuk', 'mendobrak', 'rumah', 'tetangga', 'jika', 'terjadi', 'indikasi', 'kekerasan', 'dan', 'keanehan', 'di', 'rumah', 'tersebut', 'supaya', 'warga', 'tidak', 'takut', 'dan', 'care', 'pada', 'sekitar'] |
| Data Filtering | ['payung', 'hukum', 'warga', 'tetangga', 'masyarakat', 'hak', 'mendobrak', 'rumah', 'tetangga', 'indikasi', 'kekerasan', 'keanehan', 'rumah', 'warga', 'takut', 'care'] |
| Data Stemming | ['payung', 'hukum', 'warga', 'tetangga', 'masyarakat', 'hak', 'dobrak', 'rumah', 'tetangga', 'indikasi', 'keras', 'keanehan', 'rumah', 'warga', 'takut', 'care'] |

#### 3. Labelling

Tabel Hasil Labelling
| Text | Label | Klasifikasi |
| --- | --- | --- |
| sambang obyek vital bhabinkamtibmas aiptu sisw... | 1 | Positif |
| arah kudeta bos polri tni diam gerak tangkap t... | 0 | Netral |
| tinggal kipi berat banding hidup sehat | 0 | Netral |
| kasih contoh polisi | 0 | Netral |
| pantesan lawan kakak tunggu sakit | 0 | Netral |

#### 4. Feature Extractions

Tabel Hasil Feature Extractions
| aiptu | aman | aneh | arah | barat | bhabinkamtibmas | care | cari | cocok | dobrak | ... | sehat | siswanto | takut | terap | tertib | tetangga | usul | victim | vital | warga |
|-------|------|------|------|-------|-----------------|------|------|-------|--------|-----|-------|----------|-------|-------|--------|----------|------|-------|-------|-------|
| 0     | 0    | 0    | 1    | 1     | 0               | 0    | 1    | 1     | 0      | ... | 0     | 0        | 0     | 0     | 0      | 0        | 1    | 1      | 0     | 0     |
| 0     | 0    | 1    | 0    | 0     | 0               | 1    | 0    | 0     | 1      | ... | 0     | 1        | 0     | 0     | 2      | 0        | 0    | 0      | 2     | 0     |
| 1     | 1    | 0    | 0    | 0     | 1               | 0    | 0    | 0     | 0      | ... | 1     | 0        | 1     | 1     | 0      | 1        | 0    | 1      | 0     | 1     |
Keterangan:
- 0: Tidak muncul dalam teks
- 1: Muncul dalam teks
- angka: Frekuensi kemunculan dalam teks

#### 5. Split Data
#### 6. Model

### Kesimpulan


## Technologies Used
- Google Colab
- Python
- NumPy
- Pandas
- TensorFlow
- Matplotlib
- Scikit-learn

## Features


## Setup


## Usage


## Project Status
Proyek sudah selesai dilaksanakan dan mendapatkan Nilai A pada mata kuliah Text Mining.

## Room for Improvement
Kedepannya, proyek dapat dikembangkan dan dilanjutkan ke tahap deployment. Dapat menggunakan Streamlit untuk deployment sehingga model dapat dijalankan untuk prediksi data baru.

## Acknowledgements
Terima kasih kepada Azmi selaku partner saya dalam mengerjakan proyek mata kuliah ini.

## Contact
Created by [@taufiksatrian](https://github.com/taufiksatrian) - feel free to contact me!
