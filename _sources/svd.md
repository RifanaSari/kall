# Singular Value Decomposition (SVD)

## Pengertian

Singular Value Decomposition (SVD) adalah metode faktorisasi matriks yang menguraikan suatu matriks menjadi tiga matriks:

$$
A = U \Sigma V^T
$$

SVD banyak digunakan dalam:

- Kompresi gambar
- Machine Learning
- Pemrosesan sinyal
- Analisis data
- Reduksi dimensi

---

## Komponen SVD

### Matriks U

- Berukuran $m \times m$
- Matriks ortogonal
- Memenuhi:

$$
U^T U = I
$$

- Kolom-kolomnya disebut **vektor singular kiri**

### Matriks $\Sigma$

- Berukuran $m \times n$
- Matriks diagonal
- Berisi nilai singular

Bentuk umum:

$$
\Sigma=
\begin{bmatrix}
\sigma_1 & 0 & \cdots & 0\\
0 & \sigma_2 & \cdots & 0\\
\vdots & \vdots & \ddots & \vdots\\
0 & 0 & \cdots & \sigma_r
\end{bmatrix}
$$

dengan:

$$
\sigma_1 \ge \sigma_2 \ge \cdots \ge \sigma_r \ge 0
$$

### Matriks V

- Berukuran $n \times n$
- Matriks ortogonal
- Memenuhi:

$$
V^T V = I
$$

- Kolom-kolomnya disebut **vektor singular kanan**

---

## Hubungan dengan Eigenvalue

Nilai singular diperoleh dari akar eigenvalue matriks $A^TA$ atau $AA^T$.

$$
\sigma_i = \sqrt{\lambda_i}
$$

dengan:

- $\sigma_i$ = nilai singular ke-$i$
- $\lambda_i$ = eigenvalue ke-$i$

Fakta penting:

- Eigenvalue tak nol dari $A^TA$ dan $AA^T$ adalah sama.
- Banyaknya nilai singular tak nol sama dengan rank matriks.

$$
\text{rank}(A)
=
\text{jumlah nilai singular tak nol}
$$

---

# Algoritma SVD

## Langkah 1: Hitung $AA^T$

$$
AA^T
$$

Cari:

- Eigenvalue
- Eigenvector

Eigenvector yang diperoleh akan digunakan untuk membentuk matriks $U$.

---

## Langkah 2: Bentuk Matriks $U$

Normalisasi seluruh eigenvector dari $AA^T$.

Susun eigenvector tersebut sebagai kolom-kolom matriks:

$$
U=
\begin{bmatrix}
u_1 & u_2 & \cdots & u_m
\end{bmatrix}
$$

---

## Langkah 3: Hitung $A^TA$

$$
A^TA
$$

Cari:

- Eigenvalue
- Eigenvector

Nilai singular diperoleh dari:

$$
\sigma_i=\sqrt{\lambda_i}
$$

---

## Langkah 4: Bentuk Matriks $V$

Normalisasi eigenvector dari $A^TA$.

Susun sebagai kolom-kolom matriks:

$$
V=
\begin{bmatrix}
v_1 & v_2 & \cdots & v_n
\end{bmatrix}
$$

---

## Langkah 5: Bentuk Matriks $\Sigma$

Isi diagonal utama dengan nilai singular.

$$
\Sigma=
\begin{bmatrix}
\sigma_1 & 0 & \cdots & 0\\
0 & \sigma_2 & \cdots & 0\\
\vdots & \vdots & \ddots & \vdots\\
0 & 0 & \cdots & \sigma_r
\end{bmatrix}
$$

Semua elemen selain diagonal bernilai nol.

---

## Langkah 6: Susun Hasil Akhir

Gabungkan seluruh matriks:

$$
A = U \Sigma V^T
$$

Inilah hasil dekomposisi SVD.

---

# Contoh

Diberikan matriks:

$$
A=
\begin{bmatrix}
3 & 1 & 1\\
-1 & 3 & 1
\end{bmatrix}
$$

---

## Hitung $AA^T$

$$
AA^T=
\begin{bmatrix}
11 & 1\\
1 & 11
\end{bmatrix}
$$

---

## Eigenvalue

Diperoleh:

$$
\lambda_1=12
$$

$$
\lambda_2=10
$$

---

## Nilai Singular

$$
\sigma_1=\sqrt{12}=2\sqrt{3}
$$

$$
\sigma_2=\sqrt{10}
$$

---

## Matriks U

Eigenvector yang telah dinormalisasi:

$$
u_1=
\frac1{\sqrt2}
\begin{bmatrix}
1\\
1
\end{bmatrix}
$$

$$
u_2=
\frac1{\sqrt2}
\begin{bmatrix}
1\\
-1
\end{bmatrix}
$$

Sehingga:

$$
U=
\begin{bmatrix}
\frac1{\sqrt2} & \frac1{\sqrt2}\\
\frac1{\sqrt2} & -\frac1{\sqrt2}
\end{bmatrix}
$$

---

## Matriks $\Sigma$

$$
\Sigma=
\begin{bmatrix}
\sqrt{12} & 0 & 0\\
0 & \sqrt{10} & 0
\end{bmatrix}
$$

---

## Matriks V

Diperoleh dari eigenvector matriks:

$$
A^TA
$$

yang telah dinormalisasi.

---

## Hasil Akhir

$$
A = U \Sigma V^T
$$

---

# Ringkasan Cepat

1. Hitung:

$$
AA^T
$$

2. Cari eigenvalue dan eigenvector.

3. Bentuk matriks:

$$
U
$$

4. Hitung:

$$
A^TA
$$

5. Cari eigenvalue dan eigenvector.

6. Bentuk matriks:

$$
V
$$

7. Hitung nilai singular:

$$
\sigma_i=\sqrt{\lambda_i}
$$

8. Bentuk:

$$
\Sigma
$$

9. Susun hasil akhir:

$$
A=U\Sigma V^T
$$

---

# Rumus yang Wajib Hafal

$$
A=U\Sigma V^T
$$

$$
\sigma_i=\sqrt{\lambda_i}
$$

$$
U^TU=I
$$

$$
V^TV=I
$$

$$
\text{rank}(A)=\text{jumlah nilai singular tak nol}
$$

## Implementasi SVD dengan SageMath Cell

<script src="https://sagecell.sagemath.org/static/embedded_sagecell.js"></script>

<script>
sagecell.makeSagecell({
    inputLocation: '.sage'
});
</script>

<div class="sage">
<script type="text/x-sage">
import numpy as np
A = np.array([[3, 1, 1], [-1, 3, 1]])
U, S_vektor, VT = np.linalg.svd(A)
S_matriks = np.zeros((2, 3))
S_matriks[:2, :2] = np.diag(S_vektor)
hasil = U @ S_matriks @ VT
print('matriks U')
print(U)
print('\nmatriks S')
print(S_matriks)
print('\nmatriks VT')
print(VT)
print('\nMatriks Awal:')
print(A)
print('\nHasil Rekonstruksi (U @ S @ VT):')
print(hasil)
</script>
</div>