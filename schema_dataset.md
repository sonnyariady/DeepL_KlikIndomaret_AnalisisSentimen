# Schema Dataset Final

File: `dataset_review_klikindomaret_playstore.csv`

| Kolom | Deskripsi |
|---|---|
| review_id | ID unik review dari Google Play Store |
| user_name | Nama pengguna pemberi review |
| review_date | Tanggal review dibuat |
| rating | Rating dari pengguna; hanya digunakan sebagai metadata, bukan sumber label |
| sentiment | Label sentimen hasil analisis teks: `positif`, `negatif`, atau `netral` |
| text | Teks review asli |
| clean_text | Teks hasil preprocessing |
| thumbs_up_count | Jumlah like/helpful pada review |
| review_created_version | Versi aplikasi saat review dibuat |
| app_version | Versi aplikasi yang tercatat pada review |
| developer_reply | Balasan developer jika tersedia |
| developer_reply_date | Tanggal balasan developer jika tersedia |
| source_app | Nama aplikasi sumber data |
| source_package | Package ID aplikasi |
| source_url | URL Google Play Store aplikasi |
| sumber_data | Keterangan metode pengumpulan data |

Catatan: preprocessing dan labeling dilakukan di `notebook_2_pelatihan_model.ipynb`.
