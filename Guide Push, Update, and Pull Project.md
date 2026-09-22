# Cara Mengunggah (Push) Proyek Baru ke GitHub

Jika Anda memiliki proyek baru di komputer lokal dan ingin mengunggahnya ke repositori GitHub untuk pertama kali, ikuti langkah-langkah berikut.

## Prasyarat
1. Pastikan Anda sudah membuat repositori baru yang kosong di situs GitHub.
2. Salin URL repositori tersebut (misalnya: `https://github.com`).

## Langkah-Langkah

1. **Buka Terminal / Command Prompt**  
   Masuk ke dalam folder proyek lokal Anda:
   ```bash
   cd nama-folder-proyek
   ```

2. **Inisialisasi Git**  
   Aktifkan Git di dalam folder proyek tersebut:
   ```bash
   git init
   ```

3. **Tambahkan File ke Staging Area**  
   Pilih semua file dalam folder untuk didaftarkan ke Git:
   ```bash
   git add .
   ```

4. **Lakukan Commit Pertama**  
   Simpan perubahan pertama Anda dengan pesan:
   ```bash
   git commit -m "First commit / Inisialisasi proyek"
   ```

5. **Tentukan Branch Utama**  
   Ubah nama *branch* utama menjadi `main` (standar GitHub saat ini):
   ```bash
   git branch -M main
   ```

6. **Hubungkan dengan Repositori GitHub**  
   Sambungkan folder lokal Anda dengan URL repositori GitHub yang sudah dibuat tadi:
   ```bash
   git remote add origin https://github.com
   ```

7. **Unggah Proyek (Push)**  
   Kirim seluruh kode proyek Anda ke GitHub untuk pertama kalinya:
   ```bash
   git push -u origin main
   ```
   > **Catatan:** Parameter `-u` berfungsi untuk mengingat *branch* tujuan, sehingga untuk *push* berikutnya Anda cukup mengetik `git push`.

# Panduan Update Proyek ke GitHub

Berikut adalah langkah-langkah untuk memperbarui (*update*) proyek Anda dari komputer lokal ke repositori GitHub menggunakan Git.

## Langkah-Langkah

1. **Buka Terminal / Command Prompt**  
   Buka aplikasi terminal di komputer Anda.

2. **Masuk ke Direktori Proyek**  
   Pindah ke dalam folder proyek yang ingin Anda update:
   ```bash
   cd nama-folder-proyek
   ```

3. **Periksa Status File**  
   Cek file mana saja yang telah Anda ubah atau tambahkan:
   ```bash
   git status
   ```

4. **Tambahkan Perubahan ke Staging Area**  
   Pilih semua file yang berubah untuk bersiap diunggah:
   ```bash
   git add .
   ```

5. **Simpan Perubahan (Commit)**  
   Simpan perubahan tersebut dengan memberikan pesan singkat yang jelas:
   ```bash
   git commit -m "Tuliskan pesan penjelasan update di sini"
   ```
   > **Catatan:** Gunakan format Commit yang jelas: Contohnya menggunakan konvensi Conventional Commits seperti `feat: ...` (fitur baru), `fix: ...` (perbaikan bug), atau `style: ...` (perubahan CSS).

6. **Unggah ke GitHub (Push)**  
   Kirimkan perubahan dari komputer lokal ke repositori online GitHub Anda:
   ```bash
   git push origin main
   ```
   > **Catatan:** Ganti `main` dengan `master` jika repositori Anda masih menggunakan nama *branch* utama yang lama.


# Cara Mengambil Update dari GitHub ke Komputer Lokal

Jika ada perubahan di repositori GitHub (misalnya karena perubahan langsung di web GitHub atau ada *developer* lain yang melakukan *push*), Anda harus menarik perubahan tersebut ke komputer lokal agar proyek Anda tetap *up-to-date*.

## Langkah-Langkah

1. **Buka Terminal / Command Prompt**  
   Pastikan Anda sudah berada di dalam folder proyek Anda:
   ```bash
   cd nama-folder-proyek
   ```

2. **Periksa Branch Aktif**  
   Pastikan Anda berada di *branch* yang sama dengan yang ada di GitHub (biasanya `main` atau `master`):
   ```bash
   git branch
   ```

3. **Tarik Pembaruan (Pull)**  
   Jalankan perintah berikut untuk mengambil dan menggabungkan langsung perubahan terbaru ke proyek lokal Anda:
   ```bash
   git pull origin main
   ```
   > **Catatan:** Ganti `main` dengan nama *branch* yang sesuai jika Anda bekerja di *branch* lain.

## Tips Tambahan: Hanya Cek Perubahan (Fetch)
Jika Anda hanya ingin mengecek apakah ada update di GitHub tanpa langsung menggabungkannya ke file lokal, gunakan perintah:
```bash
git fetch origin
```

