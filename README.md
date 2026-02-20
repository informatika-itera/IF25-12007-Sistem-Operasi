# Modul Praktikum Sistem Operasi (IF25-12007)

Template LaTeX modul praktikum dan hands-on mata kuliah **Sistem Operasi (IF25-12007)** — Institut Teknologi Sumatera.

---

## Daftar Modul

| No. | Topik |
|-----|-------|
| 1  | Pengenalan Antarmuka OS dan Virtual Machine |
| 2  | Instalasi Ubuntu pada VirtualBox |
| 3  | Navigasi dan Manajemen Izin File Linux |
| 4  | Automasi dengan Bash Scripting |
| 5  | Sistem Build dengan GCC |
| 6  | Otomatisasi Proses Build dengan Makefile |
| 7  | Booting dan Framework Sistem Operasi |
| 8  | Implementasi Multi-threading |
| 9  | Analisis Race Condition |
| 10 | Implementasi Mutex dan Locks |
| 11 | Penjadwalan Proses Round-Robin |
| 12 | Penjadwalan Proses Berbasis Prioritas |


---

## Prasyarat

Pastikan salah satu distribusi LaTeX berikut sudah terinstal:

- **TeX Live** (Linux/macOS/Windows) — [tug.org/texlive](https://tug.org/texlive/)
- **MiKTeX** (Windows) — [miktex.org](https://miktex.org/)
- **MacTeX** (macOS) — [tug.org/mactex](https://tug.org/mactex/)

Atau gunakan editor online **Overleaf atau Crixet** tanpa instalasi lokal.

---

## Cara Penggunaan

### 1. Isi Metadata di `config.sty`

Buka `config.sty` pada folder modul yang ingin dikerjakan dan ubah bagian **Identitas Modul Praktikum**:

```latex
\newcommand{\moduleName}{Nama Modul}
\newcommand{\moduleNumber}{1}
\newcommand{\dosenPengampu}{Nama Dosen, S.T., M.T.}
\newcommand{\labAssistantOne}{Nama Asisten Pertama}
\newcommand{\labAssistantTwo}{Nama Asisten Kedua}
\newcommand{\semester}{Genap 2025/2026}
```

Untuk Hands-On, mahasiswa juga mengisi bagian identitas:

```latex
\newcommand{\stuid}{12345678}
\newcommand{\studentName}{Budi Santoso}
\newcommand{\studyProgram}{Teknik Informatika}
\newcommand{\practClass}{RA/RB/RC/RD/RE/RF/RG}
```

### 2. Isi Konten Tiap Chapter

Buka file di dalam `chapters/` dan ganti semua `TODO` serta `\lipsum[...]`.

Gunakan **Find in Files** untuk menemukan semua bagian yang perlu diisi:

```
VS Code: Ctrl+Shift+F  →  ketik: TODO
```

### 3. Tambahkan Gambar

Letakkan gambar di `Figure/` lalu sisipkan ke chapter:

```latex
\begin{figure}[h]
    \centering
    \includegraphics[width=0.8\textwidth]{Figure/nama_gambar.png}
    \caption{Keterangan gambar}
    \label{fig:label-unik}
\end{figure}
```

### 4. Tambahkan Referensi

Edit `Referensi.bib` dan tambahkan entri BibTeX, lalu sitasi di teks:

```latex
Menurut \cite{Silberschatz2018}, sistem operasi adalah...
```

### 5. Compile PDF

**Terminal (lokal):**

```bash
cd "<folder-modul>"
pdflatex main.tex && bibtex main && pdflatex main.tex && pdflatex main.tex
```

Atau dengan `latexmk`:

```bash
latexmk -pdf main.tex
```

**Overleaf:**
1. Upload seluruh isi folder modul ke proyek baru (pertahankan struktur folder).
2. Set **Main document** ke `main.tex` → klik **Compile**.

**VS Code:**
Install ekstensi [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop), buka `main.tex`, tekan `Ctrl+Alt+B`.

---


## Konvensi Penamaan Label

| Tipe | Prefix | Contoh |
|------|--------|--------|
| Section | `sec:` | `\label{sec:persiapan}` |
| Figure | `fig:` | `\label{fig:hasil-compile}` |
| Table | `tab:` | `\label{tab:perintah-linux}` |
| Code listing | `kode:` | `\label{kode:bash-loop}` |

---

## Lisensi

Template ini dibuat untuk dipergunakan oleh Sivitas Akademik ITERA, khususnya Program Studi Teknik Informatika ITERA..
