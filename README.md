# 🔍 Deteksi API (Object Detection)

API dan Model Deteksi Objek berbasis **YOLO / PyTorch** (`best.pt`).

---

## 📌 Daftar Isi
- [Prasyarat](#-prasyarat)
- [Struktur Direktori](#-struktur-direktori)
- [Panduan Instalasi & Menjalankan Projek](#-panduan-instalasi--menjalankan-projek)
  - [1. Clone Repository](#1-clone-repository)
  - [2. Buat Virtual Environment](#2-buat-virtual-environment)
  - [3. Aktifkan Virtual Environment](#3-aktifkan-virtual-environment)
  - [4. Install Dependencies](#4-install-dependencies)
  - [5. Jalankan Aplikasi / API](#5-jalankan-aplikasi--api)
- [Catatan & Troubleshooting](#-catatan--troubleshooting)

---

## 💻 Prasyarat

Pastikan perangkat Anda sudah terinstall:
- **Python 3.8+ / 3.10+**
- **Git**

---

## 📂 Struktur Direktori

```text
deteksi-api/
│
├── best.pt            # Bobot model terlatih (YOLO/PyTorch)
├── .gitignore         # Konfigurasi file yang diabaikan git
├── README.md          # Panduan dokumentasi projek
├── requirements.txt   # Daftar dependensi Python
├── foto_api.png       # Contoh gambar / dokumentasi API
├── image.png          # Gambar sampel uji
└── image1.png         # Gambar sampel uji
```

---

## 🚀 Panduan Instalasi & Menjalankan Projek

Ikuti langkah-langkah di bawah ini setelah melakukan clone repository:

### 1. Clone Repository
```bash
git clone https://github.com/Aldikurniawan19/deteksi-api.git
cd deteksi-api
```

### 2. Buat Virtual Environment
Buat virtual environment terisolasi untuk mengelola paket dependensi:
```bash
python -m venv venv
```

### 3. Aktifkan Virtual Environment
- **Windows (PowerShell / Command Prompt):**
  ```bash
  venv\Scripts\activate
  ```
- **Linux / macOS / Git Bash:**
  ```bash
  source venv/bin/activate
  ```

*(Jika virtual environment aktif, akan muncul tanda `(venv)` di awal baris terminal).*

### 4. Install Dependencies
Install seluruh library yang dibutuhkan:
```bash
pip install -r requirements.txt
```
> **Catatan:** Jika belum ada `requirements.txt`, Anda dapat menginstall dependensi umum YOLO:
> ```bash
> pip install ultralytics opencv-python fastapi uvicorn pillow
> ```

### 5. Jalankan Aplikasi / API
Jalankan file program/API utama Anda:

- **Jika menggunakan FastAPI / Uvicorn:**
  ```bash
  uvicorn main:app --reload --host 0.0.0.0 --port 8000
  ```
  Akses dokumentasi interaktif Swagger UI di browser: `http://localhost:8000/docs`

- **Jika menggunakan script Python langsung:**
  ```bash
  python main.py
  ```

---

## ⚙️ Catatan & Troubleshooting

- **File Model (`best.pt`)**: File bobot model berukuran ~19 MB. Pastikan file ini berada di root folder projek.
- **Eksekusi Script PowerShell di Windows**: Jika muncul error `ExecutionPolicy`, jalankan PowerShell sebagai Administrator lalu ketik:
  ```powershell
  Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
  ```

---

## 👤 Author
- **Aldi Kurniawan** - [@Aldikurniawan19](https://github.com/Aldikurniawan19)
