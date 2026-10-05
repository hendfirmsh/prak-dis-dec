# Praktikum Minggu 01

**Mata Kuliah:** Sistem Terdistribusi dan Terdesentralisasi
**Topik:** Git dan GitHub

---

# A. TUJUAN

Praktikum minggu pertama bertujuan untuk:

1. Memahami pengertian dasar Git dan GitHub.
2. Melakukan instalasi Git pada komputer.
3. Melakukan konfigurasi identitas pengguna pada Git.
4. Membuat repository pada GitHub.
5. Menghubungkan repository GitHub dengan repository lokal.
6. Memahami proses `clone`, `add`, `commit`, `push`, dan `pull`.
7. Memahami penggunaan branch untuk mengembangkan suatu perubahan secara lebih aman.
8. Memahami cara membuat dan mengelola repository pribadi.
9. Memahami pengelolaan repository yang berada dalam organisasi.
10. Memahami konsep fork dan Pull Request.
11. Memahami proses kolaborasi menggunakan Git dan GitHub.
12. Mengetahui cara melakukan sinkronisasi perubahan antara repository lokal dan repository GitHub.

---

# B. DASAR TEORI

## 1. Pengertian Git

Git merupakan sistem pengendalian versi atau **Version Control System (VCS)** yang digunakan untuk mencatat perubahan pada file dari waktu ke waktu. Git dapat digunakan untuk mengelola source code, dokumentasi, maupun berbagai jenis dokumen digital.

Git bekerja secara terdistribusi sehingga repository dapat disimpan pada komputer lokal dan dapat dihubungkan dengan repository remote seperti GitHub. Dengan sistem tersebut, perubahan yang dilakukan oleh pengguna dapat dicatat dalam bentuk **commit** sehingga riwayat perubahan dapat diketahui.

Git merupakan perangkat lunak **open source** dan dapat digunakan melalui command line maupun berbagai aplikasi dengan antarmuka grafis.

## 2. Pengertian GitHub

GitHub merupakan platform berbasis web yang digunakan untuk menyimpan repository Git secara online. GitHub tidak hanya digunakan sebagai tempat menyimpan source code, tetapi juga menyediakan fasilitas untuk bekerja sama seperti branch, issue, Pull Request, review, dan pengelolaan collaborator.

Repository GitHub dapat dibuat dengan status **public** maupun **private**. Repository public dapat dilihat oleh pengguna lain, sedangkan repository private hanya dapat diakses oleh pengguna yang memiliki izin.

---

# C. PEMBAHASAN

## PRAKTIK 1 — INSTALASI GIT

### 1. Persiapan

Materi praktikum menyediakan beberapa pilihan instalasi Git. Untuk sistem operasi Windows, instalasi dilakukan menggunakan **Git for Windows**.

Setelah proses instalasi selesai, keberhasilan instalasi dapat diperiksa menggunakan perintah:

```bash
git --version
```

Perintah tersebut akan menampilkan versi Git yang terpasang pada komputer.

---

### 2. Download Git

Git dapat diunduh melalui website resmi Git.

![Download Git](images/01_Download_Git.png)

Setelah installer berhasil diunduh, jalankan file installer tersebut dengan melakukan **double click**.

---

### 3. Proses Instalasi

Pada halaman awal installer, klik:

**Next**

Kemudian tentukan lokasi instalasi Git. Jika tidak ada kebutuhan khusus, lokasi default dapat digunakan.

Selanjutnya akan muncul pilihan komponen. Pada tahap ini dapat menggunakan pilihan default.

![Components Git](images/02_Components_Git.png)

**Penjelasan:**

Pada bagian ini pengguna dapat menentukan komponen tambahan yang akan dipasang bersama Git. Untuk kebutuhan praktikum, pengaturan bawaan installer dapat digunakan.

---

### 4. Memilih Text Editor

Git membutuhkan text editor yang dapat digunakan ketika Git memerlukan editor untuk membuat pesan commit atau melakukan konfigurasi tertentu.

Beberapa editor yang dapat digunakan antara lain:

* Visual Studio Code
* Notepad++
* Vim
* Editor lainnya

![Text Editor Git](images/03_TextEditor_Git.png)

**Penjelasan:**

Untuk mahasiswa Informatika, Visual Studio Code dapat dipilih karena lebih mudah digunakan untuk mengedit source code maupun file dokumentasi.

---

### 5. Menentukan Nama Branch Utama

Pada proses instalasi Git terdapat pilihan nama branch awal.

Branch utama dapat menggunakan:

```text
main
```

![Branch Git](images/04_Branch_Git.png)

**Penjelasan:**

Branch merupakan jalur pengembangan dalam Git. Penggunaan nama `main` sesuai dengan penggunaan branch utama pada banyak repository GitHub modern dan digunakan dalam praktikum ini.

---

### 6. Menentukan PATH Git

Pada pilihan penggunaan Git dari command line, gunakan pilihan yang memungkinkan Git digunakan melalui command prompt maupun Git Bash.

![PATH Git](images/05_PATH_Git.png)

**Penjelasan:**

Dengan pengaturan tersebut, perintah Git dapat dijalankan melalui beberapa terminal pada Windows seperti Command Prompt, PowerShell, maupun Git Bash.

---

### 7. Mengatur HTTPS

Untuk koneksi repository GitHub, Git dapat menggunakan HTTPS.

![HTTPS Git](images/06_HTTPS_Git.png)

Pada installer Git for Windows, gunakan pilihan library HTTPS yang direkomendasikan oleh installer.

---

### 8. Konversi Line Ending

Pada tahap berikutnya dilakukan pengaturan konversi akhir baris atau **line ending**.

![Line Ending](images/07_EndingConversions_Git.png)

**Penjelasan:**

Line ending merupakan karakter yang digunakan untuk menandai akhir sebuah baris pada file teks. Pengaturan ini membantu menjaga kompatibilitas file ketika digunakan pada sistem operasi yang berbeda.

---

### 9. Pemilihan Terminal

Pilih **MinTTY** sebagai terminal yang digunakan untuk mengakses Git Bash.

![Terminal MinTTY](images/08_TerminalMinTTY_Git.png)

**Penjelasan:**

Git Bash menyediakan lingkungan terminal yang dapat digunakan untuk menjalankan perintah Git pada Windows.

---

### 10. Pengaturan Git Pull

Tetapkan perilaku standar dari `git pull`.

Pada praktikum ini digunakan pilihan default:

**Fast-forward or merge**

![Git Pull Merge](images/09_GitPullMarge_Git.png)

**Penjelasan:**

Pengaturan ini menentukan bagaimana Git menangani perubahan dari repository remote ketika perintah `git pull` dijalankan. Pembahasan lebih lanjut mengenai proses merge akan dipelajari pada materi berikutnya.

---

### 11. Memilih Credential Helper

Pada tahap ini dilakukan pemilihan credential helper.

![Credential Helper](images/10_CredentialHelper_Git.png)

**Penjelasan:**

Credential helper digunakan untuk membantu proses autentikasi ketika Git berkomunikasi dengan repository remote.

---

### 12. Pengaturan Extra Options

Pada opsi tambahan, aktifkan **file system caching**.

![Extra Options Git](images/11_ExtraOptions_Git.png)

**Penjelasan:**

File system caching dapat membantu meningkatkan performa Git ketika mengakses sistem file.

---

### 13. Penyelesaian Instalasi

Setelah seluruh konfigurasi selesai, klik:

**Install**

![Install Git](images/12_InstallGit_Git.png)

Tunggu hingga proses instalasi selesai.

Setelah proses selesai, klik:

**Finish**

![Finish Install Git](images/13_FinishInstall_Git.png)

**Penjelasan:**

Tahap ini menandakan bahwa seluruh komponen Git telah selesai dipasang pada komputer.

---

### 14. Mengecek Instalasi Git

Setelah instalasi selesai, buka **Command Prompt**, PowerShell, atau Git Bash.

Kemudian lakukan pengecekan instalasi Git.

![Cek Instalasi Git](images/14_CekInstallasi_Git.png)

**Penjelasan:**

Pengecekan dilakukan untuk memastikan bahwa sistem operasi sudah dapat mengenali perintah Git.

---

### 15. Mengecek Versi Git

Untuk melihat versi Git yang terpasang, jalankan perintah:

```bash
git --version
```

![Cek Versi Git](images/15_CekVersion_Git.png)

**Penjelasan:**

Perintah `git --version` digunakan untuk mengetahui versi Git yang sedang terpasang.

Jika terminal menampilkan nomor versi Git, berarti Git telah berhasil diinstal dan dapat digunakan.

Versi Git yang muncul dapat berbeda tergantung versi Git yang terpasang pada komputer.

---

# PRAKTIK 2 — KONFIGURASI GIT

Setelah Git berhasil diinstal, langkah berikutnya adalah melakukan konfigurasi identitas pengguna.

Git perlu mengetahui nama dan email pengguna karena informasi tersebut akan dicatat pada setiap commit.

---

## 1. Membuat Konfigurasi Nama

Konfigurasi username Git dilakukan menggunakan perintah:

```bash
git config --global user.name "Nama Anda"
```

![Konfigurasi Username](images/16_Username_Configurasi.png)

**Penjelasan:**

Perintah `git config` digunakan untuk mengatur konfigurasi Git.

Parameter:

```text
--global
```

berarti konfigurasi tersebut berlaku secara global untuk pengguna komputer.

Sedangkan:

```text
user.name
```

digunakan untuk menentukan nama pengguna yang akan tercatat dalam commit.

Konfigurasi nama biasanya cukup dilakukan satu kali, kecuali pengguna ingin mengubahnya.

---

## 2. Membuat Konfigurasi Email

Konfigurasi email dilakukan menggunakan perintah:

```bash
git config --global user.email "email@example.com"
```

![Konfigurasi User Email](images/17_UserEmail_Configurasi.png)

**Penjelasan:**

Email digunakan sebagai salah satu identitas pengguna Git dan akan dicatat pada setiap commit.

Email yang digunakan sebaiknya merupakan email yang terhubung dengan akun GitHub agar identitas commit dapat dikaitkan dengan akun GitHub.

---

## 3. Mengatur Branch Default

Branch default dapat diatur menjadi `main` menggunakan perintah:

```bash
git config --global init.defaultBranch main
```

![Konfigurasi Branch](images/18_Branch_Configurasi.png)

**Penjelasan:**

Konfigurasi tersebut menentukan bahwa ketika repository baru dibuat menggunakan:

```bash
git init
```

branch awal yang digunakan akan memiliki nama:

```text
main
```

Pengaturan ini membuat nama branch utama konsisten dengan repository GitHub yang digunakan dalam praktikum.

---

## 4. Mengecek Konfigurasi Git

Untuk melihat konfigurasi Git yang telah tersimpan, jalankan:

```bash
git config --list
```

![Cek Konfigurasi Git](images/19_CekConfig_Configurasi.png)

**Penjelasan:**

Perintah `git config --list` digunakan untuk menampilkan konfigurasi Git yang tersimpan pada komputer.

Dari hasil tersebut dapat diperiksa apakah:

* Username sudah benar.
* Email sudah benar.
* Branch default sudah menggunakan `main`.
* Konfigurasi Git lainnya sudah tersimpan.

---

# D. RINGKASAN PERINTAH

| Perintah                                      | Fungsi                                       |
| --------------------------------------------- | -------------------------------------------- |
| `git --version`                               | Mengecek versi Git                           |
| `git config --list`                           | Menampilkan konfigurasi Git                  |
| `git config --global user.name`               | Mengatur username Git                        |
| `git config --global user.email`              | Mengatur email Git                           |
| `git config --global init.defaultBranch main` | Mengatur branch default                      |
| `git init`                                    | Membuat repository Git lokal                 |
| `git clone`                                   | Menyalin repository remote ke komputer lokal |
| `git status`                                  | Melihat status repository                    |
| `git add`                                     | Memasukkan perubahan ke staging area         |
| `git commit`                                  | Menyimpan perubahan ke history Git           |
| `git push`                                    | Mengirim commit ke repository remote         |
| `git pull`                                    | Mengambil perubahan dari repository remote   |
| `git branch`                                  | Melihat dan mengelola branch                 |

---

# E. ALUR DASAR GIT

Secara umum, workflow dasar Git dapat digambarkan sebagai berikut:

```text
┌──────────────────────┐
│ Membuat / Mengubah   │
│       File           │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│     git status       │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│       git add        │
│    Staging Area      │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│      git commit      │
│   Local Repository   │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│       git push       │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│   Remote Repository  │
│       GitHub         │
└──────────────────────┘
```

Alur tersebut menjadi dasar dalam penggunaan Git untuk mengelola perubahan project.

---

# F. HASIL PRAKTIKUM

Berdasarkan praktikum yang telah dilakukan, diperoleh hasil sebagai berikut:

1. Git berhasil diinstal pada komputer.
2. Git dapat dijalankan melalui terminal.
3. Username Git berhasil dikonfigurasi.
4. Email Git berhasil dikonfigurasi.
5. Branch default berhasil dikonfigurasi menggunakan nama `main`.
6. Konfigurasi Git dapat diperiksa menggunakan perintah `git config --list`.
7. Pemahaman mengenai repository lokal dan remote diperoleh.
8. Pemahaman dasar mengenai `clone`, `add`, `commit`, `push`, dan `pull` diperoleh.
9. Dokumentasi hasil praktikum berhasil dibuat menggunakan Markdown.
10. Screenshot hasil praktik berhasil disimpan di dalam repository GitHub.

---

# G. KESIMPULAN

Berdasarkan praktikum minggu pertama, dapat disimpulkan bahwa **Git dan GitHub merupakan tools penting dalam pengelolaan project perangkat lunak**. Git digunakan sebagai sistem pengendalian versi untuk mencatat perubahan pada file, sedangkan GitHub dapat digunakan sebagai repository remote untuk menyimpan project dan mendukung proses kolaborasi.

Pada praktikum ini telah dilakukan instalasi Git pada Windows mulai dari pemilihan komponen, text editor, branch, PATH, HTTPS, line ending, terminal, Git Pull, credential helper, hingga proses penyelesaian instalasi. Setelah instalasi berhasil, dilakukan konfigurasi username, email, dan branch default `main`.

Selain itu, praktikum memberikan pemahaman mengenai perintah dasar Git seperti `git status`, `git add`, `git commit`, `git push`, dan `git pull`. Pemahaman terhadap perintah-perintah tersebut menjadi dasar untuk melakukan pengelolaan repository secara terstruktur serta mendukung proses kolaborasi menggunakan Git dan GitHub.

Dengan memahami konsep dasar Git dan GitHub pada praktikum ini, mahasiswa memiliki dasar yang lebih baik untuk melanjutkan praktikum berikutnya yang berkaitan dengan repository, branch, sinkronisasi, fork, Pull Request, dan kolaborasi dalam pengembangan perangkat lunak.

---

## 📁 Struktur File Modul 01

```text
01/
│
├── README.md
│
└── images/
    ├── 01_Download_Git.png
    ├── 02_Components_Git.png
    ├── 03_TextEditor_Git.png
    ├── 04_Branch_Git.png
    ├── 05_PATH_Git.png
    ├── 06_HTTPS_Git.png
    ├── 07_EndingConversions_Git.png
    ├── 08_TerminalMinTTY_Git.png
    ├── 09_GitPullMarge_Git.png
    ├── 10_CredentialHelper_Git.png
    ├── 11_ExtraOptions_Git.png
    ├── 12_InstallGit_Git.png
    ├── 13_FinishInstall_Git.png
    ├── 14_CekInstallasi_Git.png
    ├── 15_CekVersion_Git.png
    ├── 16_Username_Configurasi.png
    ├── 17_UserEmail_Configurasi.png
    ├── 18_Branch_Configurasi.png
    └── 19_CekConfig_Configurasi.png
```

---

<p align="center">

**Praktikum Minggu 01 — Git dan GitHub**

*Sistem Terdistribusi dan Terdesentralisasi*

</p>
