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

<img src="images/01_Download_Git.png" width="700">

Setelah installer berhasil diunduh, jalankan file installer tersebut dengan melakukan **double click**.

---

### 3. Proses Instalasi
Pada halaman awal installer, klik:
**Next**
Kemudian tentukan lokasi instalasi Git. Jika tidak ada kebutuhan khusus, lokasi default dapat digunakan.
Selanjutnya akan muncul pilihan komponen. Pada tahap ini dapat menggunakan pilihan default.

<img src="images/02_Components_Git.png" width="700">

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

<img src="images/03_TextEditor_Git.png" width="700">
**Penjelasan:**
Untuk mahasiswa Informatika, Visual Studio Code dapat dipilih karena lebih mudah digunakan untuk mengedit source code maupun file dokumentasi.

---

### 5. Menentukan Nama Branch Utama
Pada proses instalasi Git terdapat pilihan nama branch awal.
Branch utama dapat menggunakan:
```text
main
```
<img src="images/04_Branch_Git.png" width="700">

**Penjelasan:**
Branch merupakan jalur pengembangan dalam Git. Penggunaan nama `main` sesuai dengan penggunaan branch utama pada banyak repository GitHub modern dan digunakan dalam praktikum ini.

---

### 6. Menentukan PATH Git
Pada pilihan penggunaan Git dari command line, gunakan pilihan yang memungkinkan Git digunakan melalui command prompt maupun Git Bash.

<img src="images/05_PATH_Git.png" width="700">

**Penjelasan:**
Dengan pengaturan tersebut, perintah Git dapat dijalankan melalui beberapa terminal pada Windows seperti Command Prompt, PowerShell, maupun Git Bash.

---

### 7. Mengatur HTTPS
Untuk koneksi repository GitHub, Git dapat menggunakan HTTPS.

<img src="images/06_HTTPS_Git.png" width="700">

Pada installer Git for Windows, gunakan pilihan library HTTPS yang direkomendasikan oleh installer.

---

### 8. Konversi Line Ending
Pada tahap berikutnya dilakukan pengaturan konversi akhir baris atau **line ending**.

<img src="images/07_EndingConversions_Git.png" width="700">


**Penjelasan:**
Line ending merupakan karakter yang digunakan untuk menandai akhir sebuah baris pada file teks. Pengaturan ini membantu menjaga kompatibilitas file ketika digunakan pada sistem operasi yang berbeda.

---

### 9. Pemilihan Terminal
Pilih **MinTTY** sebagai terminal yang digunakan untuk mengakses Git Bash.

<img src="images/08_TerminalMinTTY_Git.png" width="700">

**Penjelasan:**
Git Bash menyediakan lingkungan terminal yang dapat digunakan untuk menjalankan perintah Git pada Windows.

---

### 10. Pengaturan Git Pull
Tetapkan perilaku standar dari `git pull`.
Pada praktikum ini digunakan pilihan default:

**Fast-forward or merge**

<img src="images/09_GitPullMarge_Git.png" width="700">

**Penjelasan:**
Pengaturan ini menentukan bagaimana Git menangani perubahan dari repository remote ketika perintah `git pull` dijalankan. Pembahasan lebih lanjut mengenai proses merge akan dipelajari pada materi berikutnya.

---

### 11. Memilih Credential Helper
Pada tahap ini dilakukan pemilihan credential helper.

<img src="images/10_CredentialHelper_Git.png" width="700">

**Penjelasan:**
Credential helper digunakan untuk membantu proses autentikasi ketika Git berkomunikasi dengan repository remote.

---

### 12. Pengaturan Extra Options
Pada opsi tambahan, aktifkan **file system caching**.

<img src="images/11_ExtraOptions_Git.png" width="700">

**Penjelasan:**
File system caching dapat membantu meningkatkan performa Git ketika mengakses sistem file.

---

### 13. Penyelesaian Instalasi
Setelah seluruh konfigurasi selesai, klik:
**Install**

<img src="images/12_InstallGit_Git.png" width="700">
Tunggu hingga proses instalasi selesai.
Setelah proses selesai, klik:

**Finish**

<img src="images/13_FinishInstall_Git.png" width="700">

**Penjelasan:**
Tahap ini menandakan bahwa seluruh komponen Git telah selesai dipasang pada komputer.

---

### 14. Mengecek Instalasi Git
Setelah instalasi selesai, buka **Command Prompt**, PowerShell, atau Git Bash.
Kemudian lakukan pengecekan instalasi Git.

<img src="images/14_CekInstallasi_Git.png" width="700">

**Penjelasan:**
Pengecekan dilakukan untuk memastikan bahwa sistem operasi sudah dapat mengenali perintah Git.

---

### 15. Mengecek Versi Git
Untuk melihat versi Git yang terpasang, jalankan perintah:

```bash
git --version
```

<img src="images/15_CekVersion_Git.png" width="700">

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

<img src="images/16_Username_Configurasi.png" width="700">

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

<img src="images/17_UserEmail_Configurasi.png" width="700">

**Penjelasan:**
Email digunakan sebagai salah satu identitas pengguna Git dan akan dicatat pada setiap commit.
Email yang digunakan sebaiknya merupakan email yang terhubung dengan akun GitHub agar identitas commit dapat dikaitkan dengan akun GitHub.

---

## 3. Mengatur Branch Default
Branch default dapat diatur menjadi `main` menggunakan perintah:

```bash
git config --global init.defaultBranch main
```

<img src="images/18_Branch_Configurasi.png" width="700">

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

<img src="images/19_CekConfig_Configurasi.png" width="700">

**Penjelasan:**
Perintah `git config --list` digunakan untuk menampilkan konfigurasi Git yang tersimpan pada komputer.
Dari hasil tersebut dapat diperiksa apakah:
* Username sudah benar.
* Email sudah benar.
* Branch default sudah menggunakan `main`.
* Konfigurasi Git lainnya sudah tersimpan.

---

---

# PRAKTIK 3 — MEMBUAT REPOSITORY GITHUB

Setelah memahami dasar Git dan melakukan konfigurasi Git, langkah berikutnya adalah membuat repository pada GitHub.

Repository GitHub akan digunakan sebagai **repository remote** untuk menyimpan project dan melakukan sinkronisasi dengan repository lokal.

## 1. Login ke GitHub

Buka website GitHub melalui browser, kemudian login menggunakan akun GitHub yang telah dimiliki.

<img src="images/20_LoginGitHub_Repo.png" width="700">

**Penjelasan:**

Login diperlukan agar pengguna dapat membuat dan mengelola repository pada akun GitHub.

---

## 2. Membuat Repository Baru

Setelah berhasil login, buat repository baru dengan langkah berikut:

1. Klik tanda **+** pada bagian kanan atas halaman GitHub.
2. Pilih **New repository**.
3. Masukkan nama repository.
4. Tambahkan deskripsi repository jika diperlukan.
5. Tentukan visibility repository, yaitu **Public** atau **Private**.
6. Klik **Create repository**.

<img src="images/21_MembuatRepoBaru_Repo.png" width="700">

### Contoh Nama dan Deskripsi Repository

Nama repository dapat disesuaikan dengan kebutuhan project.

<img src="images/22_NamaDanDeskripsi_Repo.png" width="700">

**Penjelasan:**

Nama repository digunakan sebagai identitas project pada GitHub. Deskripsi dapat digunakan untuk memberikan informasi singkat mengenai isi atau tujuan repository.

Repository dapat dibuat dengan dua pilihan visibility:

* **Public** — repository dapat dilihat oleh pengguna lain.
* **Private** — repository hanya dapat diakses oleh pengguna yang memiliki izin.

---

## 3. Hasil Pembuatan Repository

Setelah proses pembuatan repository berhasil, GitHub akan menampilkan halaman repository yang telah dibuat.

<img src="images/23_HasilRepo_Repo.png" width="700">

Repository tersebut akan menjadi **repository remote** yang digunakan untuk menyimpan project secara online.

Repository kosong dapat dibuat terlebih dahulu, kemudian repository tersebut dapat di-*clone* ke komputer lokal untuk mulai digunakan.

---

# PRAKTIK 4 — CLONE REPOSITORY

Setelah repository berhasil dibuat pada GitHub, repository tersebut dapat disalin ke komputer lokal menggunakan perintah `git clone`.

## 1. Clone Repository

Gunakan perintah:

```bash
git clone <URL-REPOSITORY>
```

Contoh:
```bash
git clone https://github.com/username/nama-repository.git
```

<img src="images/24_CloneRepo_Repo.png" width="700">

**Penjelasan:**
Perintah `git clone` digunakan untuk membuat salinan repository remote dari GitHub ke komputer lokal.
Dengan melakukan clone, pengguna akan mendapatkan:
* File yang terdapat pada repository.
* Riwayat commit.
* Informasi repository Git.
* Hubungan antara repository lokal dan repository remote.

---

## 2. Masuk ke Folder Repository

Setelah proses clone selesai, masuk ke folder repository menggunakan perintah:

```bash
cd nama-repository
```

Contoh:

```bash
cd praktikum-sistem-terdistribusi
```

<img src="images/25_TreeGit_Repo.png" width="700">

**Penjelasan:**
Perintah `cd` atau **change directory** digunakan untuk berpindah ke folder repository yang telah di-*clone*.
Setelah berada di dalam folder tersebut, perintah Git dapat digunakan untuk mengelola repository lokal.
Struktur repository dapat diperiksa untuk memastikan file dan folder yang diperlukan telah berhasil dibuat.
---

# PRAKTIK 5 — MEMBUAT DAN MENGUBAH FILE

Setelah repository berhasil di-*clone*, tahap berikutnya adalah membuat atau mengubah file yang berada di dalam folder repository.
## 1. Membuat File Baru
Buat sebuah file baru di dalam folder repository.
Contoh file:

```text
README.md
```

atau file lain sesuai dengan kebutuhan praktikum.

<img src="images/26_UpdateFile_Repo.png" width="700">

**Penjelasan:**
File yang dibuat atau diubah di dalam repository lokal akan terdeteksi oleh Git sebagai perubahan (*changes*).
Perubahan tersebut belum langsung tersimpan ke dalam riwayat Git. Untuk melihat perubahan yang terdeteksi oleh Git, gunakan perintah `git status`.

---

## 2. Mengecek Status Repository
Gunakan perintah:

```bash
git status
```

<img src="images/27_GitStatus_Repo.png" width="700">

**Penjelasan:**
Perintah `git status` digunakan untuk mengetahui kondisi repository saat ini.
Git akan memberikan informasi mengenai file yang:
* Baru dibuat.
* Telah diubah.
* Dihapus.
* Belum dimasukkan ke staging area.
* Sudah berada di staging area.
Contoh alur perubahan file:

```text
File dibuat / diubah
        ↓
   git status
        ↓
   git add
        ↓
   git commit
        ↓
   git push
```

Pada tahap Praktik 5, perubahan masih berada pada repository lokal dan belum dikirim ke repository GitHub. Proses `add`, `commit`, dan `push` akan digunakan pada tahap berikutnya.















































<p align="center">

**Praktikum Minggu 01 — Git dan GitHub**

*Sistem Terdistribusi dan Terdesentralisasi*

</p>
