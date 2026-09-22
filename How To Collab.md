# Cara Kolaborasi Projek

Panduan ini menjelaskan alur kerja (workflow) untuk berkolaborasi dalam proyek ini. Harap ikuti langkah-langkah di bawah ini agar proses pengembangan berjalan lancar dan terhindar dari konflik kode.

## 1. Pemberian Akses (Tugas Pemilik Repositori)
Agar kolaborator memiliki izin untuk mengirim perubahan kode (`push`) langsung ke repositori ini, pemilik repositori harus mengundang kolaborator terlebih dahulu:

1. Buka repositori proyek di website GitHub.
2. Klik tab **Settings**, lalu pilih **Collaborators** di menu sebelah kiri.
3. Klik tombol hijau **Add people** dan ketikkan *username* GitHub kolaborator.
4. Kolaborator membuka email (atau halaman notifikasi GitHub) dan mengklik **Accept Invitation**.

## 2. Setup Proyek di Komputer Lokal (Tugas Kolaborator)
Setelah menerima undangan, salin kode proyek ke komputer lokal Anda. Buka terminal atau Command Prompt dan jalankan perintah berikut secara berurutan:

```bash
# 1. Clone repositori ke komputer lokal
git clone [https://github.com/username-teman/nama-repo.git](https://github.com/username-teman/nama-repo.git)

# 2. Masuk ke dalam folder proyek
cd nama-repo

# 3. Install dependencies (Wajib dilakukan karena folder node_modules tidak ikut diunggah)
npm install

# 4. Jalankan server lokal untuk memastikan proyek berfungsi normal
npm run dev
```

## 3. Alur Kerja Kolaborasi (Saat Mulai Coding)
Aturan Penting: Dilarang mengedit atau push kode secara langsung ke cabang main. Lakukan alur di bawah ini setiap kali Anda akan mengerjakan fitur atau bagian baru:

```bash
# 1. Buat cabang (branch) baru khusus untuk tugas Anda
git checkout -b nama-fitur-baru
# Contoh: git checkout -b update-halaman-profil

# 2. Lakukan coding di editor pilihan Anda (misalnya VS Code).

# 3. Setelah selesai, simpan perubahan ke Git
git add .

# 4. Beri pesan commit yang jelas tentang apa yang diubah
git commit -m "feat: menambahkan foto profil pengguna"

# 5. Kirim kode Anda ke branch di GitHub
git push origin nama-fitur-baru
```

## 4. Menggabungkan Kode(Merge)
Setelah Anda melakukan push, proses penggabungan kode dilakukan melalui website GitHub:

1. Buka halaman GitHub repositori ini. Akan muncul tombol Compare & pull request secara otomatis.
2. Klik tombol tersebut untuk membuat Pull Request (PR).
3. Minta anggota tim Anda untuk meninjau kodenya (Code Review). Jika disetujui dan aman, teman Anda akan mengklik Merge pull request untuk menyatukan kode Anda ke cabang `main`.
4. Setelah kode berhasil disatukan di GitHub, Anda wajib menarik versi terbarunya ke komputer Anda sebelum memulai pekerjaan baru:
```bash
git checkout main
git pull origin main
```
