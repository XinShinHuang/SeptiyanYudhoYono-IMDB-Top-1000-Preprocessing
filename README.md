# IMDB Top 1000-Preprocessing
Repository ini berisi proses preprocessing dataset IMDB Top 1000 Movies.
Preprocessing dataset IMDB Top 1000: data cleaning, type conversion, sorting, dan EDA deskriptif untuk 1000 film terbaik.

## Tahapan Preprocessing
1.  Data Cleaning: Hapus Unnamed: 0, fix Rate 93 -> 9.3, handle NaN di Metascore
2.  Transformation & Sorting: Sorting Top 10 film berdasarkan Rate tertinggi
3.  EDA & Visualisasi: Distribusi Genre, Certificate, dan statistik deskriptif Rate

## Visualisasi
- Bar chart Top 10 Genre paling banyak
- Histogram distribusi Rate
- Boxplot Metascore vs Rate

## Dataset
- 1000 baris, 10 Kolom ( Sebelum Cleaning ) & 9 kolom ( Setelah Cleaning)
- Sumber: IMDB Top 1000

## Tools
Python, Pandas, Matplotlib/Seaborn, Jupyter Notebook






# Tugas 1 - Biner Water Potability

Ini tugas pertama, tentang klasifikasi biner pake dataset Water Potability.

Jadi maksudnya biner itu targetnya cuma ada 2 kelas aja. Di dataset ini targetnya itu Potability, isinya 0 sama 1. Kalau 0 artinya airnya tidak layak minum, kalau 1 artinya layak minum.

## Dataset yang dipakai

Datasetnya namanya Water Potability, saya ambil dari Kaggle.
Linknya: https://www.kaggle.com/datasets/adityakadiwal/water-potability

Isinya data tabular / angka, bukan teks bukan gambar. Jumlah datanya 3276 baris, kolomnya ada 10, 9 fitur sama 1 target.

Kolom-kolomnya:
- ph
- Hardness
- Solids
- Chloramines
- Sulfate
- Conductivity
- Organic_carbon
- Trihalomethanes
- Turbidity
- Potability (ini targetnya)

## Fitur sama Target

Yang saya pake buat fitur (X) itu 9 kolom, yaitu ph sampe Turbidity semua.

Terus targetnya (y) cuma 1, yaitu Potability:
- 0 = Tidak Layak
- 1 = Layak

## File yang ada di repo ini

- 1_Biner_Water_Potability.ipynb -> notebook utama, isinya dari awal sampe akhir
- water_potability.csv -> file datasetnya

## Langkah-langkahnya di notebook

CELL 1: Identifikasi dataset, nampilin jumlah data, nama kolom, fitur, target, sama isi labelnya. Dari sini udah keliatan kalau ini biner.

CELL 2: EDA sama cek missing. Di sini saya cek data kosong per kolom, ternyata ada yang kosong di ph, Sulfate, sama Trihalomethanes. Terus liat jumlah per kelas sama bikin bar chart distribusi target, sama heatmap korelasi antar fitur.

CELL 3: Preprocessing sama split. Data yang kosong saya isi pake rata-rata tiap kolom. Terus dibagi jadi train 80% sama test 20% pake stratify biar rasio kelasnya tetap sama.

CELL 4: Training model. Fiturnya saya scaler dulu pake StandardScaler biar skalanya sama. Terus saya coba 2 model, Logistic Regression sama Random Forest, terus dibandingin akurasinya. Yang paling tinggi yang dipilih jadi model terbaik.

CELL 5: Evaluasi. Saya evaluasi pake classification report sama confusion matrix, terus saya simpulin kalau ini emang klasifikasi biner karena targetnya cuma 2 kelas.

## Cara jalaninnya

1. Taruh file water_potability.csv sama file ipynb-nya di 1 folder yang sama
2. Buka file 1_Biner_Water_Potability.ipynb di VS Code
3. Pilih kernel Python 3.13.3
4. Jalanin dari CELL 1 sampe CELL 5 urut, jangan diloncat
5. Kalau ada error No module named, install dulu di terminal:
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

## Hasil Evaluasi

Buat nilainya saya pake:
- Accuracy, buat liat seberapa banyak yang ketebak bener
- Classification report, buat liat precision, recall, f1 per kelas
- Confusion matrix, buat liat mana yang ketebak bener sama yang salah

## Kesimpulan

Jadi dari tugas ini bisa disimpulin kalau ini emang klasifikasi biner, karena target Potability-nya cuma ada 2 kelas, 0 sama 1. Nggak ada kelas lain.

## Tools

Python, VS Code / Jupyter Notebook, Pandas, Numpy, Matplotlib, Seaborn, Scikit-learn

## Author
XinShinHuang
