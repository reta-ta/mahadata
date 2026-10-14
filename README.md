# mahadata
# Replikasi PySpark MLlib: Analisis Klasifikasi Log Keamanan Jaringan

Repositori ini dikembangkan guna memenuhi penugasan mandiri mata kuliah **Mahadata**

Proyek ini mereplikasi sebagian kerangka kerja dari jurnal internasional bereputasi mengenai pemanfaatan analitik data terdistribusi untuk keamanan siber menggunakan kerangka Apache Spark (PySpark MLlib).

---

## Literatur Referensi Utama
- **Judul:** *Cybersecurity data science: an overview from machine learning perspective*
- **Penulis:** I. H. Sarker, A. S. M. Kayes, S. Badsha, H. Alqahtani, P. Watters, & A. Ng
- **DOI:** [10.1186/s40537-020-00318-5](https://doi.org/10.1186/s40537-020-00318-5)

---

## Alur Kerja & Metodologi Eksperimen
1. **Inisiasi Data (*Data Generation*):** Membangkitkan rekam jejak simulasi log jaringan (mencakup metrik ukuran muatan data, waktu tanggap sistem, serta status tingkat ancaman).
2. **Rekayasa Fitur (*Feature Engineering*):** 
   - Mengekstrak komponen temporal (`LogHour`) dari atribut waktu kejadian.
   - Mengonversi teks kategori koneksi menggunakan `StringIndexer`.
   - Menyusun matriks variabel terpadu lewat fungsi `VectorAssembler`.
3. **Pemodelan & Evaluasi:** Pelatihan algoritma **Decision Tree Classifier** dilanjutkan dengan pengukuran tingkat ketepatan ramalan (*Accuracy*) serta pencatatan durasi komputasi.

---

## Berkas di Dalam Repositori
- `EksperimenCybersecurityDT.ipynb` : Berkas utama notebook eksperimen PySpark.
- `requirements.txt` : Rincian pustaka pendukung lingkungan Python.
- `hasil_cybersecurity_dt.csv` : Rekapitulasi metrik evaluasi model.
- `README.md` : Dokumentasi penjelasan repositori.
