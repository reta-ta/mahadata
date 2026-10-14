# mahadata-spark-cybersecurity
# Replikasi PySpark MLlib: Cybersecurity Data Science & Log Classification

Repositori ini disusun untuk memenuhi **Tugas Eksplorasi Mandiri Mahadata / Big Data (IF25-40402)** di Institut Teknologi Sumatera (ITERA).

Eksperimen ini melakukan **replikasi parsial** dari jurnal ilmiah bereputasi Scopus Q1 mengenai analisis klasifikasi log keamanan jaringan menggunakan pemrosesan data terdistribusi berbasis Apache Spark (PySpark MLlib).

---

## Artikel Acuan
- **Judul Artikel:** *Cybersecurity data science: an overview from machine learning perspective*
- **Penulis:** I. H. Sarker, A. S. M. Kayes, S. Badsha, H. Alqahtani, P. Watters, & A. Ng
- **Jurnal:** *Journal of Big Data* (Springer Nature, 2020)
- **DOI:** [10.1186/s40537-020-00318-5](https://doi.org/10.1186/s40537-020-00318-5)

---

## Ringkasan Metodologi Eksperimen
1. **Data Generation & Ingestion:** Pembangkitan dataset simulasi log keamanan jaringan yang mencakup variabel ukuran data sumber (*SourceBytes*), ukuran data tujuan (*DestinationBytes*), protokol jaringan, waktu log, dan label ancaman.
2. **Preprocessing & Feature Engineering:**
   * Ekstraksi fitur temporal (`LogHour`) dari waktu log.
   * Pengkodean variabel kategorikal protokol menggunakan `StringIndexer`.
   * Perakitan vektor fitur menggunakan `VectorAssembler`.
3. **Model Training & Evaluation:** Pelatihan model **Decision Tree Classifier** serta evaluasi metrik akurasi (*Accuracy*) dan waktu eksekusi pelatihan.

---

## Struktur Berkas Repository
- `EksperimenCybersecurityDT.ipynb` : Notebook utama eksperimen PySpark.
- `requirements.txt` : Daftar pustaka Python yang dibutuhkan.
- `hasil_cybersecurity_dt.csv` : Berkas keluaran metrik hasil evaluasi model.
- `README.md` : Dokumentasi lengkap repositori.
