# Praktikum Big Data - 1

Setup Environment & Git Workflow
- Track: Spark + Cloud (Industry Ready)

## 📖 Deskripsi Proyek

Repositori ini merupakan hasil pengerjaan Modul Praktikum 1, yang bertujuan untuk membangun fondasi lingkungan kerja seorang Data Engineer modern. Praktikum ini tidak sekadar tentang instalasi software, tetapi tentang membangun mindset komputasi terdistribusi, kesiapan integrasi cloud, dan alur kerja profesional.

## 🛠️ Teknologi yang digunakan

- **Bahasa Pemrograman: Python 3.10+**
- **Code Editor: Visual Studio Code (VS Code)**
- **CLI / Terminal: PowerShell**
- **Distributed Processing Engine: PySpark**
- **Cloud Database: MongoDB Atlas (Free Tier)**
- **Version Control: Git & GitHub**

## 📂 Struktur Direktori

```bash
bigdata-project/
├── cloud_storage/      # Simulasi penyimpanan cloud lokal
├── data/               # Folder untuk dataset raw/processed
├── notebooks/          # Jupyter notebooks untuk eksplorasi
├── reports/            # Output laporan/analisis
├── scripts/            # Skrip utama Python
│   ├── simple_job.py   # Skrip job PySpark sederhana
│   └── test_mongo.py   # Skrip pengujian koneksi database
├── requirements.txt    # Daftar dependensi library
└── README.md           # Dokumentasi proyek ini
```

## 🚀 Panduan Setup & Instalasi

### 1. Persiapan Environment Lokal
- Pastikan Python 3.10+, Git, dan VS Code sudah terinstal.
- Buka folder proyek ini di VS Code.
- Buka terminal terintegrasi (gunakan PowerShell Ctrl + \`` atau Ctrl + J`).

### 2. Instalasi Library PySpark & PyMongo

- Jalankan perintah berikut di terminal untuk menginstal engine pemrosesan dan driver database:
```bash
pip install pyspark pymongo
```

### 3. Konfigurasi MongoDB Atlas

- Cluster MongoDB Atlas (M0 Free Tier) harus berstatus ACTIVE.
- Pastikan Network Access diset ke 0.0.0.0/0 (Allow Access from Anywhere).
- bah connection string di dalam file scripts/test_mongo.py menggunakan kredensial (username & password) milik Anda sendiri.

## 💻 Panduan Menjalankan Skrip

### Test Koneksi Database
untuk memastikan proyek berhasil terhubung dengan cloud database MongoDB Atlas:
```bash
python scripts/test_mongo.py
# (Output yang diharapkan: "Pinged your deployment. You successfully connected to MongoDB!")
```
### Menjalankan PySpark Job
untuk menjalankan simulasi pemrosesan data secara terdistribusi menggunakan PySpark:
```bash
python scripts/simple_job.py
#(Output yang diharapkan: Tabel hasil agregasi "sum(value)" berdasarkan "category" tanpa ada pesan error).
```
### Output yang Diharapkan
File `simple_job.py` mendemonstrasikan operasi dasar PySpark
```
+--------+----------+
|category|sum(value)|
+--------+----------+
|       B|        20|
|       A|        40|
+--------+----------+
```

## ✅ Checklist Pengumpulan (Validasi)

- [ ] PySpark berhasil berjalan tanpa error merah.
- [ ] MongoDB Atlas, Cluster berstatus ACTIVE.
- [ ] Tautan repositori GitHub (Public & bisa diakses).
- [ ] File kode simple_job.py sudah lengkap dan ada di dalam folder scripts.
- [ ] Output tabel agregasi Spark muncul dengan benar.

## 👨‍💻 Author

**Achmad Fauzil 'Adhim**
- GitHub: [@Nouzaria](https://github.com/Nouzaria)

## 📄 Lisensi

Proyek ini dibuat untuk keperluan pembelajaran dan praktikum Big Data.

## 📚 Referensi

- [Apache Spark Documentation](https://spark.apache.org/docs/latest/)
- [PySpark Documentation](https://spark.apache.org/docs/latest/api/python/)
- [PySpark Getting Started](https://spark.apache.org/docs/latest/api/python/getting_started/index.html)

---

⭐ Jangan lupa berikan star jika repositori ini membantu!