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
