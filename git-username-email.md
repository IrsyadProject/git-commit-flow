Jika Anda ingin menetapkan email dan nama pada satu proyek Git saja (bukan secara global), Anda bisa mengkonfigurasi Git di tingkat repository lokal. Berikut langkah-langkahnya:

### Mengatur Nama dan Email untuk Satu Proyek

1. **Masuk ke Direktori Proyek**

   Pastikan Anda berada di direktori proyek Git yang ingin diubah.

   ```bash
   cd /path/to/your/project
   ```

2. **Setel Nama dan Email untuk Proyek Tersebut**

   Gunakan perintah `git config` dengan opsi `--local` untuk menetapkan nama dan email hanya untuk repository ini.

   ```bash
   git config user.name "Nama Anda"
   git config user.email "email_anda@example.com"
   ```

   Perintah ini akan menyimpan konfigurasi di file `.git/config` di dalam direktori proyek Anda.

3. **Verifikasi Konfigurasi**

   Untuk memastikan bahwa nama dan email telah diset, Anda bisa memeriksa konfigurasi Git untuk proyek tersebut:

   ```bash
   git config --get user.name
   git config --get user.email
   ```

   Ini akan menampilkan nama dan email yang telah Anda setel untuk proyek ini.

### Mengubah Email dan Nama pada Commit yang Ada

Jika Anda ingin mengubah nama dan email pada commit yang sudah ada di proyek ini, Anda bisa menggunakan `git rebase` atau `git filter-branch` seperti yang dijelaskan sebelumnya. Namun, perubahan ini akan mengubah riwayat commit dan mungkin memerlukan force push jika sudah di-push ke remote repository.

### Contoh: Mengubah Email dan Nama untuk Commit yang Sudah Ada

1. **Mulai Rebase Interaktif**

   ```bash
   git rebase -i HEAD~N  # Ganti N dengan jumlah commit yang ingin diubah
   ```

2. **Edit Commit**

   Ubah `pick` menjadi `edit` pada commit yang ingin diubah, kemudian untuk setiap commit yang diedit:

   ```bash
   GIT_COMMITTER_NAME="Nama Baru" GIT_COMMITTER_EMAIL="email_baru@example.com" git commit --amend --author="Nama Baru <email_baru@example.com>"
   git rebase --continue
   ```

3. **Push Perubahan**

   Setelah mengubah commit, jika repository sudah di-push ke remote, Anda perlu melakukan force push:

   ```bash
   git push --force
   ```

Dengan langkah-langkah ini, Anda dapat menetapkan nama dan email hanya untuk proyek Git tertentu tanpa mempengaruhi konfigurasi global Git Anda.
