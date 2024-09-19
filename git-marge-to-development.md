Jika Anda ingin **merge** branch `feature/satusehat-v2` ke branch `development`, ikuti langkah-langkah berikut:

### 1. **Pastikan Branch `development` Terupdate**

Pertama, pastikan branch `development` Anda terupdate dengan remote repository. Checkout ke branch `development` dan lakukan pull untuk mendapatkan perubahan terbaru dari remote:

```bash
git checkout development
git pull origin development
```

### 2. **Merge Branch `feature/satusehat-v2` ke `development`**

Setelah branch `development` terupdate, Anda dapat melakukan merge branch `feature/satusehat-v2` ke `development`:

```bash
git merge feature/satusehat-v2
```

### 3. **Selesaikan Konflik (jika ada)**

Jika ada konflik selama proses merge, git akan memberi tahu file mana yang mengalami konflik. Anda perlu menyelesaikan konflik dengan:

- Membuka file yang mengalami konflik.
- Mengedit file untuk memilih atau menggabungkan bagian kode yang benar.
- Setelah menyelesaikan konflik, tandai file sebagai selesai diperbaiki dengan:

  ```bash
  git add <file-yang-diperbaiki>
  ```

### 4. **Commit Hasil Merge**

Jika ada konflik, setelah Anda menyelesaikannya, Anda perlu melakukan commit hasil merge:

```bash
git commit
```

Jika tidak ada konflik, git biasanya otomatis melakukan commit setelah merge selesai.

### 5. **Push Perubahan ke Remote**

Setelah merge selesai dan commit sudah dilakukan, push perubahan ke remote repository:

```bash
git push origin development
```

### Ringkasan Perintah

1. **Checkout dan update branch `development`:**

   ```bash
   git checkout development
   git pull origin development
   ```

2. **Merge branch `feature/satusehat-v2` ke `development`:**

   ```bash
   git merge feature/satusehat-v2
   ```

3. **Selesaikan konflik dan commit (jika ada):**

   ```bash
   git add <file-yang-diperbaiki>
   git commit
   ```

4. **Push perubahan ke remote:**

   ```bash
   git push origin development
   ```

Dengan langkah-langkah ini, Anda dapat menggabungkan perubahan dari branch `feature/satusehat-v2` ke branch `development` dan memperbarui repository remote dengan hasil merge tersebut. Jika ada masalah atau pertanyaan lebih lanjut, jangan ragu untuk bertanya!
