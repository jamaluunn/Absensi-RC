🤖 Bot Absensi Telegram
Bot Telegram multifungsi yang dirancang untuk mengelola absensi karyawan secara real-time, lengkap dengan fitur manajemen, pelaporan, dan sistem persetujuan.

✨ Fitur
Absensi Masuk & Pulang: Karyawan dapat melakukan absensi dengan mengirimkan foto selfie dan lokasi.

Geofencing (Radius Absensi): Membatasi area absensi hanya dalam jarak tertentu dari lokasi kantor.

Notifikasi Real-time: Admin menerima notifikasi lengkap (termasuk foto dan peta lokasi) setiap kali ada karyawan yang absen.

Manajemen Karyawan:

Tambah karyawan baru.

Aktifkan & Nonaktifkan akun karyawan.

Hapus data karyawan secara permanen.

Sistem Pengajuan: Alur untuk pengajuan Izin dan Kasbon dengan sistem persetujuan (approve/reject) oleh admin.

Broadcast: Admin dapat mengirim pesan pengumuman (teks atau foto dengan caption) ke semua karyawan aktif.

Laporan Otomatis: Laporan absensi harian, mingguan, dan bulanan.

Pengaturan Dinamis: Admin dapat mengubah pengaturan seperti status dan jarak radius absensi langsung dari bot.

Struktur Modular: Kode dipecah menjadi beberapa file untuk kemudahan pengelolaan dan pengembangan lebih lanjut.

📁 Struktur Folder Proyek
Pastikan semua file berada di lokasi yang benar sesuai struktur di bawah ini.

AbsensiBot/
├── .env
├── bot.py
├── config.py
├── database.py
├── requirements.txt
├── setup.py
└── handlers/
    ├── __init__.py
    ├── admin.py
    ├── common.py
    └── karyawan.py

⚙️ Cara Setup
Ikuti langkah-langkah berikut untuk menjalankan bot dari awal.

1. Pra-syarat
Python 3.9+ terinstal di komputer Anda.

Memiliki akses ke Terminal atau Command Prompt.

2. Siapkan Kode
Salin semua kode dari tutorial ini ke dalam file yang sesuai di folder AbsensiBot/.

3. Lingkungan Python & Instalasi
Sangat disarankan menggunakan virtual environment.

Buka terminal, lalu masuk ke folder AbsensiBot/.

Buat virtual environment:

python -m venv venv

Aktifkan virtual environment:

Windows: .\venv\Scripts\activate

macOS / Linux: source venv/bin/activate

Instal semua library yang dibutuhkan:

pip install -r requirements.txt

4. Dapatkan Token Bot & ID Admin
Token Bot:

Buka Telegram, cari @BotFather.

Kirim /newbot dan ikuti instruksi untuk membuat bot baru.

Salin token API yang diberikan.

ID Admin:

Buka Telegram, cari @userinfobot.

Kirim /start, dan bot tersebut akan memberikan User ID Anda. Salin ID tersebut.

5. Konfigurasi File .env
Di dalam folder AbsensiBot/, buat file baru bernama .env.

Isi file tersebut dengan format berikut, ganti dengan data Anda:

TELEGRAM_TOKEN=123456:ABC-DEF1234ghIkl-zyx57W2v1u123456
ADMIN_IDS=111222333

TELEGRAM_TOKEN: Ganti dengan token dari BotFather.

ADMIN_IDS: Ganti dengan User ID Anda. Jika admin lebih dari satu, pisahkan dengan koma (contoh: 111222333,444555666).

6. Setup Database
Jalankan perintah ini sekali saja untuk membuat file absensi.db dan tabel-tabel di dalamnya.

python setup.py

7. Jalankan Bot
Ini adalah langkah terakhir untuk menghidupkan bot Anda.

python bot.py

Jika berhasil, akan muncul log Bot Absensi Dijalankan... di terminal Anda. Bot siap digunakan.
