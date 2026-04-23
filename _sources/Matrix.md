# Matrix

## Tugas 1 tanggal 9 April 2026
## Cari invers dari :
$$
A = \begin{bmatrix}
1 & 1 & 1 & 1 \\
2 & -1 & 1 & -1 \\
1 & 2 & -1 & 1 \\
3 & -1 & 2 & 1
\end{bmatrix}
$$

Kita cari determinan dengan ekspansi kofaktor (ambil baris pertama biar gampang):

$$
\det(A) = \sum_{j=1}^{n} a_{ij} \, (-1)^{i+j} \, M_{ij}
$$

Determian akhir:
det(A) = (1)(-4) + (1)(8) + (1)(12) + (1)(-4)
= -4 + 8 + 12 - 4 = 12

Adjoin :

$$
\text{adj}(A) = \begin{bmatrix}
-4 & -4 & 0 & 4 \\
8 & 4 & 8 & -4 \\
12 & 4 & -8 & -4 \\
-4 & 4 & 0 & 4
\end{bmatrix}
$$

Invers Matrix:

$$
A^{-1} = \frac{1}{12}
\begin{bmatrix}
-4 & -4 & 0 & 4 \\
8 & 4 & 8 & -4 \\
12 & 4 & -8 & -4 \\
-4 & 4 & 0 & 4
\end{bmatrix}
$$

Hasil Akhir Invers (sudah disederhanakan):

$$
A^{-1} =
\begin{bmatrix}
-\frac{1}{3} & -\frac{1}{3} & 0 & \frac{1}{3} \\
\frac{2}{3} & \frac{1}{3} & \frac{2}{3} & -\frac{1}{3} \\
1 & \frac{1}{3} & -\frac{2}{3} & -\frac{1}{3} \\
-\frac{1}{3} & \frac{1}{3} & 0 & \frac{1}{3}
\end{bmatrix}
$$

## Tugas 2 Tanggal 23 April 2026
## 1. Menentukan Determinan Matriks dengan Ekspansi Baris

Diketahui matriks:

$$
\begin{split}
A=
\begin{bmatrix}
-7 & -5 \\
1 & 4
\end{bmatrix}
\end{split}
$$

Gunakan rumus ekspansi baris:

$$
\begin{split}
\det(A)=\sum_{k=1}^{n}(-1)^{i+k}a_{ik}M_{ik}
\end{split}
$$

dengan:

- $a_{ik}$ = elemen pada baris ke-$i$, kolom ke-$k$
- $M_{ik}$ = minor dari elemen $a_{ik}$

Karena matriks berordo $2 \times 2$, maka dilakukan ekspansi pada baris pertama ($i=1$).

---

### Langkah 1: Hitung minor $M_{11}$

Elemen yang digunakan:

$$
\begin{split}
a_{11}=-7
\end{split}
$$

Hapus baris ke-1 dan kolom ke-1, maka diperoleh:

$$
\begin{split}
M_{11}=
\begin{vmatrix}
4
\end{vmatrix}
=4
\end{split}
$$

---

### Langkah 2: Hitung minor $M_{12}$

Elemen yang digunakan:

$$
\begin{split}
a_{12}=-5
\end{split}
$$

Hapus baris ke-1 dan kolom ke-2, maka diperoleh:

$$
\begin{split}
M_{12}=
\begin{vmatrix}
1
\end{vmatrix}
=1
\end{split}
$$

---

### Langkah 3: Substitusi ke rumus ekspansi baris

$$
\begin{split}
\det(A)
=
(-1)^{1+1}a_{11}M_{11}
+
(-1)^{1+2}a_{12}M_{12}
\end{split}
$$

$$
\begin{split}
=
(-1)^2(-7)(4)
+
(-1)^3(-5)(1)
\end{split}
$$

$$
\begin{split}
=
(1)(-28)
+
(-1)(-5)
\end{split}
$$

$$
\begin{split}
=
-28+5
\end{split}
$$

$$
\begin{split}
=
-23
\end{split}
$$

---

## Jawaban Akhir

$$
\begin{split}
\boxed{\det(A)=-23}
\end{split}
$$

## 2. Menentukan Determinan Matriks dengan Ekspansi Baris

Diketahui matriks:

$$
\begin{split}
A=
\begin{bmatrix}
0 & 2 & -3 \\
1 & -2 & -1 \\
0 & 0 & 1
\end{bmatrix}
\end{split}
$$

Gunakan rumus ekspansi baris:

$$
\begin{split}
\det(A)=\sum_{k=1}^{n}(-1)^{i+k}a_{ik}M_{ik}
\end{split}
$$

dengan:

- $a_{ik}$ = elemen pada baris ke-$i$, kolom ke-$k$
- $M_{ik}$ = minor dari elemen $a_{ik}$

Karena pada baris ketiga terdapat banyak nol, maka lebih mudah menggunakan ekspansi pada baris ke-3 ($i=3$).

---

### Langkah 1: Hitung minor $M_{31}$

Elemen:

$$
\begin{split}
a_{31}=0
\end{split}
$$

Karena elemennya 0, maka hasilnya langsung:

$$
\begin{split}
(-1)^{3+1}(0)(M_{31})=0
\end{split}
$$

---

### Langkah 2: Hitung minor $M_{32}$

Elemen:

$$
\begin{split}
a_{32}=0
\end{split}
$$

Karena elemennya 0, maka hasilnya langsung:

$$
\begin{split}
(-1)^{3+2}(0)(M_{32})=0
\end{split}
$$

---

### Langkah 3: Hitung minor $M_{33}$

Elemen:

$$
\begin{split}
a_{33}=1
\end{split}
$$

Hapus baris ke-3 dan kolom ke-3, diperoleh submatriks:

$$
\begin{split}
\begin{bmatrix}
0 & 2 \\
1 & -2
\end{bmatrix}
\end{split}
$$

Sehingga:

$$
\begin{split}
M_{33}
=
\begin{vmatrix}
0 & 2 \\
1 & -2
\end{vmatrix}
\end{split}
$$

Hitung determinannya:

$$
\begin{split}
M_{33}
=
(0)(-2)-(2)(1)
\end{split}
$$

$$
\begin{split}
=
0-2
\end{split}
$$

$$
\begin{split}
=
-2
\end{split}
$$

---

### Langkah 4: Substitusi ke rumus ekspansi baris

$$
\begin{split}
\det(A)
=
(-1)^{3+1}(0)(M_{31})
+
(-1)^{3+2}(0)(M_{32})
+
(-1)^{3+3}(1)(M_{33})
\end{split}
$$

$$
\begin{split}
=
0+0+(-1)^6(1)(-2)
\end{split}
$$

$$
\begin{split}
=
0+0+(1)(-2)
\end{split}
$$

$$
\begin{split}
=
-2
\end{split}
$$

---

## Jawaban Akhir

$$
\begin{split}
\boxed{\det(A)=-2}
\end{split}
$$

## 3. Menentukan Determinan Matriks dengan Ekspansi Baris

Diketahui matriks:

$$
\begin{split}
A=
\begin{bmatrix}
1 & -3 & 1 & 1 \\
-3 & 1 & 1 & 1 \\
1 & 1 & -3 & 1 \\
1 & 1 & 1 & -3
\end{bmatrix}
\end{split}
$$

Gunakan rumus ekspansi baris:

$$
\begin{split}
\det(A)=\sum_{k=1}^{n}(-1)^{i+k}a_{ik}M_{ik}
\end{split}
$$

dengan:

- $a_{ik}$ = elemen pada baris ke-$i$, kolom ke-$k$
- $M_{ik}$ = minor dari elemen $a_{ik}$

Karena semua elemen dapat dihitung, kita lakukan ekspansi pada baris pertama ($i=1$).

---

### Langkah 1: Hitung minor $M_{11}$

Elemen:

$$
\begin{split}
a_{11}=1
\end{split}
$$

Hapus baris ke-1 dan kolom ke-1:

$$
\begin{split}
\begin{bmatrix}
1 & 1 & 1 \\
1 & -3 & 1 \\
1 & 1 & -3
\end{bmatrix}
\end{split}
$$

Sehingga:

$$
\begin{split}
M_{11}=
\begin{vmatrix}
1 & 1 & 1 \\
1 & -3 & 1 \\
1 & 1 & -3
\end{vmatrix}
\end{split}
$$

Hitung determinan:

$$
\begin{split}
M_{11}=16
\end{split}
$$

---

### Langkah 2: Hitung minor $M_{12}$

Elemen:

$$
\begin{split}
a_{12}=-3
\end{split}
$$

Hapus baris ke-1 dan kolom ke-2:

$$
\begin{split}
\begin{bmatrix}
-3 & 1 & 1 \\
1 & -3 & 1 \\
1 & 1 & -3
\end{bmatrix}
\end{split}
$$

Sehingga:

$$
\begin{split}
M_{12}=
\begin{vmatrix}
-3 & 1 & 1 \\
1 & -3 & 1 \\
1 & 1 & -3
\end{vmatrix}
\end{split}
$$

Hitung determinan:

$$
\begin{split}
M_{12}=-16
\end{split}
$$

---

### Langkah 3: Hitung minor $M_{13}$

Elemen:

$$
\begin{split}
a_{13}=1
\end{split}
$$

Karena bentuknya simetris dengan minor sebelumnya:

$$
\begin{split}
M_{13}=16
\end{split}
$$

---

### Langkah 4: Hitung minor $M_{14}$

Elemen:

$$
\begin{split}
a_{14}=1
\end{split}
$$

Karena bentuknya juga simetris:

$$
\begin{split}
M_{14}=16
\end{split}
$$

---

### Langkah 5: Substitusi ke rumus ekspansi baris

$$
\begin{split}
\det(A)
=
(-1)^{1+1}(1)(16)
+
(-1)^{1+2}(-3)(-16)
+
(-1)^{1+3}(1)(16)
+
(-1)^{1+4}(1)(16)
\end{split}
$$

$$
\begin{split}
=
(1)(16)
+
(-1)(48)
+
(1)(16)
+
(-1)(16)
\end{split}
$$

$$
\begin{split}
=
16-48+16-16
\end{split}
$$

$$
\begin{split}
=
-32
\end{split}
$$

---

## Jawaban Akhir

$$
\begin{split}
\boxed{\det(A)=-32}
\end{split}
$$

## 4. Menentukan Invers Matriks dengan Metode Adjoin

Diketahui:

$$
\begin{split}
A=
\begin{bmatrix}
-7 & -5 \\
1 & 4
\end{bmatrix}
\end{split}
$$

Gunakan rumus:

$$
\begin{split}
A^{-1}=\frac{1}{\det A}\,\text{adj}\,A
\end{split}
$$

---

### Langkah 1: Hitung determinan

$$
\begin{split}
\det(A)
=
(-7)(4)-(-5)(1)
\end{split}
$$

$$
\begin{split}
=
-28+5
\end{split}
$$

$$
\begin{split}
=
-23
\end{split}
$$

---

### Langkah 2: Tentukan adjoin matriks

Untuk matriks orde $2 \times 2$:

$$
\begin{split}
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}^{-1}
=
\frac{1}{ad-bc}
\begin{bmatrix}
d & -b \\
-c & a
\end{bmatrix}
\end{split}
$$

Maka:

$$
\begin{split}
\text{adj}\,A=
\begin{bmatrix}
4 & 5 \\
-1 & -7
\end{bmatrix}
\end{split}
$$

---

### Langkah 3: Hitung invers

$$
\begin{split}
A^{-1}
=
\frac{1}{-23}
\begin{bmatrix}
4 & 5 \\
-1 & -7
\end{bmatrix}
\end{split}
$$

$$
\begin{split}
A^{-1}
=
\begin{bmatrix}
-\frac{4}{23} & -\frac{5}{23} \\
\frac{1}{23} & \frac{7}{23}
\end{bmatrix}
\end{split}
$$

---

## Jawaban Akhir

$$
\begin{split}
\boxed{
A^{-1}
=
\begin{bmatrix}
-\frac{4}{23} & -\frac{5}{23} \\
\frac{1}{23} & \frac{7}{23}
\end{bmatrix}}
\end{split}
$$

---

# 5. Menentukan Invers Matriks dengan Metode Adjoin

Diketahui:

$$
\begin{split}
A=
\begin{bmatrix}
0 & 2 & -3 \\
1 & -2 & -1 \\
0 & 0 & 1
\end{bmatrix}
\end{split}
$$

Determinan dari soal sebelumnya:

$$
\begin{split}
\det(A)=-2
\end{split}
$$

Gunakan rumus:

$$
\begin{split}
A^{-1}=\frac{1}{\det A}\,\text{adj}\,A
\end{split}
$$

---

### Hasil perhitungan adjoin

$$
\begin{split}
\text{adj}\,A=
\begin{bmatrix}
-2 & -2 & 8 \\
-1 & 0 & -3 \\
0 & 0 & -2
\end{bmatrix}
\end{split}
$$

---

### Hitung invers

$$
\begin{split}
A^{-1}
=
\frac{1}{-2}
\begin{bmatrix}
-2 & -2 & 8 \\
-1 & 0 & -3 \\
0 & 0 & -2
\end{bmatrix}
\end{split}
$$

$$
\begin{split}
A^{-1}
=
\begin{bmatrix}
1 & 1 & -4 \\
\frac{1}{2} & 0 & \frac{3}{2} \\
0 & 0 & 1
\end{bmatrix}
\end{split}
$$

---

## Jawaban Akhir

$$
\begin{split}
\boxed{
A^{-1}
=
\begin{bmatrix}
1 & 1 & -4 \\
\frac{1}{2} & 0 & \frac{3}{2} \\
0 & 0 & 1
\end{bmatrix}}
\end{split}
$$

---

# 6. Menentukan Invers Matriks dengan Metode Adjoin

Diketahui:

$$
\begin{split}
A=
\begin{bmatrix}
1 & -3 & 1 & 1 \\
-3 & 1 & 1 & 1 \\
1 & 1 & -3 & 1 \\
1 & 1 & 1 & -3
\end{bmatrix}
\end{split}
$$

Determinan dari soal sebelumnya:

$$
\begin{split}
\det(A)=-32
\end{split}
$$

Gunakan rumus:

$$
\begin{split}
A^{-1}=\frac{1}{\det A}\,\text{adj}\,A
\end{split}
$$

---

### Hasil invers

$$
\begin{split}
A^{-1}=
\begin{bmatrix}
-\frac{1}{4} & -\frac{1}{4} & 0 & 0 \\
-\frac{1}{4} & -\frac{1}{4} & 0 & 0 \\
0 & 0 & -\frac{1}{4} & 0 \\
0 & 0 & 0 & -\frac{1}{4}
\end{bmatrix}
\end{split}
$$

---

## Jawaban Akhir

$$
\begin{split}
\boxed{
A^{-1}=
\begin{bmatrix}
-\frac{1}{4} & -\frac{1}{4} & 0 & 0 \\
-\frac{1}{4} & -\frac{1}{4} & 0 & 0 \\
0 & 0 & -\frac{1}{4} & 0 \\
0 & 0 & 0 & -\frac{1}{4}
\end{bmatrix}}
\end{split}
$$