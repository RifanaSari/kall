# Transformasi Linear Geometris

## Matriks dari Transformasi Linear

### Teorema

Misalkan

$$
T:\mathbb{R}^n \rightarrow \mathbb{R}^m
$$

adalah transformasi linear.

Maka terdapat matriks unik

$$
A
$$

sedemikian sehingga

$$
T(x)=Ax
$$

untuk setiap

$$
x \in \mathbb{R}^n
$$

Matriks $A$ disebut **matriks standar (standard matrix)** dari transformasi linear $T$.

---

## Membentuk Matriks Standar

Misalkan

$$
e_1,e_2,\ldots,e_n
$$

adalah basis standar pada $\mathbb{R}^n$.

Maka matriks standar $A$ dapat dibentuk dari:

$$
A=
\begin{bmatrix}
T(e_1) & T(e_2) & \cdots & T(e_n)
\end{bmatrix}
$$

Artinya:

- Kolom pertama adalah $T(e_1)$
- Kolom kedua adalah $T(e_2)$
- dan seterusnya

---

## Bukti Singkat

Misalkan

$$
x=
\begin{bmatrix}
x_1\\
x_2\\
\vdots\\
x_n
\end{bmatrix}
$$

maka

$$
x=x_1e_1+x_2e_2+\cdots+x_ne_n
$$

Karena $T$ linear:

$$
T(x)
=
x_1T(e_1)+x_2T(e_2)+\cdots+x_nT(e_n)
$$

yang dapat ditulis sebagai:

$$
T(x)=Ax
$$

---

# Contoh: Dilatasi

Diberikan transformasi

$$
T(x)=3x
$$

untuk

$$
x\in\mathbb{R}^2
$$

Basis standar:

$$
e_1=
\begin{bmatrix}
1\\
0
\end{bmatrix}
,
\quad
e_2=
\begin{bmatrix}
0\\
1
\end{bmatrix}
$$

Hitung:

$$
T(e_1)
=
\begin{bmatrix}
3\\
0
\end{bmatrix}
$$

$$
T(e_2)
=
\begin{bmatrix}
0\\
3
\end{bmatrix}
$$

Sehingga matriks standar:

$$
A=
\begin{bmatrix}
3 & 0\\
0 & 3
\end{bmatrix}
$$

---

# Transformasi Geometris pada Bidang

## 1. Dilatasi

Memperbesar atau memperkecil objek.

Faktor skala:

$$
k
$$

Matriks transformasi:

$$
A=
\begin{bmatrix}
k & 0\\
0 & k
\end{bmatrix}
$$

Transformasi:

$$
T(x,y)
=
(kx,ky)
$$

---

## 2. Refleksi terhadap Sumbu-X

Transformasi:

$$
T(x,y)
=
(x,-y)
$$

Matriks:

$$
A=
\begin{bmatrix}
1 & 0\\
0 & -1
\end{bmatrix}
$$

---

## 3. Refleksi terhadap Sumbu-Y

Transformasi:

$$
T(x,y)
=
(-x,y)
$$

Matriks:

$$
A=
\begin{bmatrix}
-1 & 0\\
0 & 1
\end{bmatrix}
$$

---

## 4. Refleksi terhadap Garis y = x

Transformasi:

$$
T(x,y)
=
(y,x)
$$

Matriks:

$$
A=
\begin{bmatrix}
0 & 1\\
1 & 0
\end{bmatrix}
$$

---

## 5. Rotasi

Rotasi berlawanan arah jarum jam sebesar sudut $\theta$.

Transformasi:

$$
T(x,y)
=
(x\cos\theta-y\sin\theta,
x\sin\theta+y\cos\theta)
$$

Matriks:

$$
A=
\begin{bmatrix}
\cos\theta & -\sin\theta\\
\sin\theta & \cos\theta
\end{bmatrix}
$$

---

## Rotasi 90°

$$
A=
\begin{bmatrix}
0 & -1\\
1 & 0
\end{bmatrix}
$$

---

## Rotasi 180°

$$
A=
\begin{bmatrix}
-1 & 0\\
0 & -1
\end{bmatrix}
$$

---

## Rotasi 270°

$$
A=
\begin{bmatrix}
0 & 1\\
-1 & 0
\end{bmatrix}
$$

---

# Transformasi Geser (Shear)

## Shear Horizontal

$$
T(x,y)
=
(x+ky,y)
$$

Matriks:

$$
A=
\begin{bmatrix}
1 & k\\
0 & 1
\end{bmatrix}
$$

---

## Shear Vertikal

$$
T(x,y)
=
(x,y+kx)
$$

Matriks:

$$
A=
\begin{bmatrix}
1 & 0\\
k & 1
\end{bmatrix}
$$

---

# Onto (Surjektif)

## Definisi

Transformasi

$$
T:\mathbb{R}^n \rightarrow \mathbb{R}^m
$$

disebut **onto (surjektif)** apabila setiap

$$
b\in\mathbb{R}^m
$$

merupakan bayangan dari paling sedikit satu

$$
x\in\mathbb{R}^n
$$

sehingga

$$
T(x)=b
$$

---

## Syarat Matriks

Transformasi matriks

$$
T(x)=Ax
$$

bersifat onto jika:

$$
\operatorname{rank}(A)=m
$$

Jumlah pivot harus sama dengan jumlah baris.

---

# One-to-One (Injektif)

## Definisi

Transformasi

$$
T:\mathbb{R}^n \rightarrow \mathbb{R}^m
$$

disebut **one-to-one (injektif)** apabila setiap

$$
b\in\mathbb{R}^m
$$

memiliki paling banyak satu prapeta.

Artinya:

$$
T(x_1)=T(x_2)
\Rightarrow
x_1=x_2
$$

---

## Syarat Matriks

Transformasi

$$
T(x)=Ax
$$

bersifat one-to-one jika:

$$
\operatorname{rank}(A)=n
$$

Jumlah pivot harus sama dengan jumlah kolom.

---

# Ringkasan Rumus Penting

$$
T(x)=Ax
$$

$$
A=
\begin{bmatrix}
T(e_1) & T(e_2) & \cdots & T(e_n)
\end{bmatrix}
$$

$$
A_{\text{rotasi}}
=
\begin{bmatrix}
\cos\theta & -\sin\theta\\
\sin\theta & \cos\theta
\end{bmatrix}
$$

$$
A_{\text{dilatasi}}
=
\begin{bmatrix}
k & 0\\
0 & k
\end{bmatrix}
$$

$$
\operatorname{rank}(A)=m
\Rightarrow
\text{onto}
$$

$$
\operatorname{rank}(A)=n
\Rightarrow
\text{one-to-one}
$$