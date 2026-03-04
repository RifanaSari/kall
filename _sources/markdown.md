## Eliminasi Gauss (Gaussian Elimination)

### Gambaran Umum

Bagian ini melanjutkan pembahasan sistem persamaan linear dengan memperkenalkan Eliminasi Gauss, yaitu algoritma sistematis untuk mereduksi sistem linear menjadi bentuk yang lebih sederhana (row echelon form) sehingga mudah diselesaikan dengan substitusi mundur.

### Apa Itu Gaussian Elimination?

Gaussian Elimination adalah algoritma untuk mengubah sistem persamaan linear menjadi bentuk yang lebih sederhana sehingga kita bisa menemukan solusi variabelnya.

$$\begin{equation}
F(x_1,x_2,\dots, x_n)=G(x_1,x_2,\dots, x_n)\tag{1.1.5}
\end{equation}$$

Menulis sistem persamaan sebagai matriks augmented (koefisien + konstanta)

Menggunakan operasi baris elementer untuk mengubah matriks

Mengubahnya ke bentuk eselon baris (row echelon form) atau bahkan bentuk eselon baris tereduksi (RREF)

Here is a "note" directive:

```{note}
Here is a note
```

It will be rendered in a special box when you build your book.

Here is an inline directive to refer to a document: {doc}`markdown-notebooks`.


## Citations

You can also cite references that are stored in a `bibtex` file. For example,
the following syntax: `` {cite}`holdgraf_evidence_2014` `` will render like
this: {cite}`holdgraf_evidence_2014`.

Moreover, you can insert a bibliography into your page with this syntax:
The `{bibliography}` directive must be used for all the `{cite}` roles to
render properly.
For example, if the references for your book are stored in `references.bib`,
then the bibliography is inserted with:

```{bibliography}
```

## Learn more

This is just a simple starter to get you started.
You can learn a lot more at [jupyterbook.org](https://jupyterbook.org).
