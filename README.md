# Analisis Rantai Pasok (Supply Chain Analysis)

## Deskripsi Proyek
Proyek ini merupakan analisis data rantai pasok (*supply chain*) berbasis Python untuk memahami pola logistik, profitabilitas produk, kendala kualitas, serta performa pemasok. Melalui analisis data eksploratif (EDA), proyek ini menyajikan informasi berbasis data untuk optimasi operasional dan efisiensi biaya.

## Sumber Data
* **Sumber**: Dataset Kaggle (*Supply Chain Analysis*)
* **Ukuran**: 100 baris × 24 kolom
* **Informasi Utama**: Jenis produk, variabel keuangan (harga jual, biaya manufaktur, total pendapatan), logistik (*lead time*, moda transportasi, biaya pengiriman), serta indikator kualitas (*defect rate* dan hasil inspeksi).

## Tahapan Pengerjaan
1. **Pemuatan dan Pemeriksaan Data**: Pengimporan dataset, pemeriksaan tipe data, serta verifikasi nilai yang hilang (*missing values*) atau data duplikat.
2. **Pembersihan dan Rekayasa Fitur**:
   * Penyesuaian nama kolom agar konsisten dalam pemrosesan data.
   * Pembuatan variabel baru, seperti `profit` (pendapatan dikurangi biaya manufaktur dan pengiriman) serta selisih hari pengiriman (*shipping delay*).
3. **Analisis Agregasi (*Groupby Analysis*)**:
   * **Finansial**: Evaluasi total pendapatan dan keuntungan per kategori produk.
   * **Kualitas**: Penilaian tingkat cacat (*defect rate*) serta hasil inspeksi produk dari setiap pemasok.
   * **Logistik**: Perhitungan rata-rata waktu tunggu (*lead time*) dan efisiensi jalur pengiriman.
4. **Visualisasi Data**: Pembuatan grafik batang, distribusi, dan *heatmap* menggunakan Matplotlib serta Seaborn untuk memperjelas hasil analisis.

## Ringkasan Hasil Utama
* **Performa Finansial**: Kategori produk **Skincare** mencatatkan total pendapatan dan profit tertinggi dibandingkan kategori produk lainnya.
* **Evaluasi Pemasok**: Terdapat variasi *defect rate* dan *lead time* antar pemasok. Pemasok dengan *lead time* terpanjang tidak selalu menghasilkan produk dengan tingkat cacat terkecil.
* **Efisiensi Logistik**: Pemilihan jalur pengiriman dan moda transportasi menunjukkan perbedaan biaya yang signifikan serta berpengaruh langsung pada margin keuntungan bersih.

## Struktur Direktori Proyek
```text
├── data/
│   └── supply_chain_data.csv    # Dataset mentah dari Kaggle
├── notebooks/
│   └── supply_chain_analysis.ipynb  # Notebook analisis dan visualisasi
├── README.md                    # Dokumentasi proyek
└── requirements.txt             # Daftar pustaka yang dibutuhkan
```

## Alat dan Pustaka
* **Bahasa Pemrograman**: Python 3.x
* **Analisis Data**: Pandas, NumPy
* **Visualisasi Data**: Matplotlib, Seaborn
* **Lingkungan Kerja**: Google Colab / Jupyter Notebook

## Cara Menjalankan Proyek
1. Kloning repositori ke direktori lokal:
   ```bash
   git clone https://github.com/username/supply-chain-analysis.git
   ```
2. Masuk ke direktori proyek:
   ```bash
   cd supply-chain-analysis
   ```
3. Instal pustaka yang dibutuhkan:
   ```bash
   pip install -r requirements.txt
   ```
4. Buka file `notebooks/supply_chain_analysis.ipynb` di Google Colab atau Jupyter Notebook untuk menjalankan analisis.
