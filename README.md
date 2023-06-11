# UAP-KINERJA

**1. Buat direktori dengan nama UAP-Adsis, isi dengan file txt dengan format penamaan catatannya-.txt, kemudian isi file txt tersebut dengan nama dan NIM kamu. Kemudian atur permission view-only pada file tersebut untuk user biasa. Tunjukkan bukti berupa screenshot yang menunjukkan bahwa file tersebut berhasil diatur permissionnya menjadi view-only untuk user biasa.**

**Screenshoot**

<p align="center">
  <img src="https://github.com/fauzanzakaria/UAP-KINERJA_ADSIS/blob/6f456c4680322d16e6284f31cab7e66b2aaa02ce/Screenshoot/1%20Membuat%20Direktori%20UAP-Adsis.png" >
</p>
<p align="center">Membuat direktori baru UAP-Adsis dengan perintah mkdir</p>

<p align="center">
  <img src="https://github.com/fauzanzakaria/UAP-KINERJA_ADSIS/blob/78f1af57f03d3f17b73890ac9af9fc14243516f3/Screenshoot/1%20Membuat%20file.txt.png" >
</p>
<p align="center">Membuat file.txt dengan nama catatannya-fauzan.txt dan mengisinya dengan perintah sudo nano</p>

<p align="center">
  <img src="https://github.com/fauzanzakaria/UAP-KINERJA_ADSIS/blob/78f1af57f03d3f17b73890ac9af9fc14243516f3/Screenshoot/1%20Mengisi%20file.txt.png" >
</p>
<p align="center">Mengisi catatannya-fauzan.txt dengan NAMA dan NIM</p>

<p align="center">
  <img src="https://github.com/fauzanzakaria/UAP-KINERJA_ADSIS/blob/78f1af57f03d3f17b73890ac9af9fc14243516f3/Screenshoot/1%20Mengubah%20Permission.png" >
</p>
<p align="center">Mengubah Permission catatannya-fauzan.txt ke view-only dengan perintah chmod 400</p>

**2. Lakukan konfigurasi alamat IP address sementara pada sistem dan default gateway. (petunjuk 192.168.56.x | x adalah nomor absen)**

**Screenshoot**

<p align="center">
  <img src="https://github.com/fauzanzakaria/UAP-KINERJA_ADSIS/blob/78f1af57f03d3f17b73890ac9af9fc14243516f3/Screenshoot/2%20Melihat%20IP.png" >
</p>
<p align="center">Melihat ip dengan perintah ifconfig</p>

<p align="center">
  <img src="https://github.com/fauzanzakaria/UAP-KINERJA_ADSIS/blob/78f1af57f03d3f17b73890ac9af9fc14243516f3/Screenshoot/2%20Mengubah%20IP.png" >
</p>
<p align="center">Mengubah IP dengan perintah sudo ifconfig ens33 192.168.56.11 netmask 255.255.255.0</p>

<p align="center">
  <img src="https://github.com/fauzanzakaria/UAP-KINERJA_ADSIS/blob/78f1af57f03d3f17b73890ac9af9fc14243516f3/Screenshoot/2%20Menambahkan%20default%20gateway.png" >
</p>
<p align="center">Menambahkan default gateway dengan perintah sudo route add default gw 192.168.56.110 ens33</p>

**3. Lakukan Instalasi Webmin lalu buatlah user bernama nama anda, lalu buat group Adsis_(kelas masing-masing) dan masukkan nama anda di group**

**Screenshoot**

<p align="center">
  <img src="https://github.com/fauzanzakaria/UAP-KINERJA_ADSIS/blob/78f1af57f03d3f17b73890ac9af9fc14243516f3/Screenshoot/3%20Install%20Webmin.png" >
</p>
<p align="center">Menginstall Webmin</p>

<p align="center">
  <img src="https://github.com/fauzanzakaria/UAP-KINERJA_ADSIS/blob/78f1af57f03d3f17b73890ac9af9fc14243516f3/Screenshoot/3%20Membuat%20group%20dan%20memasukkan%20user.png" >
</p>
<p align="center">Membuat groups baru dengan nama Adsis_E lalu masukkan user fauzan didalamnya</p>

<p align="center">
  <img src="https://github.com/fauzanzakaria/UAP-KINERJA_ADSIS/blob/78f1af57f03d3f17b73890ac9af9fc14243516f3/Screenshoot/3%20Cek%20groups%20dan%20user.png" >
</p>
<p align="center">Groups Adsis_E dengan id 1009 dengan user fauzan berhasil ditambahkan</p>

**4. akukan ping ke alamat ip anda dan coba lakukan reject dan drop di webmin, lalu analisis apa yang terjadi?**

**Screenshoot**

<p align="center">
  <img src="https://github.com/fauzanzakaria/UAP-KINERJA_ADSIS/blob/78f1af57f03d3f17b73890ac9af9fc14243516f3/Screenshoot/4%20Setting.jpg" >
</p>
<p align="center">Mengubah konfigurasi reject dan drop</p>

<p align="center">
  <img src="https://github.com/fauzanzakaria/UAP-KINERJA_ADSIS/blob/78f1af57f03d3f17b73890ac9af9fc14243516f3/Screenshoot/4%20Test%20ping.jpg" >
</p>
<p align="center">Menjalankan test ping</p>

**Penjelasan**

Dapat disimpulkan saat kita merubah setting ke reject saat di lakukan test ping maka yang terjadi adalah Destination port unreachable. sedangkan kalau kita drop maka tidak akan terjadi balasan sama sekali karena pengiriman pake telah sepenuhnya di tolak

**5. Buatlah perintah otomatis yang berfungsi untuk ping www.filkom.ub.ac.id**

**Screenshoot**

<p align="center">
  <img src="https://github.com/fauzanzakaria/UAP-KINERJA_ADSIS/blob/78f1af57f03d3f17b73890ac9af9fc14243516f3/Screenshoot/5%20Memasukkan%20perintah.png" >
</p>
<p align="center">Menambahkan perintah */3 * * * * ping filkom.ub.ac.id</p>

<p align="center">
  <img src="https://github.com/fauzanzakaria/UAP-KINERJA_ADSIS/blob/78f1af57f03d3f17b73890ac9af9fc14243516f3/Screenshoot/5%20Hasilnya.png" >
</p>
<p align="center">Hasil dari perintah */3 * * * * ping filkom.ub.ac.id</p>

**Penjelasan**

Sistem akan secara otomatis melakukan ping ke filkom.ub.ac.id setiap 3 menit sekali. Gambar yang disertakan menunjukkan bahwa ada selisih waktu 3 menit di antara setiap pengiriman ping yang ditunjukkan dalam keterangan waktu