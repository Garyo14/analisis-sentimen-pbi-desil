# Analisis Sentimen Publik terhadap Penonaktifan PBI JKN Berbasis Desil

Analisis sentimen dan isu komunikasi publik terhadap kebijakan penonaktifan
peserta PBI JKN berdasarkan desil DTSEN, menggunakan komentar YouTube dari
kanal berita nasional.

> **Status: dalam pengerjaan.** Dashboard dan ringkasan eksekutif akan
> ditautkan di sini setelah analisis selesai.

---

## 1. Latar Belakang
Pemerintah memperbarui kepesertaan Penerima Bantuan Iuran Jaminan Kesehatan
(PBI JK) berdasarkan Data Tunggal Sosial Ekonomi Nasional (DTSEN). Peserta
yang tidak lagi berada di kelompok desil penerima bantuan dinonaktifkan,
sehingga memicu diskusi publik yang luas, termasuk kebingungan istilah dan
isu salah sasaran. Proyek ini memetakan sentimen dan isu yang muncul di
kolom komentar sebagai gambaran risiko komunikasi kebijakan.

## 2. Pertanyaan Analisis
1. Bagaimana distribusi sentimen publik terhadap kebijakan ini?
2. Isu (aspek) apa yang paling memicu sentimen negatif?
3. Bagaimana perbedaan sentimen antar-periode dan antar-kanal?
4. Seberapa banyak komentar yang mengandung informasi keliru?

## 3. Data
| Item | Keterangan |
|---|---|
| Sumber | Komentar YouTube (YouTube Data API v3) |
| Kanal | KompasTV, Najwa Shihab, CNN Indonesia, Narasi |
| Periode analisis | Februari 2026 dan Oktober-November 2026 |
| Jumlah video | _akan diisi_ |
| Tanggal pengambilan data | _akan diisi_ |
| Komentar mentah | _akan diisi_ |
| Setelah cleaning dan filter relevansi | _akan diisi_ |

Username pengguna tidak disimpan untuk menjaga privasi.

## 4. Metodologi (rencana)
1. Pengumpulan komentar via YouTube Data API
2. Cleaning: hapus duplikat, URL, komentar terlalu pendek; normalisasi slang;
   filter relevansi topik
3. Klasifikasi sentimen (positif/netral/negatif) dengan model pre-trained
4. Validasi dengan pelabelan manual pada sampel komentar
5. Klasifikasi aspek berbasis kamus kata kunci
6. Visualisasi dengan dashboard Looker Studio

## 5. Temuan Utama
_Akan diisi setelah analisis selesai._

## 6. Rekomendasi Komunikasi
_Akan diisi setelah analisis selesai._

## 7. Limitasi
- Komentar YouTube hanya mewakili audiens kanal tertentu, bukan seluruh publik
- Model sentimen dapat kesulitan mendeteksi sarkasme dan slang
- Kemungkinan terdapat komentar dari akun bot
- Klasifikasi berbasis kata kunci dapat melewatkan konteks
- Kebijakan terus berubah; analisis mencerminkan kondisi pada tanggal
  pengambilan data

## 8. Struktur Repo
- `data/` : daftar video dan data komentar (versi anonim)
- `notebooks/` : notebook pengambilan data hingga analisis
- `outputs/` : ringkasan eksekutif dan visualisasi
- `requirements.txt` : daftar pustaka Python

## 9. Tools
Python (pandas, transformers, Sastrawi), YouTube Data API v3,
Google Sheets, Looker Studio

## Kontak
Tegar Haryo | [LinkedIn](https://linkedin.com/in/tegarharyo) | haryotegar14@gmail.com
