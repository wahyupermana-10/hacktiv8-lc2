[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/v1YrMfK2)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11324243&assignment_repo_type=AssignmentRepo)
# Live Code 2

# Instruction

Live Code ini dikerjakan dalam format ***notebook*** isi *notebook* harus mengikuti *outline* di bawah ini:
1. Perkenalan\
   Bab pengenalan harus diisi dengan identitas
2. **Judul/Penanda Soal**\
    Sediakan *Cell* Markdown sebelum cell import pustaka yang berisi nomor soal dan judul problem yang dikerjakan di tiap soalnya. Tiap soal mengikuti format nomor 2-6.
3. *Import* pustaka yang dibutuhkan\
   *Cell* pertama pada *notebook* **harus berisi dan hanya berisi** semua *library* yang digunakan dalam *project*.
4. *Data Loading*\
   Bagian ini berisi proses *data loading* yang kemudian dilanjutkan dengan *explorasi data* secara sederhana.
5. *Mathematical Calculations*\
   Bagian ini berisi proses pengolahan data dengan perhitungan matematis yang diperlukan.
6. Hasil\
   Pada bab terakhir ini berisi jawaban dari pertanyaan soal.

---

# Problems

## Problem 1
Salah satu ruang lingkup Natural Language Processing (NLP) adalah mengukur kesamaan konteks antar kalimat. Untuk mengetahui dua kalimat memiliki konteks yang sama atau tidak, kita mengukurnya dengan *cosine similarity*. Cosine similarity sejatinya mengukur 'jarak' antar dua vektor yang mana vektor-vektor tersebut berisikan angka-angka, sehingga kita perlu menerjemahkan kalimat menjadi list angka (encoding). Ada banyak metode encoding yang dapat digunakan untuk menerjemahkan kalimat ke angka, salah satunya adalah dengan menghitung frekuensi kemunculan kata pada setiap kalimat.

Kalimat 1: Julie loves me more than Linda loves me

Kalimat 2: Jane likes me more than Julie loves me

Berikut tabel yang berisikan frekuensi kata yang muncul pada kedua kalimat:

|Kata|Kalimat 1|Kalimat 2|
|--- |--- |--- |
| me  | 2  | 2 |
| Jane | 0 | 1 |
|Julie |  1 | 1 |
|Linda |  1 | 0 |
|likes |  0 | 1 |
|loves |  2 | 1 |
|more |  1 | 1 |
|than |  1 | 1 |

Buatlah vektor yang merupakan representasi masing-masing kalimat berdasarkan tabel di atas dan hitung cosine similarity antar kedua vektor. Kemudian *jawab pertanyaan berikut* di **markdown**:

a. Apakah kedua kalimat memiliki konteks yang serupa? jika iya, mengapa dan jika tidak, mengapa (jawab berdasarkan hasil perhitungan cosine similaritynya)?

b. Jika meninjau dua buah vektor dan dihitung cosine similaritynya (cos theta), jelaskan secara singkat, jelas, padat apa makna cosine similarity yang bernilai 0 dan 1 (tinjau dari posisi dua vektor di koordinat kartesian)?

c. Mengapa cosine similarity harus melibatkan vektor bukan matriks?

---
## Problem 2

### Dataset Description

* Pada graded challenge ini, data diakses menggunakan `bigquery-public-data` pada Google Cloud Big Query.
* Buka [Google Cloud Platform](https://console.cloud.google.com/), masuk ke BigQuery, lalu buka tab `bigquery-public-data` atau klik link [berikut](https://console.cloud.google.com/bigquery?p=bigquery-public-data&d=samples&page=dataset&_ga=2.245085957.1471931019.1642739417-486643658.1638156099) atau link [berikut](https://console.cloud.google.com/bigquery?p=bigquery-public-data&d=iowa_liquor_sales&t=sales&page=table) untuk langsung menuju ke tabel.

```{attention}
Perhatikan petunjuk penggunaan dataset!
```

1. Gunakan tabel `sales` pada dataset `iowa_liquor_sales.
2. Buatlah query dengan kriteria sebagai berikut:
   - Pilih **HANYA** kolom `sale_dollars`

   - Batasi jumlah data maksimal 5000
3. Simpan dataset dalam bentuk csv, dengan nama `h8dsft_P0LC3_<nama-students>.csv`.
4. Salin query yang telah dibuat di Google Cloud Platform, tulislah pada bagian atas notebook!
5. Tampilkan `head` dan `tail` dari dataset pada notebook!

**Clue**
Untuk mengetahui adanya anomali, kamu bisa menggunakan metode extreme value analysis. Untuk melakukan pengecekan anomali/outlier, lakukan langkah-langkah di bawah ini:
1. Lakukan perhitungan central tendency (mean, median, modus) terhadap data sebelum dideteksi adanya anomali.
2. Cek skewness data untuk mengetahui apakah data terdistribusi normal atau tidak.
3. Lakukan pengolahan data dengan menggunakan extreme value analysis.
4. Buat variabel baru yang menyimpan data yang sudah dibuang data anomalinya.

**PERTANYAAN**

**Silahkan jawab pertanyaan-pertanyaan di bawah ini berdasarkan hasil yang kamu peroleh dan tulis pada bagian hasil:**
1. Berapa rata-rata, median, dan modus dari data tersebut sebelum dihilangkan outliernya? Bagaimana kecerendungan pemusatan datanya? jelaskan jawabanmu!
2. Sebelum melakukan extreme value analysis, kamu harus melakukan pengecekan skewness dari distribusi datanya. Apakah datanya skew atau normal? jelaskan jawabanmu!
3. Ada dua teknik untuk melakukan extreme value analysis, teknik yang mana yang kamu pakai? berikan alasanmu berdasarkan data!

---

## Assignment Rubrics

<img src="https://github.com/fahmimnalfrzki/Dataset/raw/main/Screenshot%202022-12-12%20at%2007.38.12.png"></img>

---

```{admonition} Total Points
**32**
```

---
