Berikut adalah daftar perintah Git beserta penjelasan lengkapnya:

### 1. **`git init`**

Inisialisasi repositori Git baru di direktori saat ini.

```bash
git init
```

- Membuat direktori `.git` di dalam folder proyek Anda untuk melacak perubahan versi.

### 2. **`git clone`**

Mengunduh (clone) repositori dari remote ke direktori lokal.

```bash
git clone <repository-url>
```

- Membuat salinan repositori yang ada di URL tertentu ke direktori lokal.

### 3. **`git status`**

Menampilkan status repositori, termasuk file yang telah dimodifikasi, staged, atau belum di-tracking.

```bash
git status
```

- Memeriksa status file di repositori.

### 4. **`git add`**

Menambahkan file ke **staging area** sebelum melakukan commit.

```bash
git add <file>
git add .
```

- `git add <file>` menambahkan file tertentu ke staging, sedangkan `git add .` menambahkan semua perubahan ke staging.

### 5. **`git commit`**

Menyimpan snapshot perubahan yang telah ditambahkan ke staging area.

```bash
git commit -m "Pesan commit"
```

- `-m` digunakan untuk menambahkan pesan commit singkat.

### 6. **`git log`**

Melihat riwayat commit dalam repositori.

```bash
git log
```

- Menampilkan daftar commit, termasuk hash commit, penulis, dan tanggal.

### 7. **`git diff`**

Melihat perbedaan antara file yang belum di-commit atau yang ada di staging area.

```bash
git diff
git diff --staged
```

- `git diff` membandingkan perubahan yang belum di-stage, sedangkan `git diff --staged` membandingkan file yang sudah di-stage.

### 8. **`git branch`**

Melihat, membuat, atau menghapus cabang (branch) di repositori.

```bash
git branch
git branch <nama-branch>
git branch -d <nama-branch>
```

- `git branch` tanpa parameter akan menampilkan daftar branch saat ini.

### 9. **`git checkout`**

Berpindah ke branch lain atau memeriksa versi file yang lebih lama.

```bash
git checkout <nama-branch>
git checkout -b <nama-branch>
```

- `-b` digunakan untuk membuat branch baru sekaligus berpindah ke branch tersebut.

### 10. **`git merge`**

Menggabungkan perubahan dari satu branch ke branch yang aktif.

```bash
git merge <nama-branch>
```

### 11. **`git pull`**

Menarik (fetch) dan menggabungkan (merge) perubahan dari remote ke cabang lokal.

```bash
git pull origin <branch>
```

### 12. **`git push`**

Mengirimkan commit dari branch lokal ke repositori remote.

```bash
git push origin <branch>
```

### 13. **`git fetch`**

Mengambil data terbaru dari remote tanpa menggabungkannya ke branch lokal.

```bash
git fetch
```

### 14. **`git reset`**

Membatalkan perubahan dalam staging atau menghapus commit dari riwayat commit.

```bash
git reset <file>
git reset --soft HEAD~1
git reset --hard HEAD~1
```

- `--soft` hanya membatalkan commit terakhir, tapi tetap menyimpan perubahan di staging area.
- `--hard` menghapus commit dan perubahan lokal.

### 15. **`git revert`**

Membuat commit baru yang membatalkan perubahan dari commit tertentu.

```bash
git revert <hash-commit>
```

### 16. **`git stash`**

Menyimpan perubahan lokal sementara untuk melanjutkan nanti.

```bash
git stash
git stash apply
git stash drop
```

- `git stash` menyimpan perubahan yang belum di-commit, `git stash apply` mengembalikannya, dan `git stash drop` menghapus stash.

### 17. **`git tag`**

Menandai (tag) titik tertentu dalam riwayat commit sebagai versi tertentu.

```bash
git tag <nama-tag>
git push origin <nama-tag>
```

### 18. **`git remote`**

Mengelola remote repository (misalnya, GitHub atau GitLab).

```bash
git remote add origin <repository-url>
git remote -v
```

- `git remote add` menambahkan remote, `git remote -v` menampilkan daftar remote yang ada.

### 19. **`git rm`**

Menghapus file dari repositori Git dan sistem file.

```bash
git rm <file>
```

### 20. **`git mv`**

Memindahkan atau mengganti nama file yang sudah ada dalam tracking Git.

```bash
git mv <file-lama> <file-baru>
```

### 21. **`git rebase`**

Menggabungkan perubahan dari satu branch ke branch lain dengan cara yang lebih bersih dibanding merge.

```bash
git rebase <branch>
```

### 22. **`git cherry-pick`**

Menyalin commit tertentu dari satu branch ke branch lain.

```bash
git cherry-pick <hash-commit>
```

### 23. **`git bisect`**

Membantu menemukan commit yang menyebabkan bug dengan metode binary search.

```bash
git bisect start
git bisect good <hash>
git bisect bad <hash>
```

### 24. **`git blame`**

Menampilkan siapa yang terakhir memodifikasi setiap baris dalam file.

```bash
git blame <file>
```

### 25. **`git show`**

Menampilkan detail dari commit tertentu.

```bash
git show <hash-commit>
```

### 26. **`git archive`**

Membuat arsip (zip atau tar) dari file dalam revisi tertentu.

```bash
git archive --format=zip HEAD > repo.zip
```

### 27. **`git gc`**

Mengoptimalkan repositori Git dengan membersihkan data yang tidak diperlukan.

```bash
git gc
```

### 28. **`git config`**

Mengatur konfigurasi Git, seperti nama pengguna dan email.

```bash
git config --global user.name "Nama Anda"
git config --global user.email "email@example.com"
```

### 29. **`git clean`**

Menghapus file yang tidak dilacak (untracked files) dari direktori kerja.

```bash
git clean -f
```

### 30. **`git ls-files`**

Menampilkan file yang sedang dilacak oleh Git.

```bash
git ls-files
```

---

Perintah-perintah ini memberikan fleksibilitas penuh dalam mengelola proyek, baik itu versi kontrol lokal maupun berkolaborasi melalui remote.
