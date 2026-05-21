# Tugas
Buat matrik tranformasi dari:
<iframe src="https://www.geogebra.org/calculator/jxrvcyu6?embed" width="800" height="600" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

Dari gambar, koordinat titik:
- A = (2, 3)
- B = (2, 1)
- C = (4, 1)

---

Diketahui:
A = (2,3)

---
## Tugas tanggal 30 April 2026

### 1. Transformasi A ke B

Perpindahan:
(2,3) → (2,1)

$$
\begin{bmatrix}
1 & 0 \\
2 & -1
\end{bmatrix}
\begin{bmatrix}
2 \\
3
\end{bmatrix}
=
\begin{bmatrix}
(1 \cdot 2 + 0 \cdot 3) \\
(2 \cdot 2 + (-1) \cdot 3)
\end{bmatrix}
=
\begin{bmatrix}
2 \\
1
\end{bmatrix}
$$

---

### 2. Transformasi B ke C

Perpindahan:
(2,1) → (4,1)

$$
\begin{bmatrix}
2 & 0 \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
2 \\
1
\end{bmatrix}
=
\begin{bmatrix}
(2 \cdot 2 + 0 \cdot 1) \\
(0 \cdot 2 + 1 \cdot 1)
\end{bmatrix}
=
\begin{bmatrix}
4 \\
1
\end{bmatrix}
$$

---

### 3. Transformasi A ke C

Perpindahan:
(2,3) → (4,1)

$$
\begin{bmatrix}
2 & 0 \\
2 & -1
\end{bmatrix}
\begin{bmatrix}
2 \\
3
\end{bmatrix}
=
\begin{bmatrix}
(2 \cdot 2 + 0 \cdot 3) \\
(2 \cdot 2 + (-1) \cdot 3)
\end{bmatrix}
=
\begin{bmatrix}
4 \\
1
\end{bmatrix}
$$

Diketahui:
D = (2,4)

---

### 1. Transformasi D ke E

Perpindahan:
(2,4) → (2,0)

$$
\begin{bmatrix}
1 & 0 \\
2 & -1
\end{bmatrix}
\begin{bmatrix}
2 \\
4
\end{bmatrix}
=
\begin{bmatrix}
(1 \cdot 2 + 0 \cdot 4) \\
(2 \cdot 2 + (-1) \cdot 4)
\end{bmatrix}
=
\begin{bmatrix}
2 \\
0
\end{bmatrix}
$$

---

### 2. Transformasi E ke F

Perpindahan:
(2,0) → (4,0)

$$
\begin{bmatrix}
2 & 0 \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
2 \\
0
\end{bmatrix}
=
\begin{bmatrix}
(2 \cdot 2 + 0 \cdot 0) \\
(0 \cdot 2 + 1 \cdot 0)
\end{bmatrix}
=
\begin{bmatrix}
4 \\
0
\end{bmatrix}
$$

---

### 3. Transformasi D ke F

Perpindahan:
(2,4) → (4,0)

$$
\begin{bmatrix}
2 & 0 \\
2 & -1
\end{bmatrix}
\begin{bmatrix}
2 \\
4
\end{bmatrix}
=
\begin{bmatrix}
(2 \cdot 2 + 0 \cdot 4) \\
(2 \cdot 2 + (-1) \cdot 4)
\end{bmatrix}
=
\begin{bmatrix}
4 \\
0
\end{bmatrix}
$$

## Tugas tanggal 7 Mei 2026
https://colab.research.google.com/drive/1TDfNxR2WUjFVcQH4KGCe1IIm9_gdjT1T?usp=sharing

### Penjelasan Program Transformasi Geometri dengan Python

Program ini digunakan untuk membuat animasi transformasi geometri menggunakan Python.

Transformasi yang digunakan:

1. Translasi (pergeseran)
2. Refleksi / pencerminan terhadap sumbu-x

Library yang digunakan:

- NumPy → operasi matriks
- Matplotlib → membuat grafik dan animasi

---

### 1. Import Library

```python
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation
from IPython.display import HTML
```

Penjelasan:

- `numpy` digunakan untuk operasi matriks dan koordinat.
- `matplotlib.pyplot` digunakan untuk membuat grafik.
- `FuncAnimation` digunakan untuk membuat animasi.
- `HTML` digunakan agar animasi tampil di notebook `.ipynb`.

---

### 2. Membuat Objek Awal

```python
objek = np.array([
    [2, 3],
    [2, 4],
    [3, 4],
    [3, 3],
    [2, 3]
])
```

Objek berbentuk persegi dengan titik:

- A(2,3)
- B(2,4)
- C(3,4)
- D(3,3)

Titik pertama diulang agar garis kembali ke titik awal sehingga bangun tertutup.

---

### 3. Matriks Refleksi

```python
R = np.array([
    [1,  0],
    [0, -1]
])
```

Matriks refleksi terhadap sumbu-x:

$$
\begin{bmatrix}
1 & 0 \\
0 & -1
\end{bmatrix}
$$

Rumus refleksi:

$$
(x,y) \rightarrow (x,-y)
$$

Artinya:

- koordinat x tetap
- koordinat y berubah tanda

Contoh:

$$
(2,3) \rightarrow (2,-3)
$$

---

### 4. Fungsi Translasi

```python
def T(tx, ty):
```

Fungsi ini membuat matriks translasi:

$$
\begin{bmatrix}
1 & 0 & t_x \\
0 & 1 & t_y \\
0 & 0 & 1
\end{bmatrix}
$$

Rumus translasi:

$$
(x,y) \rightarrow (x+t_x,\ y+t_y)
$$

Keterangan:

- `tx` = pergeseran horizontal
- `ty` = pergeseran vertikal

---

### 5. Koordinat Homogen

```python
def ke_homogen(obj):
```

Digunakan untuk mengubah koordinat biasa:

$$
(x,y)
$$

menjadi koordinat homogen:

$$
(x,y,1)
$$

Tujuannya agar translasi dapat dilakukan menggunakan perkalian matriks.

---

### 6. Fungsi update(frame)

```python
def update(frame):
```

Fungsi ini merupakan inti animasi.

Fungsi akan dijalankan terus-menerus untuk setiap frame animasi.

---

### 7. Gerakan Translasi

```python
ty = (frame / (total_frames - 1)) * max_translation
```

Nilai `ty` berubah setiap frame sehingga objek bergerak perlahan.

Karena:

```python
max_translation = -2.0
```

maka objek bergerak turun sejauh 2 satuan.

Transformasi:

$$
(x,y) \rightarrow (x,y-2)
$$

---

### 8. Translasi Objek Asli

```python
asli = (T(0, ty) @ obj_h.T).T
```

Objek asli bergerak turun secara vertikal.

Contoh:

$$
(2,3) \rightarrow (2,1)
$$

---

### 9. Refleksi terhadap Sumbu-x

```python
refleksi_awal = (R @ objek.T).T
```

Objek dicerminkan terhadap sumbu-x.

Contoh:

$$
(2,3) \rightarrow (2,-3)
$$

---

### 10. Gerakan Bayangan Refleksi

```python
refleksi = (T(0, -ty) @ refleksi_h.T).T
```

Bayangan refleksi bergerak berlawanan arah dengan objek asli.

Jika objek asli turun, maka bayangan bergerak naik.

Hal ini membuat animasi tetap simetris terhadap sumbu-x.

---

### 11. Menggambar Objek

```python
ax.plot(...)
```

Digunakan untuk menggambar:

- objek asli (warna biru)
- bayangan refleksi (warna merah)

---

### 12. Label Koordinat

```python
gambar_label(...)
```

Digunakan untuk menampilkan koordinat setiap titik pada grafik.

Contoh:

$$
(2,3)
$$

---

### 13. Membuat Animasi

```python
anim = FuncAnimation(...)
```

Keterangan:

- `frames=15` → jumlah frame animasi
- `interval=300` → jeda antar frame (300 ms)
- `repeat=True` → animasi diulang terus-menerus

---

### 14. Menampilkan Animasi

```python
HTML(anim.to_jshtml())
```

Digunakan agar animasi tampil langsung pada notebook `.ipynb`.

---

### Kesimpulan

Program ini menerapkan konsep transformasi geometri berupa:

#### Refleksi terhadap sumbu-x

$$
(x,y) \rightarrow (x,-y)
$$

#### Translasi

$$
(x,y) \rightarrow (x+t_x,\ y+t_y)
$$

#### Matriks Refleksi

$$
\begin{bmatrix}
1 & 0 \\
0 & -1
\end{bmatrix}
$$

#### Matriks Translasi Homogen

$$
\begin{bmatrix}
1 & 0 & t_x \\
0 & 1 & t_y \\
0 & 0 & 1
\end{bmatrix}
$$

Dengan menggunakan transformasi tersebut, objek dapat bergerak dan dicerminkan secara animasi pada bidang koordinat.

## Tugas tanggal 21 Mei 2026
### Dekomposisi QR Manual (Gram-Schmidt)

#### Matriks A

$$
A=
\begin{bmatrix}
2 & 1 & 3 & 0\\
1 & 4 & 2 & 1\\
3 & 0 & 1 & 2\\
0 & 2 & 1 & 3
\end{bmatrix}
$$

Kolom-kolom:

$$
a_1=(2,1,3,0)
$$

$$
a_2=(1,4,0,2)
$$

$$
a_3=(3,2,1,1)
$$

$$
a_4=(0,1,2,3)
$$

---

#### 1. Cari q₁

Norm:

$$
\sqrt{2^2+1^2+3^2+0^2}
=
\sqrt{14}
$$

$$
q_1=
\left(
\frac2{\sqrt{14}},
\frac1{\sqrt{14}},
\frac3{\sqrt{14}},
0
\right)
$$

---

#### 2. Cari q₂

Dot product:

$$
a_2 \cdot q_1
=
\frac{2(1)+1(4)+3(0)+0(2)}{\sqrt{14}}
=
\frac6{\sqrt{14}}
$$

Proyeksi:

$$
\frac6{\sqrt{14}}q_1
=
\left(
\frac67,
\frac37,
\frac97,
0
\right)
$$

Kurangkan:

$$
u_2
=
(1,4,0,2)
-
\left(
\frac67,
\frac37,
\frac97,
0
\right)
$$

$$
=
\left(
\frac17,
\frac{25}7,
-\frac97,
2
\right)
$$

Norm:

$$
\|u_2\|
=
\frac{\sqrt{903}}7
$$

Maka:

$$
q_2=
\left(
\frac1{\sqrt{903}},
\frac{25}{\sqrt{903}},
-\frac9{\sqrt{903}},
\frac{14}{\sqrt{903}}
\right)
$$

---

#### 3. Cari q₃

Hitung dot pertama:

$$
a_3 \cdot q_1
=
\frac{2(3)+1(2)+3(1)+0(1)}{\sqrt{14}}
=
\frac{11}{\sqrt{14}}
$$

Proyeksi ke q₁:

$$
\frac{11}{\sqrt{14}}q_1
=
\left(
\frac{11}7,
\frac{11}{14},
\frac{33}{14},
0
\right)
$$

---

Dot kedua:

$$
a_3 \cdot q_2
=
\frac{
1(3)+25(2)+(-9)(1)+14(1)
}{\sqrt{903}}
=
\frac{58}{\sqrt{903}}
$$

Proyeksi ke q₂:

$$
\frac{58}{\sqrt{903}}q_2
=
\left(
\frac{58}{903},
\frac{1450}{903},
-\frac{522}{903},
\frac{812}{903}
\right)
$$

---

Kurangkan semuanya:

$$
u_3
=
a_3
-
\text{proj}_{q_1}
-
\text{proj}_{q_2}
$$

$$
=
(3,2,1,1)
-
\left(
\frac{11}7,
\frac{11}{14},
\frac{33}{14},
0
\right)
-
\left(
\frac{58}{903},
\frac{1450}{903},
-\frac{522}{903},
\frac{812}{903}
\right)
$$

Hasil pendekatan:

$$
u_3
\approx
(1.364,-0.391,-0.781,0.101)
$$

Norm:

$$
\|u_3\|
\approx 1.622
$$

Maka:

$$
q_3
\approx
(0.841,-0.241,-0.482,0.062)
$$

---

#### 4. Cari q₄

Hitung:

$$
a_4 \cdot q_1
=
\frac{2(0)+1(1)+3(2)+0(3)}{\sqrt{14}}
=
\frac7{\sqrt{14}}
$$

Proyeksi:

$$
\frac7{\sqrt{14}}q_1
=
(1,\tfrac12,\tfrac32,0)
$$

---

Dot kedua:

$$
a_4 \cdot q_2
=
\frac{
1(0)+25(1)+(-9)(2)+14(3)
}{\sqrt{903}}
=
\frac{49}{\sqrt{903}}
$$

Proyeksi:

$$
\frac{49}{\sqrt{903}}q_2
\approx
(0.054,1.357,-0.488,0.760)
$$

---

Dot ketiga:

$$
a_4 \cdot q_3
\approx 1.221
$$

Proyeksi:

$$
1.221q_3
\approx
(1.027,-0.294,-0.589,0.076)
$$

---

Kurangkan:

$$
u_4
=
a_4
-
\text{proj}_{q_1}
-
\text{proj}_{q_2}
-
\text{proj}_{q_3}
$$

$$
\approx
(-2.081,-0.563,1.577,2.164)
$$

Norm:

$$
\|u_4\|
\approx 3.422
$$

Maka:

$$
q_4
\approx
(-0.608,-0.165,0.461,0.632)
$$

---

#### Hasil Akhir Q

$$
Q
\approx
\begin{bmatrix}
0.535 & 0.033 & 0.841 & -0.608\\
0.267 & 0.832 & -0.241 & -0.165\\
0.802 & -0.300 & -0.482 & 0.461\\
0 & 0.466 & 0.062 & 0.632
\end{bmatrix}
$$