# 💼 SaaS Sales Data Cleaning & Preparation
**Capstone Project 2 – JCDS BSD Muhamad Farhan Budiana**

Proyek ini merupakan bagian dari Capstone Project yang berfokus pada proses *data cleaning* dan *data preparation* terhadap dataset penjualan perusahaan **Software as a Service (SaaS)**.  
Tujuannya adalah memastikan dataset siap digunakan untuk analisis eksploratif dan visualisasi di Tableau.

---

## 📊 **1. Deskripsi Proyek**
Perusahaan SaaS Company (fiktif) menyediakan perangkat lunak berbasis langganan untuk klien korporat.  
Data yang digunakan merupakan simulasi transaksi penjualan SaaS yang mencakup berbagai produk, pelanggan, wilayah, serta diskon yang diberikan.

Analisis ini bertujuan untuk memahami:
- Bagaimana hubungan antara **diskon, penjualan, dan profit margin**  
- Segmen dan wilayah mana yang paling menguntungkan  
- Persiapan data agar dapat digunakan di **Tableau Dashboard**

---

## 🧾 **2. Dataset**
- **Nama file:** `SaaS-Sales.csv` (raw)  
- **Hasil cleaning:** `SaaS-Sales-Clean.csv`  
- **Sumber data:** Kaggle – *AWS SaaS Sales Dataset*  
- **Periode waktu:** 2020–2023  
- **Ukuran data:** ±10.000 baris (simulasi transaksi)

### Kolom utama:
| Kolom | Deskripsi |
|--------|------------|
| `Order Date` | Tanggal transaksi penjualan |
| `Customer` | Nama pelanggan / perusahaan |
| `Segment` | Jenis pelanggan (SMB, Enterprise, Strategic) |
| `Region` | Wilayah penjualan (AMER, EMEA, APJ) |
| `Country` | Negara tempat pelanggan berada |
| `Product` | Nama produk SaaS |
| `Sales` | Nilai total penjualan |
| `Profit` | Keuntungan bersih |
| `Discount` | Potongan harga (%) |
| `Quantity` | Jumlah lisensi yang dijual |
| `Profit Margin` | Rasio keuntungan terhadap penjualan |

---

## 🧹 **3. Proses Data Cleaning (Jupyter Notebook)**
Notebook: `saas-sales-analisis.ipynb`

Langkah-langkah utama yang dilakukan:

### 🧩 a. Import & Initial Exploration
- Membaca dataset mentah menggunakan `pandas`  
- Mengecek struktur data, tipe kolom, dan jumlah missing values  
- Melihat ringkasan statistik awal dengan `.describe()`  

### 🔧 b. Data Type & Formatting
- Mengonversi kolom tanggal (`Order Date`, `Date Key`) menjadi `datetime`  
- Mengubah kolom numerik seperti `Sales`, `Profit`, dan `Discount` menjadi tipe `float`  
- Membersihkan kolom kategori dari spasi berlebih dan nilai duplikat  

### 🧭 c. Missing Values & Duplicates
- Menghapus baris duplikat berdasarkan `Order ID`  
- Mengisi nilai kosong dengan:
  - Median (untuk kolom numerik seperti `Profit`, `Discount`)  
  - “Unknown” (untuk kolom kategori seperti `Country` atau `Product`)

### 📈 d. Outlier Detection & Correction
- Mengidentifikasi anomali dengan boxplot & IQR  
- Menemukan nilai *Profit Margin* yang tidak realistis (>100%)  
- Menyesuaikan rumus perhitungan:  

### Dashboard
https://public.tableau.com/app/profile/muhamad.farhan.budiana/viz/DashboardSaaSSales-MuhamadFarhanBudiana/AWSSaaSSalesPerformanceDashboard?publish=yes
