# Laju Reaksi dan Teori Tumbukan

Materi interaktif Kimia SMA/MA Kelas XI, Bab Laju Reaksi, Subbab 1. Halaman ini berisi konsep laju reaksi, teori tumbukan, tiga simulasi, dan latihan soal dengan pembahasan.

## Isi halaman

- **Simulasi 1: Reaksi bromin dengan asam format.** Warna larutan memudar sesuai konsentrasi Br₂, grafik konsentrasi terhadap waktu, kalkulator laju rata-rata, dan garis singgung untuk laju sesaat.
- **Simulasi 2: Uji satu tumbukan.** Siswa mengatur energi dan orientasi tumbukan, lalu melihat hasilnya pada diagram energi aktivasi.
- **Simulasi 3: Ruang partikel.** Partikel A dan B bertumbukan secara acak dan membentuk produk, disertai grafik jumlah pereaksi yang tersisa.
- **Cek pemahaman** di akhir tiap bagian dan **evaluasi akhir** berisi tujuh soal dengan skor dan pembahasan.

## Struktur file

```
laju-reaksi/
├── index.html
└── README.md
```

Seluruh CSS, JavaScript, ornamen, dan ikon tab sudah berada di dalam `index.html`. Font dimuat dari Google Fonts. Proyek ini tidak memerlukan `package.json`, proses build, atau `vercel.json`.

## Deploy ke Vercel

### Hal yang wajib dipenuhi

1. Nama file harus persis `index.html`, huruf kecil semua. Jika peramban menyimpannya sebagai `index (1).html` atau `index.html.txt`, ganti namanya terlebih dahulu.
2. `index.html` harus berada di **akar (root) repositori**, bukan di dalam subfolder. Jika file ditaruh di subfolder, isi pengaturan **Root Directory** di Vercel dengan nama subfolder tersebut.

### Cara A: lewat GitHub

1. Buat repositori baru di GitHub, lalu unggah `index.html` dan `README.md` langsung ke halaman utama repositori.
2. Buka [vercel.com](https://vercel.com), pilih **Add New → Project**, lalu impor repositori tersebut.
3. Atur seperti berikut:
   - **Framework Preset:** Other
   - **Root Directory:** `./`
   - **Build Command:** kosongkan
   - **Output Directory:** kosongkan
   - **Install Command:** kosongkan
4. Tekan **Deploy**. Setelah selesai, Vercel memberikan alamat seperti `nama-proyek.vercel.app`.

Setiap revisi cukup dilakukan dengan mengganti `index.html` di GitHub. Vercel akan men-deploy ulang secara otomatis.

### Cara B: lewat terminal

Pastikan Node.js sudah terpasang, lalu jalankan perintah berikut di dalam folder `laju-reaksi`:

```bash
npx vercel
```

Ikuti pertanyaan yang muncul dan biarkan pengaturan build kosong. Untuk menerbitkan versi publik, jalankan:

```bash
npx vercel --prod
```

## Jika halaman tidak muncul (404 atau halaman kosong)

| Gejala | Penyebab yang paling mungkin | Solusi |
|---|---|---|
| Muncul **404: NOT_FOUND** | `index.html` tidak berada di root, atau namanya berbeda | Pindahkan file ke root, atau atur Root Directory, lalu deploy ulang |
| Build gagal | Framework Preset bukan **Other**, atau ada Build Command | Ubah di **Settings → Build and Deployment**, lalu deploy ulang |
| Halaman tampil tetapi font berbeda | Koneksi internet lambat atau Google Fonts diblokir | Halaman tetap berfungsi dengan font bawaan perangkat |

## Mencoba di komputer sendiri

Buka `index.html` langsung dengan peramban dengan cara klik dua kali pada file. Halaman berjalan tanpa server.
