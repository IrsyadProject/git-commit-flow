# GIT COMMIT FLOW

Alur perintah Git pada dasarnya mengikuti beberapa langkah umum yang digunakan untuk mengelola proyek berbasis version control. Git memungkinkan pengembang melacak perubahan, berkolaborasi dengan tim, dan memanipulasi versi dari proyek secara fleksibel.

Berikut adalah alur dasar dan perintah-perintah penting dalam Git:

### 1. **Inisialisasi Repositori**

Sebelum mulai bekerja, Anda harus menginisialisasi repositori Git di direktori proyek.

```bash
git init
```

- **Keterangan:** Ini membuat direktori `.git` yang menyimpan semua informasi versi proyek.

### 2. **Clone Repositori**

Jika Anda bekerja di repositori remote (misalnya, GitHub), Anda bisa meng-clone repositori yang sudah ada.

```bash
git clone <repository-url>
```

- **Keterangan:** Ini akan membuat salinan lokal dari repositori remote.

### 3. **Melihat Status Proyek**

Untuk melihat status file yang sudah atau belum ditambahkan ke dalam tracking Git.

```bash
git status
```

- **Keterangan:** Menunjukkan file mana yang dimodifikasi, belum ditambahkan, atau siap di-commit.

### 4. **Menambahkan Perubahan ke Staging Area**

Sebelum melakukan commit, Anda harus menambahkan file yang telah dimodifikasi ke staging area menggunakan perintah:

```bash
git add <nama-file>
```

Atau untuk menambahkan semua file yang telah diubah:

```bash
git add .
```

- **Keterangan:** `git add` hanya menambahkan perubahan ke staging area, bukan langsung ke repositori.

### 5. **Commit Perubahan**

Setelah file ditambahkan ke staging area, Anda dapat melakukan commit untuk menyimpan snapshot dari perubahan.

```bash
git commit -m "Pesan commit yang jelas"
```

- **Keterangan:** `-m` digunakan untuk menambahkan pesan singkat commit. Jika mengikuti **Conventional Commit**, pesan commit harus sesuai format yang telah dibahas sebelumnya.

### 6. **Melihat Riwayat Commit**

Untuk melihat riwayat commit pada proyek Anda:

```bash
git log
```

- **Keterangan:** Ini menunjukkan daftar commit yang telah dilakukan dengan informasi seperti hash commit, penulis, dan tanggal.

### 7. **Membuat dan Berpindah Cabang (Branch)**

Cabang (branch) memungkinkan Anda untuk bekerja pada fitur baru atau perbaikan bug tanpa mempengaruhi cabang utama (`main` atau `master`).

```bash
git branch <nama-branch>
```

Berpindah ke branch lain:

```bash
git checkout <nama-branch>
```

Atau buat dan langsung pindah ke branch baru:

```bash
git checkout -b <nama-branch>
```

- **Keterangan:** Branch memungkinkan Anda bekerja secara paralel di fitur atau perbaikan yang berbeda.

### 8. **Menggabungkan (Merge) Cabang**

Setelah selesai bekerja di sebuah branch, Anda bisa menggabungkannya kembali ke cabang utama:

```bash
git checkout main  # Pindah ke branch utama
git merge <nama-branch>
```

- **Keterangan:** Ini menggabungkan perubahan dari branch lain ke branch yang aktif.

### 9. **Push ke Repositori Remote**

Untuk mengirimkan commit lokal ke repositori remote (misalnya di GitHub atau GitLab):

```bash
git push origin <nama-branch>
```

- **Keterangan:** `origin` adalah alias default untuk remote repository. Ini akan mengirimkan perubahan ke server.

### 10. **Pull Perubahan dari Remote**

Untuk menarik (fetch dan merge) perubahan terbaru dari remote repository:

```bash
git pull origin <nama-branch>
```

- **Keterangan:** Ini memastikan Anda selalu bekerja dengan versi terbaru dari kode yang ada di repositori remote.

### 11. **Mengatasi Konflik Merge**

Ketika Anda menggabungkan cabang dan terdapat konflik (dua perubahan bertentangan), Git akan meminta Anda untuk menyelesaikan konflik tersebut secara manual:

```bash
git status
# Edit file yang konflik, lalu:
git add <nama-file>
git commit
```

- **Keterangan:** Git akan menandai bagian file yang perlu diselesaikan, dan Anda harus memilih perubahan mana yang akan disimpan.

### 12. **Membatalkan Perubahan**

Untuk membatalkan perubahan pada file yang belum di-commit:

```bash
git checkout -- <nama-file>
```

Untuk membatalkan commit terakhir:

```bash
git reset --soft HEAD~1
```

- **Keterangan:** `reset --soft` akan membatalkan commit, tapi tetap menyimpan perubahan di staging area.

### Alur Umum Pekerjaan dalam Git:

1. **`git clone <repo-url>`** (untuk project baru dari remote).
2. **`git checkout -b <branch-fitur>`** (buat branch baru).
3. **`git add <file>`** (tambahkan perubahan ke staging).
4. **`git commit -m "pesan commit"`** (commit perubahan).
5. **`git push origin <branch>`** (kirim branch ke remote).
6. Buat **pull request** di platform seperti GitHub atau GitLab.
7. Review code dan **merge** ke `main`.

Alur ini membantu menjaga agar kolaborasi dan pengembangan tetap teratur, baik saat bekerja sendiri atau dalam tim.
