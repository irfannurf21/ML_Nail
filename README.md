1. Dataset Preprocessing:
    Dataset gambar diunduh dari Kaggle, diekstrak, dan diproses menggunakan fungsi image_dataset_from_directory dari TensorFlow. Gambar diubah ukurannya menjadi 256x256 piksel dan dibagi menjadi set pelatihan dan validasi (80% untuk pelatihan, 20% untuk validasi).
    CNN Architecture:

2. Model CNN disusun menggunakan lapisan-lapisan berikut:
  - Rescaling: Normalisasi nilai piksel (0 hingga 1).
  - Convolutional Layers: Menggunakan lapisan konvolusi untuk mendeteksi fitur visual pada gambar, diikuti dengan MaxPooling untuk mengurangi dimensi.
  - Flatten Layer: Mengubah matriks hasil konvolusi menjadi vektor.
  - Dense Layers: Menggunakan lapisan fully connected untuk klasifikasi akhir, dengan output berupa softmax yang menghasilkan probabilitas untuk setiap kelas.

3. Model Compilation:
  - Model dikompilasi menggunakan optimizer Adam, dengan fungsi loss sparse_categorical_crossentropy dan metrik accuracy.

4. Model Training:
  - Model dilatih selama 50 epoch menggunakan dataset gambar untuk klasifikasi, dengan validasi dilakukan di setiap epoch.
    Evaluation and Prediction:

Setelah dilatih, model dievaluasi menggunakan dataset validasi, dan akurasi validasi dihitung.
Model kemudian digunakan untuk membuat prediksi pada gambar baru.
