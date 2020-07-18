UAS-Web-2
Ini Adalah Aplikasi PHP Sederhana Untuk Pendataan Zakat
Ini Merupakan Tugas UAS untuk Pemrograman WEB 2

Kelompok 4 Kelas 06TPLM010
Fikri Mutaqin
Guntur Leon Saputra
Hesti Rahmawati
Ichwanul Syarif H.
Ilham Dwi Nugraha

Penjelasan
folder assets
Terdapat framework boostrap untuk mengatur tampilan
Terdapat library fpdf untuk mencetak laporan dalam bentuk pdf

Pada file koneksi.php
Tedapat Fungsi PHP mysqli_connect untuk menghubungkan ke databasenya

Pada file login.php
terdapat fungsi php isset($_GET['pesan']) untuk mengecek notifikasi apakah user dalam keadaan login / tidak
tedapat form untuk login dengan method post untuk mengirimkan data, pada form juga terdapat action'file_tujuan.php untuk menentukan file tujuan setelah submit

pada file cek_login.php
terdapat fungsi session_start untuk inisialisasi / mengaktifkan session
terdapat funsgi php include 'koneksi.php' untuk menghubungkan dengan file koneksi.php
terdapat fungsi $_POST['...'] untuk mendapatkan nilai dari form sebelumnya
tedapat fungsi mysqli_query untuk mendapatkan semua data admin
terdapat fungsi mysqli_num_rows($data) untuk mengecek apakah data username dan password ada pada database , jika ada fungsi ini mereturn nilai 1
jika username dan password sesuai dengan db akan dilanjutkan dengan fungsi mysqli_query lagi untuk mendapatkan id username tersebut dan kemudian buat session untuk menyimpan id_admin dan juga session status login. kemudian terdapat fungsi header(...); untuk mengalihkan halaman ke halaman utama

pada file index.php
terdapat fungsi session_start untuk inisialisasi / mengaktifkan session
terdapat funsgi php include 'koneksi.php' untuk menghubungkan dengan file koneksi.php
terdapat fungsi isset($_GET[...]) untuk mengecek notifikasi apakah user dalam keadaan login / tidak
terdapat sidebar untuk navigasi
terdapat keterangan aplikasi

pada file list_data.php
terdapat fungsi session_start untuk inisialisasi / mengaktifkan session
terdapat funsgi php include 'koneksi.php' untuk menghubungkan dengan file koneksi.php
terdapat fungsi isset($_GET[...]) untuk mengecek notifikasi apakah user dalam keadaan login / tidak
terdapat juga fungsi session_start untuk mengecek notifikasi apakah berhasil menghapus / mengedit data
terdapat sidebar untuk navigasi
terdapat fungsi mysqli_query dengan isis query inner join untuk mendapatkan nilai pada database tabel_zakat dan tabel_admin
mysqli_num_rows untuk mendapatkan data tersebut , fungsi ini di loop untuk mendapatkan semua data
terdapat button hapus dan edit yang jika diklik akan dialihkan ke manu edit / meenghapus data

pada file add_data.php
terdapat fungsi session_start untuk inisialisasi / mengaktifkan session
terdapat funsgi php include 'koneksi.php' untuk menghubungkan dengan file koneksi.php
terdapat fungsi isset($_GET[...]) untuk mengecek notifikasi apakah user dalam keadaan login / tidak
terdapat juga fungsi session_start untuk mengecek notifikasi apakah berhasil menambahkan data
terdapat sidebar untuk navigasi
terdapat form dengan method post , dan action ke ce_tambah_data.php
terdapat fungsi mysqli_query untuk mendapatkan semua data pada database tabel zakat, untuk fitur dropdown

pada file cek_tambah_data.php
terdapat fungsi session_start untuk inisialisasi / mengaktifkan session
terdapat funsgi php include 'koneksi.php' untuk menghubungkan dengan file koneksi.php
terdapat fungsi isset($_GET[...]) untuk mengecek notifikasi apakah user dalam keadaan login / tidak
terdapat method $_POST[..] untuk mendapatkan data dari form
terdapat $_SESSIO[id_admin] untuk mendapakan data id_admin
terdapat mysqli_query dengan metode sql SELECT untuk mendapatkan id_zakat dari jenis_zakat
terdapat mysqli_query dengan metode sql INSERT untuk menambahan data tesebut ke database
jika berhasil halaman akan dialihkan ke halaman add_data.php dengan mengirim pesan 'berhasil_menambahkan_data'
jika gagal halaman akan dialihkan ke halaman add_data.php dengan mengirim pesan 'gagal_menambahkan_data'

pada file edit_data.php
terdapat fungsi session_start untuk inisialisasi / mengaktifkan session
terdapat funsgi php include 'koneksi.php' untuk menghubungkan dengan file koneksi.php
terdapat fungsi $_GET[id] untuk mendapatkan id_pembayaran
terdapat form dengan method get dan action ke cek_edit data untuk proses edit data ke database
terdapat fungsi php mysqli_query dengan syntaks select untuk mendapatkan data dari database pembayaran kemudian data
tersebut di letakan pada value form untuk empermudah proses edit data

pada file cek_ubah_data.php
terdapat fungsi session_start untuk inisialisasi / mengaktifkan session
terdapat fungsi php include 'koneksi.php' untuk menghubungkan dengan file koneksi.php
terdapat fungsi mysqli_query dengan syntaks select untuk mendapatkan data zakat dari acuan id zakat

pada file print_data.php
pada file ini menggunakan library fpdf untuk proses mencetak data
data diambil dari database dengan perintah mysqli_query select dan inner join untuk menghubungkan dua tabel
terdapat fungsi mysqli_query dengan syntaks update untuk mengubah data dengan titik acuan id_pembayaran

pada file logut.php
session_start() mengaktifkan session
session_destroy() untuk menghapus semua session
header("location:login.php?pesan=logout") mengalihkan halaman sambil mengirim pesan logout
