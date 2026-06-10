# Dekomposisi QR

## Pengertian

Dekomposisi QR adalah metode untuk memfaktorkan suatu matriks menjadi dua matriks:

$$
A = QR
$$

dengan:

- $Q$ = matriks ortogonal
- $R$ = matriks segitiga atas (*upper triangular*)

Karena $Q$ ortogonal, maka berlaku:

$$
Q^TQ = I
$$

atau

$$
Q^{-1}=Q^T
$$

---

# Algoritma QR

Algoritma QR merupakan metode numerik yang umum digunakan untuk mencari seluruh nilai eigen (*eigenvalue*) suatu matriks.

Metode ini bekerja dengan melakukan dekomposisi QR secara berulang (*iteratif*) hingga matriks berubah menjadi bentuk segitiga atas.

---

## Langkah-Langkah Algoritma QR

Misalkan:

$$
A_0 = A
$$

Untuk setiap iterasi ke-$k$:

### 1. Faktorkan Matriks

$$
A_k = Q_kR_k
$$

### 2. Bentuk Matriks Baru

$$
A_{k+1}=R_kQ_k
$$

### 3. Ulangi

Lakukan proses tersebut sampai konvergen.

---

## Mengapa Algoritma QR Berhasil?

Karena:

$$
A_k = Q_kR_k
$$

maka

$$
R_k = Q_k^TA_k
$$

Substitusi ke:

$$
A_{k+1}=R_kQ_k
$$

menghasilkan:

$$
A_{k+1}=Q_k^TA_kQ_k
$$

Bentuk ini disebut **transformasi keserupaan** (*similarity transformation*).

Transformasi keserupaan tidak mengubah nilai eigen matriks.

Akibatnya:

$$
\lambda(A_{k+1})
=
\lambda(A_k)
$$

Setelah iterasi yang cukup banyak, elemen-elemen di bawah diagonal utama akan mendekati nol sehingga diperoleh matriks segitiga atas.

Nilai eigen dapat dibaca langsung dari diagonal utama matriks tersebut.

---

# Faktorisasi QR dengan Gram-Schmidt

Tujuan metode Gram-Schmidt adalah mengubah sekumpulan vektor bebas linier menjadi sekumpulan vektor ortonormal.

Misalkan matriks:

$$
A=
\begin{bmatrix}
a_1 & a_2 & \cdots & a_n
\end{bmatrix}
$$

dengan kolom-kolom:

$$
a_1,a_2,\ldots,a_n
$$

Kita ingin membentuk vektor:

$$
q_1,q_2,\ldots,q_n
$$

yang:

1. Saling ortogonal
2. Memiliki panjang 1 (normal)

---

# Langkah 1: Vektor Pertama

Ambil kolom pertama:

$$
a_1
$$

Hitung normanya:

$$
\|a_1\|
$$

Kemudian normalisasi:

$$
q_1=
\frac{a_1}{\|a_1\|}
$$

---

# Langkah 2: Vektor Kedua

Hilangkan komponen yang searah dengan $q_1$.

Hitung proyeksi:

$$
\text{proj}_{q_1}(a_2)
=
(q_1^Ta_2)q_1
$$

Hitung komponen tegak lurus:

$$
u_2
=
a_2-\text{proj}_{q_1}(a_2)
$$

Normalisasi:

$$
q_2=
\frac{u_2}{\|u_2\|}
$$

---

# Langkah ke-k (Generalisasi)

Untuk kolom ke-$k$:

$$
u_k
=
a_k
-
\sum_{i=1}^{k-1}
(q_i^Ta_k)q_i
$$

Kemudian normalisasi:

$$
q_k=
\frac{u_k}{\|u_k\|}
$$

---

# Membentuk Matriks Q

Setelah seluruh vektor ortonormal diperoleh:

$$
Q=
\begin{bmatrix}
q_1 & q_2 & \cdots & q_n
\end{bmatrix}
$$

Karena semua kolom ortonormal:

$$
Q^TQ=I
$$

---

# Membentuk Matriks R

Elemen-elemen matriks $R$ diperoleh dari hasil proyeksi selama proses Gram-Schmidt.

Bentuk umumnya:

$$
R=
\begin{bmatrix}
r_{11} & r_{12} & \cdots & r_{1n}\\
0 & r_{22} & \cdots & r_{2n}\\
0 & 0 & \ddots & \vdots\\
0 & 0 & \cdots & r_{nn}
\end{bmatrix}
$$

Matriks $R$ selalu berbentuk segitiga atas.

---

# Contoh Sederhana

Diberikan:

$$
A=
\begin{bmatrix}
3 & 1\\
4 & 2
\end{bmatrix}
$$

## Kolom Pertama

$$
a_1=
\begin{bmatrix}
3\\
4
\end{bmatrix}
$$

Norma:

$$
\|a_1\|
=
\sqrt{3^2+4^2}
=
5
$$

Sehingga:

$$
q_1=
\frac{1}{5}
\begin{bmatrix}
3\\
4
\end{bmatrix}
=
\begin{bmatrix}
\frac35\\
\frac45
\end{bmatrix}
$$

---

## Kolom Kedua

$$
a_2=
\begin{bmatrix}
1\\
2
\end{bmatrix}
$$

Proyeksi terhadap $q_1$:

$$
\text{proj}_{q_1}(a_2)
=
(q_1^Ta_2)q_1
$$

Hitung vektor tegak lurus:

$$
u_2
=
a_2-(q_1^Ta_2)q_1
$$

Kemudian normalisasi:

$$
q_2=
\frac{u_2}{\|u_2\|}
$$

---

# Hasil Akhir

Diperoleh:

$$
A=QR
$$

dengan:

- $Q$ matriks ortogonal
- $R$ matriks segitiga atas

---

# Ringkasan Cepat

1. Faktorkan:

$$
A=QR
$$

2. Matriks $Q$ ortogonal:

$$
Q^TQ=I
$$

3. Matriks $R$ segitiga atas.

4. Algoritma QR:

$$
A_k=Q_kR_k
$$

$$
A_{k+1}=R_kQ_k
$$

5. Setelah konvergen, diagonal utama matriks hasil berisi nilai eigen.

6. Gram-Schmidt digunakan untuk membentuk matriks $Q$.

---

# Rumus yang Wajib Hafal

$$
A=QR
$$

$$
Q^TQ=I
$$

$$
Q^{-1}=Q^T
$$

$$
A_{k+1}=R_kQ_k
$$

$$
A_{k+1}=Q_k^TA_kQ_k
$$

$$
q_1=\frac{a_1}{\|a_1\|}
$$

$$
u_k=
a_k-\sum_{i=1}^{k-1}(q_i^Ta_k)q_i
$$

$$
q_k=\frac{u_k}{\|u_k\|}
$$