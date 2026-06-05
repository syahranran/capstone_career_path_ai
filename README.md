# Career Path Predictor (Deep Learning )

Aplikasi Deep Learning berbasis **TensorFlow Functional API** yang dirancang untuk memprediksi **Top-3 Alternatif Karier Terbaik** berdasarkan jawaban kuesioner dari 10 pertanyaan psikometrik atau minat bakat.

---

## Ringkasan Dataset & Proyek
* **Sumber Data:** Gabungan data dari **Kaggle** (`kaggle`) dan data buatan (`dummy`) untuk pemodelan jalur karier.
* **Ukuran Data:** 1.180 baris data dengan 12 kolom (10 pertanyaan kuesioner `Q1` - `Q10`, 1 kolom target `career`, dan 1 kolom `source`).
* **Fitur Utama:** Rekomendasi tidak hanya berfokus pada 1 pilihan tunggal (*Top-1*), melainkan mengekstrak 3 probabilitas tertinggi (*Top-3*) untuk memberikan alternatif karier yang lebih fleksibel bagi pengguna.

---

##  Eksperimen & Arsitektur Model

Proyek ini mengeksperimentasikan 3 arsitektur Neural Network yang berbeda untuk mencari performa terbaik:

| Model | Karakteristik / Arsitektur | Train Accuracy | Validation Accuracy | Status Akhir |
| :--- | :--- | :---: | :---: | :--- |
| **Model 1** | **Baseline Model:** Arsitektur standar sederhana dengan optimizer Adam default. | 53.30% | 52.54% | Stabil, tapi performa rendah |
| **Model 2** | **Deeper & Wider:** Struktur diperdalam dan diperlebar tanpa regularisasi. | 73.49% | 53.39% | Overfitting (Menghafal data) |
| **Model 3** | **Regularized Model:** Menggunakan Dropout Layer & Batch Normalization (Learning Rate: 0.001). | **66.42%** | **57.20%** | **Terbaik & Paling Optimal** |

##  REST API Architecture (Rencana Deployment)

Model TensorFlow (`.keras` / `.h5`) yang telah dilatih dapat diintegrasikan ke dalam layanan **REST API** berbasis **FastAPI** atau **Flask** untuk melayani prediksi secara real-time.
> **Evaluasi Akhir:** Model 3 dipilih sebagai model final dan berhasil mencetak akurasi sebesar **55.08% pada Test Set** (data uji yang benar-benar baru).

---
