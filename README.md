# Submission Final - Analisis Sentimen Review Aplikasi Klik Indomaret

## Judul Proyek
Analisis Sentimen Review Pengguna Aplikasi **Klik Indomaret** di Google Play Store.

## Sumber Data
Data dikumpulkan secara mandiri melalui scraping review Google Play Store menggunakan library `google-play-scraper`.

- Nama aplikasi: Klik Indomaret
- Package ID: `com.indomaret.klikindomaret`
- URL sumber: `https://play.google.com/store/apps/details?id=com.indomaret.klikindomaret`
- Notebook scraping: `notebook_1_pengumpulan_data.ipynb`
- Dataset raw: `raw_review_klikindomaret_playstore.csv`
- Dataset final: `dataset_review_klikindomaret_playstore.csv`

## Pembagian Notebook

1. `notebook_1_pengumpulan_data.ipynb`
   - Hanya berisi proses scraping review Google Play Store.
   - Menyimpan hasil scraping mentah ke `raw_review_klikindomaret_playstore.csv`.
   - Menampilkan jumlah raw data sebelum preprocessing.

2. `notebook_2_pelatihan_model.ipynb`
   - Membaca raw data dari notebook 1.
   - Melakukan preprocessing teks: lowercasing, penghapusan URL, mention, hashtag, angka, punctuation, karakter non-huruf, stopword removal, dan stemming.
   - Melakukan labeling sentimen berbasis lexicon dari `sentiment_lexicon_indonesia.csv`.
   - Menyimpan dataset final ke `dataset_review_klikindomaret_playstore.csv`.
   - Melatih dan mengevaluasi model machine learning.

## Catatan Perbaikan

- Label `sentiment` dibuat dari **isi teks review**, bukan dari `rating`.
- Kolom `rating` hanya disimpan sebagai metadata.
- Proses scraping dipisahkan dari preprocessing dan labeling.
- `requirements.txt` sudah menggunakan versi spesifik untuk mengurangi risiko dependency conflict.

## Cara Menjalankan

```bash
pip install -r requirements.txt
```

Kemudian jalankan notebook secara berurutan:

1. `notebook_1_pengumpulan_data.ipynb`
2. `notebook_2_pelatihan_model.ipynb`

## Isi Berkas

- `notebook_1_pengumpulan_data.ipynb`: scraping dan penyimpanan raw data.
- `notebook_2_pelatihan_model.ipynb`: preprocessing, labeling, training, evaluasi, dan inference.
- `raw_review_klikindomaret_playstore.csv`: raw hasil scraping.
- `dataset_review_klikindomaret_playstore.csv`: dataset final hasil preprocessing dan labeling.
- `sentiment_lexicon_indonesia.csv`: lexicon sentimen yang digunakan untuk labeling.
- `requirements.txt`: dependensi Python dengan versi spesifik.
- `schema_dataset.md`: skema dataset final.
"# DeepL_KlikIndomaret_AnalisisSentimen" 
