# Analisis Sentimen Publik terhadap Penonaktifan PBI JKN Berbasis Desil

Analisis sentimen dan isu komunikasi publik terhadap kebijakan penonaktifan
peserta PBI JKN berdasarkan desil DTSEN, menggunakan komentar YouTube dari
kanal berita nasional.

**Dashboard:** [tautan Looker Studio]
**Ringkasan eksekutif:** [tautan PDF di folder outputs]

---

## 1. Latar Belakang
Pemerintah memperbarui kepesertaan PBI JKN berdasarkan Data Tunggal Sosial
Ekonomi Nasional (DTSEN). Peserta di luar kelompok desil penerima bantuan
dinonaktifkan, sehingga memicu diskusi publik yang luas. Proyek ini
memetakan sentimen dan isu yang muncul sebagai gambaran risiko komunikasi
kebijakan.

## 2. Pertanyaan Analisis
1. Bagaimana distribusi sentimen publik terhadap kebijakan ini?
2. Isu (aspek) apa yang paling memicu sentimen negatif?
3. Bagaimana perbedaan sentimen antar-periode dan antar-kanal?
4. Seberapa banyak komentar yang mengandung informasi keliru?

## 3. Data
| Item | Keterangan |
|---|---|
| Sumber | Komentar YouTube (YouTube Data API v3) |
| Kanal | [KompasTV, Najwa Shihab, CNN Indonesia, Narasi] |
| Jumlah video | [..] (daftar lengkap di `data/daftar_video.csv`) |
| Periode analisis | [Feb 2026] dan [Okt-Nov 2026] |
| Tanggal pengambilan data | [..] |
| Komentar mentah | [..] |
| Setelah cleaning dan filter relevansi | [..] |

Username pengguna tidak disimpan untuk menjaga privasi.

## 4. Metodologi
1. **Pengumpulan data:** pengambilan komentar via YouTube Data API
2. **Cleaning:** hapus duplikat, URL, dan komentar terlalu pendek; normalisasi
   slang; filter relevansi topik
3. **Sentimen:** model pre-trained [nama model] (positif/netral/negatif)
4. **Validasi:** pelabelan manual [..] komentar sampel, akurasi [..]%
5. **Analisis aspek:** klasifikasi berbasis kamus kata kunci
   (akurasi data, reaktivasi, keadilan, kebingungan desil, kepercayaan)
6. **Visualisasi:** dashboard Looker Studio

## 5. Temuan Utama
- [Temuan 1, dengan angka]
- [Temuan 2, dengan angka]
- [Temuan 3, dengan angka]

## 6. Rekomendasi Komunikasi
- [..]
- [..]

## 7. Limitasi
- Komentar YouTube hanya mewakili audiens kanal tertentu, bukan seluruh publik
- Model sentimen kesulitan mendeteksi sarkasme dan slang
- Kemungkinan ada komentar dari akun bot
- Klasifikasi aspek berbasis kata kunci dapat melewatkan konteks
- Kebijakan terus berubah; analisis mencerminkan kondisi per [tanggal]

## 8. Struktur Repo
```
├── data/
│   ├── daftar_video.csv
│   └── komentar_bersih_anonim.csv
├── notebooks/
│   ├── 01_pengambilan_data.ipynb
│   ├── 02_cleaning.ipynb
│   ├── 03_sentimen.ipynb
│   └── 04_analisis_aspek.ipynb
├── outputs/
│   └── ringkasan_eksekutif.pdf
└── README.md
```

## 9. Cara Menjalankan
1. Clone repo ini
2. Instal dependensi: `pip install -r requirements.txt`
3. Isi API key YouTube di file `.env` (tidak disertakan di repo)
4. Jalankan notebook sesuai urutan

## 10. Tools
Python (pandas, transformers, Sastrawi), YouTube Data API v3,
Google Sheets, Looker Studio

## Kontak
Tegar Haryo | [LinkedIn] | haryotegar14@gmail.com
