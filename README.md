# Peramalan Kunjungan Harian Rumah Sakit

Tugas Analisis Deret Waktu tentang peramalan jumlah kunjungan harian rumah sakit dengan membandingkan metode SARIMA dan Prophet. Repositori ini berisi notebook analisis untuk tahap awal, yaitu membaca data, menguji stasioneritas, dan differencing.

## Struktur folder

```
peramalan-kunjungan-harian/
├── data/            
├── notebooks/       
├── .gitignore
├── requirements.txt
└── README.md
```

Folder `data/` tidak ikut diunggah ke GitHub karena berisi data rumah sakit. Folder ini sengaja dikecualikan lewat `.gitignore`.

## Data

Data harus ditaruh manual di folder `data/` dengan nama file:

```
Harian_Total_2023_sd_2026.xlsx
```

File ini berisi data harian dari 1 Januari 2023 sampai 13 Oktober 2026 dengan kolom `no`, `tanggal`, `ri`, `rj`, `jk`, `jp`, `bpjs`, `umum`, `asuransi`, `px_baru`, `px_lama`, `bulan`, dan `tahun`. Variabel yang diramalkan adalah `jk` (jumlah kunjungan). Data bisa diminta ke [nama pemilik data / dosen].

## Cara menjalankan

1. Clone repositori ini, lalu masuk ke foldernya.

```powershell
git clone https://github.com/USERNAME/peramalan-kunjungan-harian.git
cd peramalan-kunjungan-harian
```

2. Buat virtual environment dan pasang paket yang dibutuhkan.

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

3. Taruh file data di folder `data/` sesuai nama di atas.

4. Buka notebook di folder `notebooks/` dengan VS Code, pilih kernel `.venv`, lalu jalankan semua sel. Path data di notebook diatur ke `../data/Harian_Total_2023_sd_2026.xlsx`.

## Isi analisis

- Membaca data dan memastikan tidak ada tanggal yang hilang
- Uji stasioneritas dengan ADF dan KPSS (level dan trend)
- Visualisasi pola tren, simpangan baku, level bulanan, pola mingguan, dan ACF
- Differencing musiman lag 7 dan uji ulang stasioneritas

## Penyusun

Aurel Maritza Maheswari Ahmad - 24083010011