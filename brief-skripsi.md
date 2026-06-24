# BRIEF SKRIPSI UNTUK CODEX

## Judul Penelitian

**Integrasi Sistem Akselerator CNN Berbasis Komputasi Fixed-Point 16-Bit pada Board FPGA**

---

## Tujuan Brief

Dokumen ini digunakan sebagai panduan bagi Codex untuk membantu menyempurnakan naskah skripsi berbasis LaTeX yang telah tersedia. Fokus utama bukan membuat ulang isi skripsi dari awal, melainkan melakukan perbaikan akademik, pelengkapan pembahasan, peningkatan konsistensi antar bab, serta menghasilkan penjelasan ilmiah yang sesuai dengan hasil penelitian yang sudah diperoleh.

Codex harus bertindak sebagai asisten penulis skripsi yang memahami konteks penelitian FPGA dan CNN, bukan sekadar generator teks.

---

# Konteks Penelitian

Penelitian ini mengimplementasikan sistem embedded vision berbasis FPGA yang terdiri atas:

* Board FPGA Digilent Arty A7-100T.
* Kamera OV7670.
* DDR SDRAM sebagai frame buffer.
* VGA PMOD Digilent sebagai display output.
* CNN accelerator berbasis Verilog.
* Representasi fixed-point 16-bit.
* Dataset MNIST grayscale 28×28.
* Training model dilakukan menggunakan Python.
* Inferensi dilakukan sepenuhnya di FPGA.

Kontribusi utama penelitian ini bukan sekadar implementasi CNN pada FPGA, melainkan integrasi seluruh subsistem menjadi sistem embedded vision end-to-end.

Aliran sistem:

OV7670
→ DDR Frame Buffer
→ ROI
→ CNN Accelerator
→ Argmax
→ VGA Display

---

# Struktur Proyek

Seluruh proyek menggunakan LaTeX.

Struktur direktori utama:

```
naskah-skripsi/
├── bab1.tex
├── bab2.tex
├── bab3.tex
├── bab4.tex
├── bab5.tex
├── lampiran.tex
├── daftar-pustaka.bib
├── template-skripsi.tex
├── gambar/
└── ...
```

Seluruh gambar yang digunakan berada pada folder:

```
./gambar/
```

Jangan mengubah struktur folder.

Jangan memindahkan gambar.

Gunakan path gambar yang sudah ada.

---

# Tugas Utama Codex

Codex bertugas melakukan:

1. Analisis konsistensi antar bab.
2. Penyempurnaan bahasa akademik.
3. Pelengkapan bagian yang masih lemah.
4. Penulisan pembahasan hasil.
5. Menjaga seluruh hasil penelitian tetap sama.
6. Tidak mengubah angka hasil eksperimen.

---

# Aturan Global

## Yang BOLEH dilakukan

* Memperbaiki tata bahasa Indonesia akademik.
* Memperjelas alur penjelasan.
* Menambah paragraf transisi.
* Menambahkan interpretasi ilmiah terhadap hasil.
* Menambahkan research gap.
* Menambahkan pembahasan kritis.
* Memperbaiki rumusan masalah.
* Memperbaiki tujuan penelitian.
* Memperjelas kontribusi penelitian.
* Menyesuaikan isi dengan sitasi yang sudah tersedia.
* Menambah sitasi dari daftar pustaka yang sudah ada.

---

## Yang TIDAK BOLEH dilakukan

Jangan pernah:

* Mengubah hasil eksperimen.
* Mengubah angka pada tabel.
* Mengubah isi gambar.
* Mengubah nilai akurasi.
* Mengubah nilai latency.
* Mengubah nilai resource FPGA.
* Mengubah hasil timing.
* Mengubah hasil power.
* Menghapus gambar.
* Menghapus tabel.
* Mengubah arsitektur CNN.
* Menambahkan eksperimen baru.
* Mengarang hasil yang tidak ada.

Jika suatu hasil tidak tersedia:

Tuliskan keterbatasannya.

Jangan mengada-ada.

---

# Analisis Kelemahan Skripsi yang Harus Diperbaiki

## 1. Rumusan Masalah (Prioritas Tinggi)

Rumusan masalah saat ini terlalu umum.

Perbaiki menjadi pertanyaan penelitian yang sesuai dengan metodologi.

Minimal mencakup:

1. Bagaimana merancang akselerator CNN fixed-point 16-bit pada FPGA?
2. Bagaimana mengintegrasikan kamera, DDR, VGA, dan CNN accelerator?
3. Bagaimana performa sistem dari sisi akurasi, latensi, resource, daya, dan kemampuan real-time?

---

## 2. Tujuan Penelitian (Prioritas Tinggi)

Tujuan penelitian saat ini terlalu umum.

Perbaiki agar sesuai dengan Bab III dan Bab IV.

Tujuan minimal mencakup:

* Merancang CNN accelerator fixed-point 16-bit.
* Mengintegrasikan subsistem embedded vision.
* Mengevaluasi akurasi.
* Mengevaluasi latensi.
* Mengevaluasi resource FPGA.
* Mengevaluasi konsumsi daya.
* Mengevaluasi kemampuan real-time.

---

## 3. Research Gap (Prioritas Sangat Tinggi)

Bab II belum menunjukkan gap penelitian secara eksplisit.

Tambahkan subsection atau paragraf akhir tinjauan pustaka yang membandingkan:

### Solovyev et al.

* Cyclone IV
* Fixed-point CNN
* OV7670
* VGA
* MNIST

Keterbatasan:

* Arsitektur sederhana.
* Tidak membahas integrasi DDR.
* Tidak membahas resource multiplexing mendalam.

### Qiu et al.

* ZC706
* VGG16
* Fixed-point 16-bit

Keterbatasan:

* Fokus akselerator.
* Tidak terintegrasi dengan sistem embedded vision.

### Navaneethan et al.

* OV7670
* VGA

Keterbatasan:

* Tidak memiliki CNN accelerator.

### Penelitian Ini

Mengintegrasikan:

OV7670

* DDR
* VGA
* CNN Accelerator
* Fixed-point 16-bit
* Time Multiplexing
* Arty A7-100T

sebagai sistem embedded vision end-to-end.

Research gap harus memperjelas kontribusi penelitian.

---

# Penyempurnaan Bab II

Urutan teori saat ini kurang natural.

Apabila memungkinkan, ubah menjadi:

Neural Network

↓

CNN

↓

Konvolusi

↓

ReLU

↓

Max Pooling

↓

Kuantisasi Fixed-Point

↓

MAC

↓

Time Multiplexing

↓

Shift Register

↓

FIFO

↓

FSM

↓

Backpressure

↓

DDR

↓

AXI

↓

MIG

↓

OV7670

↓

VGA

Urutan harus bergerak dari konsep algoritma menuju implementasi hardware.

---

# Penyempurnaan Bab III

Jangan mengubah metodologi.

Perbaiki hanya pada:

## Penambahan transisi antar subsection.

Misalnya:

Rancangan Sistem
→ Implementasi
→ Integrasi
→ Pengujian
→ Evaluasi.

Perjelas bahwa pengujian dilakukan secara bertahap:

Python

↓

Verilog

↓

Subsistem

↓

Integrasi penuh.

Tekankan alasan engineering:

Setiap blok diverifikasi sebelum integrasi.

---

# Penyempurnaan Bab IV (Prioritas Utama)

Bab IV mayoritas sudah memiliki gambar dan tabel.

Tugas Codex adalah menulis pembahasan ilmiah terhadap hasil tersebut.

Gunakan pola berikut.

---

## Untuk Gambar

Jangan hanya mendeskripsikan isi gambar.

Gunakan format:

### Paragraf 1

Menjelaskan apa yang ditampilkan gambar.

### Paragraf 2

Menginterpretasikan makna hasil.

### Paragraf 3

Menghubungkan dengan teori atau penelitian terdahulu.

---

## Untuk Tabel

Gunakan format:

### Deskripsi hasil.

Apa isi tabel.

### Analisis.

Mengapa hasil tersebut muncul.

### Implikasi.

Apa dampaknya terhadap sistem.

---

# Panduan Pembahasan Bab IV

## Dataset

Jelaskan bahwa distribusi dataset yang seimbang membantu mencegah bias model.

---

## Arsitektur CNN

Jelaskan alasan pemilihan model kecil:

* keterbatasan resource FPGA,
* tetap mempertahankan kemampuan ekstraksi fitur.

---

## Loss Training

Bahas:

* tren penurunan loss,
* konvergensi,
* tidak terjadi divergensi.

---

## Accuracy Training

Bahas:

* peningkatan akurasi,
* stabilitas model,
* kemampuan generalisasi awal.

---

## Confusion Matrix

Bahas:

* kelas dominan,
* kesalahan klasifikasi,
* kemiripan digit tertentu.

Jangan mengarang angka baru.

Gunakan hanya observasi visual.

---

## Parameter Model

Bahas:

* jumlah parameter kecil,
* cocok untuk FPGA,
* mengurangi kebutuhan memori.

---

## Evaluasi Python

Bahas:

* baseline software,
* acuan implementasi hardware.

---

## Kuantisasi

Bahas:

* tidak terjadi saturasi.
* fixed-point 16-bit cukup merepresentasikan parameter.
* F=14 menjaga resolusi pecahan.

---

## Resource FPGA

Bahas:

* DSP hampir penuh.
* LUT/FF masih tersedia.
* Time multiplexing berhasil menekan resource.

Tekankan trade-off:

resource vs latency.

---

## Timing

Bahas:

* WNS positif.
* Timing closure tercapai.
* Desain memenuhi constraint clock.

---

## Latency

Bahas:

* jumlah siklus dipengaruhi time multiplexing.
* Conv2 dan Conv3 menjadi bottleneck.
* trade-off throughput dan DSP.

---

## Power

Bahas:

* FPGA menunjukkan efisiensi daya.
* sesuai motivasi embedded vision.

Hubungkan dengan literatur FPGA vs GPU.

---

## Real-Time

Bahas:

* apakah throughput memenuhi kebutuhan aplikasi.
* implikasi terhadap embedded vision.

Jangan mengklaim lebih dari hasil aktual.

---

# Gaya Penulisan

Gunakan bahasa Indonesia akademik formal.

Hindari:

* "penulis merasa"
* "menurut penulis"
* "sangat bagus"
* "luar biasa"

Gunakan:

* "hasil menunjukkan"
* "dapat diamati"
* "mengindikasikan"
* "menggambarkan"
* "berdasarkan hasil pengujian"

Panjang pembahasan ideal:

* 2–4 paragraf per gambar.
* 2–3 paragraf per tabel.
* 150–300 kata per subsection Bab IV.

---

# Sitasi

Gunakan referensi yang sudah tersedia pada:

```
daftar-pustaka.bib
```

Prioritaskan:

* Solovyev et al.
* Qiu et al.
* Zhang et al.
* Guo et al.
* Abdelouahab et al.
* Navaneethan et al.
* Qasaimeh et al.
* Goodfellow.
* LeCun.

Jangan menambahkan referensi baru kecuali benar-benar diperlukan.

---

# Output yang Diharapkan

Untuk setiap perubahan:

1. Tampilkan file yang dimodifikasi.
2. Jelaskan alasan perubahan.
3. Berikan diff atau patch yang jelas.
4. Pastikan LaTeX tetap dapat dikompilasi.
5. Jangan menghapus label, caption, atau citation yang sudah ada.

Tujuan akhir adalah menghasilkan naskah skripsi yang siap diajukan kepada dosen pembimbing dan siap dipertahankan pada sidang skripsi tanpa mengubah hasil penelitian yang telah diperoleh.
