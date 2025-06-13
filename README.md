# EKSPLORASI-VARIATIONAL-AUTOENCODER-VAE-PADA-DATASET-FASHION-MNIST

# Ringkasan Hasil Eksplorasi
1. Model: Convolutional Variational Autoencoder (CVAE) dibangun dengan 3 lapis encoder dan decoder berbasis CNN.

2. Dataset: Fashion-MNIST (10 kelas pakaian grayscale 28x28 piksel).

3. Latent Space:

   Menggunakan dimensi 2 agar bisa divisualisasikan.

   Menunjukkan clustering alami berdasarkan kelas.

   Mampu digunakan untuk interpolasi visual yang smooth antar gaya.

4. Rekonstruksi:

   Citra hasil rekonstruksi cukup mirip dengan input asli.

   Detail halus sedikit hilang karena sifat probabilistik VAE.

5. Interpolasi:

   Hasil interpolasi menunjukkan transisi kontinu antar dua titik gaya (misalnya sepatu → sandal).

6. Refleksi Teknis:

   Dimensi laten kecil bagus untuk eksplorasi, tapi terbatas untuk kompleksitas tinggi.

   Tambahan KL divergence penting agar ruang laten terstruktur.

   Hasil agak blur, bisa ditingkatkan dengan VAE-GAN atau arsitektur lain.

# Petunjuk Eksekusi Kode
Persyaratan:
Pastikan Python telah terinstal dengan pustaka berikut:

pip install torch torchvision matplotlib

# Struktur File:
cvae_fashionmnist.py: skrip utama pelatihan dan visualisasi model.

# Menjalankan:
1. Jalankan seluruh skrip Python:

python cvae_fashionmnist.py

2. Skrip akan secara otomatis:

Melatih model selama 10 epoch.

Menampilkan visualisasi hasil rekonstruksi.

Menunjukkan visualisasi distribusi ruang laten.

Melakukan interpolasi di ruang laten dan menampilkan hasilnya.

📌 Catatan:
Latent dimension dapat diubah pada bagian model = CVAE(latent_dim=2) untuk eksperimen lebih lanjut.

Untuk menyimpan gambar hasil visualisasi, cukup tambahkan plt.savefig("nama_file.png") di fungsi visualisasi.
