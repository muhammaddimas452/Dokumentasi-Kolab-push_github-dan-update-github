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

6. **Unggah ke GitHub (Push)**  
   Kirimkan perubahan dari komputer lokal ke repositori online GitHub Anda:
   ```bash
   git push origin main
   ```
   > **Catatan:** Ganti `main` dengan `master` jika repositori Anda masih menggunakan nama *branch* utama yang lama.
