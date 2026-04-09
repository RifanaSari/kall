# Matrix

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
