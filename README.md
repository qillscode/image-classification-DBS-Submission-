# Klasifikasi Gambar Bunga (Flowers Dataset)

Proyek ini dibuat sebagai submission untuk kelas Fundamental Deep Learning di Dicoding, yang merupakan bagian dari program powered by DBS Foundation.

## Deskripsi Proyek
Proyek ini membangun model klasifikasi gambar untuk mengenali 5 jenis bunga:

- daisy
- dandelion
- roses
- sunflowers
- tulips

Model dilatih menggunakan TensorFlow, lalu diekspor ke beberapa format deployment:

- TensorFlow SavedModel
- TensorFlow Lite (TFLite)
- TensorFlow.js (TFJS)

## Struktur Direktori
```text
submission/
├── Notebook_Aqilla_Zeba_Fakhira.ipynb   # Notebook utama (training, evaluasi, export)
├── README.md
├── requirements.txt
├── saved_model/                          # Format TensorFlow SavedModel
│   ├── fingerprint.pb
│   ├── saved_model.pb
│   └── variables/
├── tfjs_model/                           # Format TensorFlow.js
│   └── model.json
└── tflite/                               # Format TensorFlow Lite
    ├── model.tflite
    └── label.txt
```

## Cara Menjalankan

### 1. Clone / buka proyek
Pastikan kamu berada di folder proyek `BFDL_Aqilla Zeba Fakhira`.

### 2. Buat virtual environment (opsional tapi disarankan)
```bash
python -m venv .venv
```

Aktivasi environment:

- Windows (PowerShell)
```bash
.venv\Scripts\Activate.ps1
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Jalankan notebook
Buka file `Notebook_Aqilla_Zeba_Fakhira.ipynb` menggunakan Jupyter Notebook atau VS Code, lalu jalankan sel dari awal hingga akhir.

## Output Model
Setelah proses training/export, artefak model tersedia di:

- `saved_model/` untuk kebutuhan TensorFlow Serving atau inferensi Python
- `tflite/model.tflite` untuk deployment mobile/edge
- `tfjs_model/` untuk deployment web berbasis JavaScript

Label kelas untuk model TFLite tersedia di `tflite/label.txt`.

## Dependencies
Daftar library dapat dilihat di file `requirements.txt`.
