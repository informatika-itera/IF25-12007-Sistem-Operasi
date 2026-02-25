# Modul Praktikum Sistem Operasi (IF25-12007)

Template LaTeX modul praktikum dan hands-on mata kuliah **Sistem Operasi (IF25-12007)** — Institut Teknologi Sumatera.

---

## Daftar Modul

| No. | Topik | File |
|-----|-------|------|
| 1  | Pengenalan Antarmuka OS dan Virtual Machine | `chapters/modul_01.tex` |
| 2  | Instalasi Ubuntu pada VirtualBox | `chapters/modul_02.tex` |
| 3  | Navigasi dan Manajemen Izin File Linux | `chapters/modul_03.tex` |
| 4  | Automasi dengan Bash Scripting | `chapters/modul_04.tex` |
| 5  | Sistem Build dengan GCC | `chapters/modul_05.tex` |
| 6  | Otomatisasi Proses Build dengan Makefile | `chapters/modul_06.tex` |
| 7  | Booting dan Framework Sistem Operasi | `chapters/modul_07.tex` |
| 8  | Implementasi Multi-threading | `chapters/modul_08.tex` |
| 9  | Analisis Race Condition | `chapters/modul_09.tex` |
| 10 | Implementasi Mutex dan Locks | `chapters/modul_10.tex` |
| 11 | Penjadwalan Proses Round-Robin | `chapters/modul_11.tex` |
| 12 | Penjadwalan Proses Berbasis Prioritas | `chapters/modul_12.tex` |

---

## Struktur Proyek

```
Modul Praktikum/
├── main.tex              ← Entry point (compile file ini)
├── config.sty            ← Package & metadata bersama
├── Referensi.bib         ← Bibliografi bersama
├── chapters/
│   ├── modul_01.tex      ← Satu file per modul
│   ├── modul_02.tex
│   ├── ...
│   └── modul_12.tex
└── Figure/
    ├── ifitera-header.png  ← Header bersama
    ├── 01/                 ← Gambar modul 1
    ├── 02/                 ← Gambar modul 2
    ├── ...
    └── 12/                 ← Gambar modul 12
```

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

Buka `Modul Praktikum/config.sty` dan ubah bagian **Identitas Mata Kuliah**:

```latex
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

### 2. Isi Konten Tiap Modul

Buka file `chapters/modul_XX.tex` yang ingin dikerjakan dan ganti semua `TODO` serta `\lipsum[...]`.

Setiap file modul berisi satu `\chapter` dengan section:
- Tujuan dan Output Praktikum
- Dasar Teori
- Alat dan Bahan
- Langkah-Langkah Praktikum

Gunakan **Find in Files** untuk menemukan semua bagian yang perlu diisi:

```
VS Code: Ctrl+Shift+F  →  ketik: TODO
```

### 3. Tambahkan Gambar

Letakkan gambar di `Figure/XX/` (sesuai nomor modul) lalu sisipkan di chapter:

```latex
\begin{figure}[h]
    \centering
    \includegraphics[width=0.8\textwidth]{Figure/01/nama_gambar.png}
    \caption{Keterangan gambar}
    \label{fig:m01-label-unik}
\end{figure}
```

### 4. Tambahkan Referensi

Edit `Referensi.bib` dan tambahkan entri BibTeX, lalu sitasi di teks:

```latex
Menurut \cite{Silberschatz2018}, sistem operasi adalah...
```

### 5. Compile PDF

Semua modul dikompilasi menjadi **satu dokumen PDF**.

**Terminal (lokal):**

```bash
cd "Modul Praktikum"
pdflatex main.tex && bibtex main && pdflatex main.tex && pdflatex main.tex
```

Atau dengan `latexmk`:

```bash
latexmk -pdf main.tex
```

**Overleaf:**
1. Upload seluruh isi folder `Modul Praktikum/` ke proyek baru (pertahankan struktur folder).
2. Set **Main document** ke `main.tex` → klik **Compile**.

**VS Code:**
Install ekstensi [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop), buka `main.tex`, tekan `Ctrl+Alt+B`.

---

## Konvensi Penamaan Label

Label diberi prefix `mXX-` untuk menghindari konflik antar modul.

| Tipe | Prefix | Contoh |
|------|--------|--------|
| Chapter | `chap:` | `\label{chap:modul-01}` |
| Section | `sec:` | `\label{sec:m01-persiapan}` |
| Figure | `fig:` | `\label{fig:m01-sesi1}` |
| Table | `tab:` | `\label{tab:m01-dasar-teori}` |
| Code listing | `kode:` | `\label{kode:m01-bash-loop}` |

---

## Lisensi

Template ini dibuat untuk dipergunakan oleh Sivitas Akademik ITERA, khususnya Program Studi Teknik Informatika ITERA.
