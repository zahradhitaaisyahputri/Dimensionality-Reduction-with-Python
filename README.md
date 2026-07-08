# Dimensionality-Reduction-with-Python

## Deskripsi Kasus

Project ini membahas penerapan **dimensionality reduction** pada dataset **Social Media Addiction vs Productivity**. Kasus yang diangkat adalah analisis hubungan antara kebiasaan penggunaan media sosial dengan tingkat produktivitas pengguna.

Masalah utama dalam kasus ini adalah data memiliki beberapa fitur numerik yang saling berkaitan, seperti waktu layar harian, durasi penggunaan media sosial, jam belajar, jam tidur, jumlah notifikasi, tingkat fokus, tingkat kecanduan, dan skor produktivitas. Jika seluruh fitur tersebut dianalisis secara langsung, pola data akan sulit dilihat karena jumlah dimensinya cukup banyak.

Dimensionality reduction digunakan untuk menyederhanakan data berdimensi tinggi menjadi bentuk 2D atau 3D. Dengan begitu, pola penyebaran data dan kemungkinan terbentuknya kelompok pengguna dapat diamati dengan lebih mudah melalui visualisasi.

## Dataset yang Digunakan

Dataset yang digunakan adalah **Social Media Addiction vs Productivity Dataset**. Dataset ini berisi data perilaku pengguna yang berkaitan dengan penggunaan media sosial dan produktivitas.

Beberapa fitur yang digunakan dalam analisis ini antara lain:

- `age`
- `daily_screen_time`
- `social_media_hours`
- `study_hours`
- `sleep_hours`
- `notifications_per_day`
- `focus_score`
- `addiction_level`
- `productivity_score`

Pada project ini, fitur numerik digunakan sebagai input untuk proses dimensionality reduction. Kolom `addiction_level` digunakan sebagai label warna pada visualisasi agar pola tingkat kecanduan media sosial dapat diamati dengan lebih jelas.

## Ringkasan Metode

Metode dimensionality reduction yang digunakan dalam project ini adalah **PCA** dan **t-SNE**.

### 1. PCA 2D

PCA atau **Principal Component Analysis** digunakan untuk mereduksi beberapa fitur numerik menjadi dua komponen utama. Sebelum PCA diterapkan, data terlebih dahulu distandarisasi menggunakan `StandardScaler` agar setiap fitur berada pada skala yang seimbang.

PCA 2D menghasilkan dua komponen utama, yaitu `principal_component_1` dan `principal_component_2`. Visualisasi PCA 2D digunakan untuk melihat gambaran umum penyebaran data berdasarkan tingkat `addiction_level`.

### 2. PCA 3D

Selain PCA 2D, project ini juga menerapkan PCA 3D dengan menggunakan tiga komponen utama. PCA 3D digunakan agar informasi yang ditampilkan lebih banyak dibandingkan visualisasi 2D.

Pada visualisasi PCA 3D, setiap titik mewakili satu pengguna, sedangkan warna menunjukkan kategori `addiction_level`. Dengan tambahan komponen ketiga, pola penyebaran data dapat diamati dari sudut yang lebih luas.

### 3. t-SNE 2D

t-SNE atau **t-Distributed Stochastic Neighbor Embedding** digunakan untuk mereduksi data menjadi dua dimensi dengan mempertahankan kemiripan antar data. Data yang memiliki karakteristik mirip akan ditempatkan berdekatan, sedangkan data yang berbeda akan ditempatkan lebih jauh.

Berbeda dengan PCA yang bersifat linear, t-SNE lebih cocok digunakan untuk melihat pola data yang kompleks dan kemungkinan terbentuknya cluster.

## Analisis Hasil

Berdasarkan hasil visualisasi PCA 2D, data berhasil direduksi menjadi dua komponen utama. PCA membantu memberikan gambaran umum mengenai penyebaran data berdasarkan fitur-fitur perilaku pengguna. Hasil PCA juga dapat dijelaskan melalui nilai **explained variance ratio**, yaitu nilai yang menunjukkan seberapa besar informasi dari data asli yang berhasil dirangkum oleh komponen utama.

Pada PCA 2D, dua komponen utama mampu merangkum sebagian informasi dari data asli. Namun, visualisasi ini belum tentu mampu memisahkan kategori `addiction_level` secara jelas. Jika titik dari kategori rendah, sedang, dan tinggi masih saling bercampur, berarti tingkat kecanduan media sosial belum dapat dipisahkan secara kuat hanya menggunakan dua komponen utama PCA.

Pada PCA 3D, visualisasi menjadi lebih informatif karena menggunakan tiga komponen utama. Dengan adanya tambahan komponen ketiga, informasi yang ditampilkan menjadi lebih banyak dibandingkan PCA 2D. Jika titik dengan warna yang sama terlihat berdekatan, maka pengguna dengan tingkat kecanduan yang sama memiliki karakteristik perilaku yang mirip. Namun, jika titik antar kategori masih bercampur, maka PCA belum mampu membentuk pemisahan cluster yang jelas.

Sementara itu, hasil t-SNE lebih fokus pada kemiripan antar data. Pada visualisasi t-SNE, data yang memiliki karakteristik mirip akan ditempatkan saling berdekatan. Oleh karena itu, t-SNE lebih mudah digunakan untuk melihat kemungkinan adanya cluster atau kelompok pengguna berdasarkan perilaku penggunaan media sosial dan produktivitas.

Dalam kasus ini, t-SNE lebih sesuai digunakan untuk eksplorasi cluster karena hubungan antara penggunaan media sosial dan produktivitas tidak selalu bersifat linear. Produktivitas pengguna dapat dipengaruhi oleh beberapa faktor sekaligus, seperti durasi penggunaan media sosial, waktu layar harian, jam belajar, jam tidur, jumlah notifikasi, dan tingkat fokus.

Dengan demikian, PCA berguna untuk melihat gambaran umum data dan mengetahui seberapa besar informasi yang berhasil dirangkum. Sementara itu, t-SNE lebih sesuai untuk melihat pola pengelompokan pengguna secara visual.

## Kesimpulan

Dimensionality reduction membantu menyederhanakan data yang memiliki banyak fitur agar lebih mudah dianalisis dan divisualisasikan. Pada dataset **Social Media Addiction vs Productivity**, PCA dan t-SNE sama-sama dapat digunakan untuk memahami pola perilaku pengguna.

PCA lebih cocok digunakan untuk melihat struktur umum data dan merangkum informasi utama dari fitur asli. Sedangkan t-SNE lebih cocok digunakan untuk melihat pola cluster atau pengelompokan pengguna. Berdasarkan tujuan project, yaitu melihat pola pengguna berdasarkan tingkat kecanduan media sosial dan produktivitas, t-SNE menjadi metode yang lebih sesuai untuk eksplorasi cluster.
