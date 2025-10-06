# UTS_DATAMINING_MIRZARAMADHAN_2310631170139

ini adalah sebuah proyek data mining yang bertujuan untuk membuat model prediksi harga mobil bekas menggunakan Regresi Linear.
Prosesnya dibagi menjadi tiga tahap utama:

1. Preprocessing Data:

Pembersihan (Cleaning): Data "kotor" dibersihkan. Kolom yang tidak relevan (Unnamed: 0, New_Price) dibuang. Tipe data yang salah (misalnya, Engine yang terbaca sebagai teks seperti "998 CC") diubah menjadi angka. Nilai yang kosong (missing values) diisi menggunakan median (untuk angka) dan modus (untuk jumlah kursi).

Analisis (EDA): Dilakukan visualisasi data untuk memahami distribusi harga dan dominasi jenis bahan bakar (Diesel & Bensin).

Transformasi: Fitur baru Car_Age (Umur Mobil) dibuat dari kolom Year agar lebih mudah dipahami model. Fitur Brand (Merek) diekstrak dari kolom Name. Data kategorikal seperti Lokasi, Tipe Bahan Bakar, dan Merek diubah menjadi format numerik menggunakan One-Hot Encoding.

2. Modelling (Pemodelan):

Data dibagi menjadi data fitur (X) yang akan digunakan untuk memprediksi, dan data target (y) yaitu Price.
Dataset kemudian dipecah lagi menjadi 80% data latih (untuk melatih model) dan 20% data uji (untuk menguji performa model).
Fitur-fitur numerik diskalakan (scaling) agar tidak ada fitur yang mendominasi hanya karena skalanya besar (misal: Kilometers_Driven vs Car_Age).
Sebuah model Regresi Linear dilatih menggunakan data latih tersebut.

3. Evaluation (Evaluasi):

Model yang sudah dilatih digunakan untuk memprediksi harga pada data uji yang belum pernah "dilihat" sebelumnya.
Hasil prediksi dievaluasi menggunakan beberapa metrik, dengan R-squared (R2) Score sebesar 0.5796. Ini berarti model tersebut dapat menjelaskan sekitar 58% dari variasi harga mobil bekas.
Dibuat juga visualisasi yang membandingkan nilai harga aktual dengan nilai prediksi untuk melihat seberapa baik performa model.

Secara keseluruhan, notebook ini mendemonstrasikan alur kerja standar dalam proyek machine learning: mulai dari data mentah, pembersihan, rekayasa fitur, pelatihan model, hingga evaluasi performa.
