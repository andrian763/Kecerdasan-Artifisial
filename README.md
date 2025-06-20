# 📧 Email Phishing and Spam Detection App

Repositori ini berisi proyek aplikasi klasifikasi email phishing dan spam menggunakan pendekatan **Naive Bayes manual** dengan antarmuka pengguna berbasis **Streamlit**. Aplikasi dapat membaca email dari akun Gmail pengguna, kemudian memproses dan mengklasifikasikan konten email berbahasa Inggris sebagai **Phishing**/**Safe** dan **Spam**/**Ham**.

---

## 🎯 Tujuan Proyek

- Mengimplementasikan **model klasifikasi teks** secara manual tanpa library ML eksternal
- Menerapkan **probabilistic reasoning** (Naive Bayes) untuk mendeteksi email berbahaya
- Menyediakan antarmuka interaktif berbasis **Streamlit**
- Mengintegrasikan aplikasi dengan **akun Gmail pengguna via IMAP**

---

## ⚙️ Fitur Aplikasi

- 🔐 Login ke akun Gmail pengguna
- 📥 Ambil dan proses hingga **50 email terakhir**
- 🔍 Deteksi bahasa email menggunakan `langdetect` (hanya bahasa Inggris)
- 🧠 Klasifikasi pesan email sebagai:
  - **Phishing** atau **Safe**
  - **Spam** atau **Ham**
- 📊 Tampilkan hasil klasifikasi secara interaktif di dalam Streamlit

---

## 🧠 Model yang Digunakan

Model dibangun secara manual berdasarkan algoritma **Naive Bayes** dengan teknik:
- Preprocessing teks (case folding, clean symbols, remove non-alpha)
- Pembuatan word frequency dictionary untuk masing-masing kelas
- Perhitungan peluang dengan Laplace smoothing
- Log-likelihood untuk menghindari underflow
- Dua model: `PhishingModel` dan `SpamModel` dilatih terpisah

---



