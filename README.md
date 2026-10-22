# Maybank Media News - Named-Entity Recognition (NER) Service

Proyek ini adalah layanan pengolahan *Natural Language Processing* (NLP) berbasis Python untuk mengekstrak entitas bernama (*Named-Entity Recognition*) dari kliping berita online Maybank. Sistem ini dirancang secara end-to-end mulai dari analisis data (*profiling*), pengujian otomatis (*unit testing*), penyediaan *Backend API*, hingga antarmuka web interaktif untuk keperluan demonstrasi.

---

## 🚀 Fitur Utama
1. **Automated Data Profiling**: Memindai dan menganalisis kualitas dataset CSV secara otomatis (menghitung total baris, duplikat, *missing values*, dan distribusi bahasa).
2. **Evaluation Dataset Generator**: Menyaring artikel dengan panjang teks ideal (150–1000 karakter) dan mengekspor sampel acak terstandar ke dalam format `evaluation_examples.json`.
3. **Baseline NER Model**: Memanfaatkan model prapelatihan spaCy (`en_core_web_sm`) untuk mengekstrak entitas seperti Organisasi (`ORG`), Lokasi/Entitas Geopolitik (`GPE`), dan Tanggal (`DATE`).
4. **Automated Unit Testing**: Dilengkapi 5 skenario pengujian menggunakan pustaka `unittest` untuk memastikan validitas input, kontrak JSON, penanganan *error*, dan determinisme program.
5. **FastAPI Backend**: Menyediakan RESTful API endpoint (`/extract-entities`) dengan validasi tipe data berbasis Pydantic.
6. **Gradio Web Frontend**: Panel antarmuka web interaktif yang bersih (tanpa tombol *flag*) untuk memudahkan demonstrasi secara *real-time*.

---

## 🛠️ Teknologi yang Digunakan
* **Bahasa Pemrograman**: Python
* **Pengolahan Data**: Pandas, Glob
* **NLP / Machine Learning**: spaCy (`en_core_web_sm`)
* **Pengujian (Testing)**: Unittest
* **Backend API**: FastAPI, Uvicorn, Pydantic
* **Frontend UI**: Gradio

---

## 📂 Struktur Proyek
```text
├── evaluation_examples.json       # File evaluasi standar (Ground Truth)
├── main.py (atau Notebook)        # Skrip utama pipeline end-to-end
└── README.md                      # Dokumentasi proyek
