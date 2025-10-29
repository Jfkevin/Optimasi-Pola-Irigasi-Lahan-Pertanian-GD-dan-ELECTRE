# 🌾 Optimasi Pola Irigasi Lahan Pertanian
### Menggunakan Algoritma Gradient Descent & Metode ELECTRE

> **Proyek Ujian Akhir Semester IF541-F (Expert System)**  
> Fakultas Teknik dan Informatika – Universitas Multimedia Nusantara  
> Semester Gasal 2024/2025  

---

## 👥 Anggota Kelompok 6
| Nama | NIM |
|------|------|
| Farrelius Kevin | 00000081783 |
| Merhandes Gunawan | 00000081070 |
| Genadi Ikhsan Jaya | 00000080773 |
| Nadhila Citra | 00000072495 |

---

## 🧠 Deskripsi Proyek

Proyek ini bertujuan untuk **mengoptimalkan pola irigasi lahan pertanian** agar distribusi air menjadi lebih efisien dan hasil panen meningkat.  
Pendekatan dilakukan dengan menggabungkan dua metode:

1. **Algoritma Gradient Descent** – digunakan untuk mencari *bobot optimal* dari setiap kriteria irigasi.  
2. **Metode ELECTRE (Elimination and Choice Translating Reality)** – digunakan untuk melakukan *pengambilan keputusan multi-kriteria (MCDM)* guna menentukan sistem irigasi terbaik.

Proyek ini dibuat menggunakan **Python (NumPy, Pandas, Matplotlib)**.

---

## 🎯 Tujuan
- Menggunakan **Gradient Descent** untuk optimasi bobot dalam menentukan prioritas kriteria.
- Menggunakan **ELECTRE** untuk menentukan pola irigasi terbaik berdasarkan hasil optimasi bobot.
- Mendapatkan sistem irigasi modern yang paling efisien terhadap kondisi lahan dan jenis tanaman.

---

## 🔍 Rumusan Masalah
1. Bagaimana algoritma Gradient Descent dapat digunakan untuk mengoptimalkan pola irigasi modern sehingga meningkatkan efisiensi distribusi air dan hasil panen?
2. Bagaimana metode ELECTRE dapat membantu menentukan sistem irigasi terbaik berdasarkan berbagai kriteria lahan pertanian?

---

## ⚙️ Metodologi

### 1️⃣ Tahap Optimasi Bobot (Gradient Descent)
- Inisialisasi bobot awal setiap kriteria.  
- Hitung fungsi tujuan dengan *penalty* L2 (Ridge Regularization).  
- Lakukan iterasi pembaruan bobot hingga konvergensi tercapai.  

> **Output:** Bobot optimal setiap kriteria (contoh hasil)
> 
| Kriteria | Bobot Optimal |
|-----------|---------------|
| Topografi | 0.1658 |
| Biaya Implementasi | 0.1604 |
| Efisiensi Air | 0.1711 |
| Jenis Tanah | 0.1818 |
| Jenis Tanaman | 0.1711 |
| Ketersediaan Air | 0.1497 |

---

### 2️⃣ Tahap Pengambilan Keputusan (ELECTRE)
- Normalisasi matriks keputusan.
- Pembobotan menggunakan hasil Gradient Descent.
- Hitung **Concordance** dan **Discordance Matrix**.
- Tentukan **Matriks Dominan** dan lakukan eliminasi alternatif.
- Dapatkan **alternatif terbaik (sistem irigasi paling efisien).**

---

## 💾 Dataset

| Sistem Irigasi | Topografi | Biaya Implementasi | Efisiensi Air | Jenis Tanah | Jenis Tanaman | Ketersediaan Air |
|----------------|------------|--------------------|----------------|---------------|----------------|------------------|
| Surface Irrigation | 4 | 2 | 5 | 4 | 3 | 5 |
| Sprinkler Irrigation | 5 | 3 | 4 | 5 | 4 | 4 |
| Drip Irrigation | 3 | 5 | 3 | 5 | 5 | 3 |
| Subsurface Irrigation | 3 | 5 | 4 | 5 | 5 | 3 |
| Center Pivot Irrigation | 4 | 4 | 5 | 4 | 4 | 4 |
| Lateral Move Irrigation | 4 | 4 | 5 | 5 | 4 | 4 |
| Rain Irrigation | 5 | 2 | 2 | 3 | 2 | 2 |
| Fog Irrigation | 3 | 5 | 4 | 3 | 5 | 3 |

---

## 📈 Hasil & Visualisasi

### 🔹 Perubahan Nilai Fungsi Tujuan
Menunjukkan proses konvergensi Gradient Descent menuju nilai minimum (*loss function*).

### 🔹 Optimasi Bobot
Visualisasi evolusi nilai bobot setiap kriteria selama proses iterasi.

### 🔹 Matriks Concordance & Discordance
Menampilkan tingkat dominasi antar alternatif berdasarkan kriteria berbobot.

### 🔹 Hasil Akhir
Sistem irigasi dengan skor **dominasi tertinggi** dari metode ELECTRE dianggap **paling optimal**.

---

