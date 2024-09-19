Conventional Commits adalah spesifikasi yang digunakan untuk memberi struktur pada pesan commit dalam sistem version control, seperti Git. Tujuannya adalah untuk membuat sejarah commit yang lebih mudah dibaca dan dipahami, serta untuk memfasilitasi proses otomatis seperti pembuatan changelog, penentuan versi semantik, dan otomatisasi rilis.

Berikut adalah format dasar dari Conventional Commits:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

**Elemen penting dari format ini:**

1. **type**: Menjelaskan kategori dari commit. Beberapa tipe yang umum digunakan adalah:

   - `feat`: Menambahkan fitur baru.
   - `fix`: Memperbaiki bug.
   - `docs`: Perubahan dokumentasi.
   - `style`: Perubahan pada format atau gaya kode (misal, indentasi), tanpa mengubah logika kode.
   - `refactor`: Perubahan pada kode yang tidak memperbaiki bug atau menambah fitur, seperti perbaikan struktur kode.
   - `test`: Menambah atau memperbaiki tes.
   - `chore`: Tugas kecil atau pekerjaan yang tidak terkait langsung dengan kode aplikasi, misalnya memperbarui dependensi.

2. **optional scope**: (Opsional) Menjelaskan bagian kode yang terpengaruh, misalnya nama modul atau fungsi.

3. **description**: Deskripsi singkat, maksimal 72 karakter, yang menjelaskan perubahan yang dilakukan.

4. **optional body**: (Opsional) Penjelasan lebih rinci mengenai perubahan yang dilakukan. Bisa menjelaskan alasan perubahan atau dampaknya.

5. **optional footer**: (Opsional) Biasanya digunakan untuk memberikan informasi tambahan, seperti referensi ke issue atau bug yang diselesaikan (`Closes #123`), atau memberikan breaking change (`BREAKING CHANGE`).

### Contoh commit yang sesuai dengan Conventional Commits:

1. Commit untuk fitur baru:

   ```
   feat(authentication): add OAuth2 login
   ```

2. Commit untuk memperbaiki bug:

   ```
   fix(user-profile): resolve issue with avatar upload
   ```

3. Commit untuk perubahan yang merusak (breaking change):

   ```
   feat(database): update schema for user table

   BREAKING CHANGE: Updated user table schema to include unique constraints.
   ```

Dengan menggunakan Conventional Commits, tim dapat menjaga standar dan konsistensi dalam pesan commit, sehingga lebih mudah melacak perubahan dan mengelola proyek di masa depan.
