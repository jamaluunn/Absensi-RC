\# 🤖 Bot Absensi Telegram



Bot Telegram multifungsi yang dirancang untuk mengelola absensi karyawan secara real-time, lengkap dengan fitur manajemen, pelaporan, dan sistem persetujuan.



---



\## ✨ Fitur



\-   \*\*Absensi Masuk \& Pulang\*\*: Karyawan dapat melakukan absensi dengan mengirimkan foto selfie dan lokasi.

\-   \*\*Geofencing (Radius Absensi)\*\*: Membatasi area absensi hanya dalam jarak tertentu dari lokasi kantor.

\-   \*\*Notifikasi Real-time\*\*: Admin menerima notifikasi lengkap (termasuk foto dan peta lokasi) setiap kali ada karyawan yang absen.

\-   \*\*Manajemen Karyawan\*\*:

&nbsp;   -   Tambah karyawan baru.

&nbsp;   -   Aktifkan \& Nonaktifkan akun karyawan.

&nbsp;   -   Hapus data karyawan secara permanen.

\-   \*\*Sistem Pengajuan\*\*: Alur untuk pengajuan Izin dan Kasbon dengan sistem persetujuan (approve/reject) oleh admin.

\-   \*\*Broadcast\*\*: Admin dapat mengirim pesan pengumuman (teks atau foto dengan caption) ke semua karyawan aktif.

\-   \*\*Laporan Otomatis\*\*: Laporan absensi harian, mingguan, dan bulanan.

\-   \*\*Pengaturan Dinamis\*\*: Admin dapat mengubah pengaturan seperti status dan jarak radius absensi langsung dari bot.

\-   \*\*Struktur Modular\*\*: Kode dipecah menjadi beberapa file untuk kemudahan pengelolaan dan pengembangan lebih lanjut.



---



\## 📁 Struktur Folder Proyek



Pastikan semua file berada di lokasi yang benar sesuai struktur di bawah ini.



AbsensiBot/

├──  handlers/

│   ├── init.py

│   ├── admin.py

│   ├── karyawan.py

│   └── common.py

│

├── .env

├── bot.py

├── config.py

├── database.py

├── requirements.txt

└── setup.py



---



\## ⚙️ Cara Setup



Ikuti langkah-langkah berikut untuk menjalankan bot dari awal.



\### 1. Pra-syarat

\-   \*\*Python 3.9+\*\* terinstal di komputer Anda.

\-   Memiliki akses ke \*\*Terminal\*\* atau \*\*Command Prompt\*\*.



\### 2. Siapkan Kode

\-   Salin semua kode dari tutorial ini ke dalam file yang sesuai di folder `AbsensiBot/`.



\### 3. Lingkungan Python \& Instalasi

Sangat disarankan menggunakan \*virtual environment\*.



1\.  Buka terminal, masuk ke folder `AbsensiBot/`.

2\.  Buat virtual environment:

&nbsp;   ```bash

&nbsp;   python -m venv venv

&nbsp;   ```

3\.  Aktifkan:

&nbsp;   -   \*\*Windows\*\*: `.\\venv\\Scripts\\activate`

&nbsp;   -   \*\*macOS / Linux\*\*: `source venv/bin/activate`

4\.  Instal semua library yang dibutuhkan:

&nbsp;   ```bash

&nbsp;   pip install -r requirements.txt

&nbsp;   ```



\### 4. Dapatkan Token Bot \& ID Admin

1\.  \*\*Token Bot\*\*:

&nbsp;   -   Buka Telegram, cari \*\*@BotFather\*\*.

&nbsp;   -   Kirim `/newbot` dan ikuti instruksi untuk membuat bot baru.

&nbsp;   -   Salin \*\*token API\*\* yang diberikan.

2\.  \*\*ID Admin\*\*:

&nbsp;   -   Buka Telegram, cari \*\*@userinfobot\*\*.

&nbsp;   -   Kirim `/start`, dan bot tersebut akan memberikan User ID Anda. Salin ID tersebut.



\### 5. Konfigurasi File `.env`

1\.  Di folder `AbsensiBot/`, buat file baru bernama `.env`.

2\.  Isi file tersebut dengan format berikut:



&nbsp;   ```env

&nbsp;   TELEGRAM\_TOKEN=123456:ABC-DEF1234ghIkl-zyx57W2v1u123456

&nbsp;   ADMIN\_IDS=111222333

&nbsp;   ```



3\.  Ganti isinya:

&nbsp;   -   `TELEGRAM\_TOKEN`: Ganti dengan token dari BotFather.

&nbsp;   -   `ADMIN\_IDS`: Ganti dengan User ID Anda. Jika admin lebih dari satu, pisahkan dengan koma (contoh: `111222333,444555666`).



\### 6. Setup Database

Jalankan perintah ini \*\*sekali saja\*\* untuk membuat file `absensi.db` dan tabel-tabel di dalamnya.



```bash

python setup.py

### 7. Jalankan Bot

Ini adalah langkah terakhir untuk menghidupkan bot Anda.



```bash

python bot.py



Jika berhasil, akan muncul log Bot Absensi Dijalankan... di terminal Anda. Bot siap digunakan.

