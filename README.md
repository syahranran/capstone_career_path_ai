# Career Path Predictor (Deep Learning )

Aplikasi Deep Learning berbasis **TensorFlow Functional API** yang dirancang untuk memprediksi **Top-3 Alternatif Karier Terbaik** berdasarkan jawaban kuesioner dari 10 pertanyaan psikometrik atau minat bakat.

---

## Ringkasan Dataset & Proyek
* **Sumber Data:** Gabungan data dari **Kaggle** (`kaggle`) dan data buatan (`dummy`) untuk pemodelan jalur karier.
* **Ukuran Data:** 1.180 baris data dengan 12 kolom (10 pertanyaan kuesioner `Q1` - `Q10`, 1 kolom target `career`, dan 1 kolom `source`).
* **Fitur Utama:** Rekomendasi tidak hanya berfokus pada 1 pilihan tunggal (*Top-1*), melainkan mengekstrak 3 probabilitas tertinggi (*Top-3*) untuk memberikan alternatif karier yang lebih fleksibel bagi pengguna.

---

##  REST API Architecture (Rencana Deployment)

Model TensorFlow (`.keras` / `.h5`) yang telah dilatih dapat diintegrasikan ke dalam layanan **REST API** berbasis **FastAPI** atau **Flask** untuk melayani prediksi secara real-time.
> **Evaluasi Akhir:** Model 3 dipilih sebagai model final dan berhasil mencetak akurasi sebesar **55.08% pada Test Set** (data uji yang benar-benar baru).

---
## CARA MENJALANKAN MODEL DI COLLAB 
1. Clone Repository git clone [https://github.com/syahranran/capstone_career_path_ai/](https://github.com/syahranran/capstone_career_path_ai/)
cd capstone_career_path_ai
2. Gunakan berkas requirements.txt untuk menginstal seluruh pustaka yang dibutuhkan
3. Buka Code Model .ipynb
