## Eliminasi Gauss (Gaussian Elimination)

### Tugas

Contoh SPL 3 Variabel
## Sistem Persamaan Linear 3 Variabel

Diketahui:

$$
\begin{cases}
x_1 - x_2 + x_3 = 3 \\
2x_1 + x_2 + 8x_3 = 18 \\
4x_1 + 2x_2 - 3x_3 = -2
\end{cases}
$$

Bentuk matriks augmented:

$$
\left[
\begin{array}{rrr|r}
1 & -1 & 1 & 3 \\
2 & 1 & 8 & 18 \\
4 & 2 & -3 & -2
\end{array}
\right]
$$

### Eliminasi Kolom Pertama

$$
R_2 \rightarrow R_2 - 2R_1
$$

$$
R_3 \rightarrow R_3 - 4R_1
$$

Hasil:

$$
\left[
\begin{array}{rrr|r}
1 & -1 & 1 & 3 \\
0 & 3 & 6 & 12 \\
0 & 6 & -7 & -14
\end{array}
\right]
$$

### Eliminasi Kolom Kedua

$$
R_3 \rightarrow R_3 - 2R_2
$$

$$
\left[
\begin{array}{rrr|r}
1 & -1 & 1 & 3 \\
0 & 3 & 6 & 12 \\
0 & 0 & -19 & -38
\end{array}
\right]
$$

### Membuat Pivot = 1

$$
R_3 \rightarrow -\frac{1}{19}R_3
$$

$$
\left[
\begin{array}{rrr|r}
1 & -1 & 1 & 3 \\
0 & 3 & 6 & 12 \\
0 & 0 & 1 & 2
\end{array}
\right]
$$

### Substitusi Balik

$$
x_3 = 2
$$

$$
x_2 = 0
$$

$$
x_1 = 1
$$

$$
(x_1, x_2, x_3) = (1,0,2)
$$

## Sistem Persamaan Linear 4 Variabel

Diketahui:

$$
\begin{cases}
x_1 + x_2 + x_3 + x_4 = 10 \\
2x_1 + 3x_2 + x_3 + x_4 = 16 \\
x_1 - x_2 + 2x_3 + x_4 = 8 \\
3x_1 + x_2 + x_3 + 2x_4 = 17
\end{cases}
$$

Bentuk matriks augmented:

$$
\left[
\begin{array}{rrrr|r}
1 & 1 & 1 & 1 & 10 \\
2 & 3 & 1 & 1 & 16 \\
1 & -1 & 2 & 1 & 8 \\
3 & 1 & 1 & 2 & 17
\end{array}
\right]
$$

### Eliminasi Kolom Pertama

$$
R_2 \rightarrow R_2 - 2R_1
$$

$$
R_3 \rightarrow R_3 - R_1
$$

$$
R_4 \rightarrow R_4 - 3R_1
$$

Hasil:

$$
\left[
\begin{array}{rrrr|r}
1 & 1 & 1 & 1 & 10 \\
0 & 1 & -1 & -1 & -4 \\
0 & -2 & 1 & 0 & -2 \\
0 & -2 & -2 & -1 & -13
\end{array}
\right]
$$

### Eliminasi Kolom Kedua

$$
R_3 \rightarrow R_3 + 2R_2
$$

$$
R_4 \rightarrow R_4 + 2R_2
$$

$$
\left[
\begin{array}{rrrr|r}
1 & 1 & 1 & 1 & 10 \\
0 & 1 & -1 & -1 & -4 \\
0 & 0 & -1 & -2 & -10 \\
0 & 0 & -4 & -3 & -21
\end{array}
\right]
$$

### Eliminasi Kolom Ketiga

$$
R_4 \rightarrow R_4 - 4R_3
$$

$$
\left[
\begin{array}{rrrr|r}
1 & 1 & 1 & 1 & 10 \\
0 & 1 & -1 & -1 & -4 \\
0 & 0 & -1 & -2 & -10 \\
0 & 0 & 0 & 5 & 19
\end{array}
\right]
$$

### Membuat Pivot = 1

$$
R_4 \rightarrow \frac{1}{5}R_4
$$

$$
\left[
\begin{array}{rrrr|r}
1 & 1 & 1 & 1 & 10 \\
0 & 1 & -1 & -1 & -4 \\
0 & 0 & -1 & -2 & -10 \\
0 & 0 & 0 & 1 & \frac{19}{5}
\end{array}
\right]
$$

### Substitusi Balik

$$
x_4 = \frac{19}{5}
$$

$$
x_3 = \frac{12}{5}
$$

$$
x_2 = \frac{11}{5}
$$

$$
x_1 = \frac{8}{5}
$$

$$
(x_1,x_2,x_3,x_4)=
\left(
\frac{8}{5},
\frac{11}{5},
\frac{12}{5},
\frac{19}{5}
\right)
$$

```{bibliography}
```

## Learn more

This is just a simple starter to get you started.
You can learn a lot more at [jupyterbook.org](https://jupyterbook.org).
