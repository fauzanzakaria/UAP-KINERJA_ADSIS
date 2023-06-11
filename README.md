# UAP-KINERJA

**1. Buat direktori dengan nama UAP-Adsis, isi dengan file txt dengan format penamaan catatannya-.txt, kemudian isi file txt tersebut dengan nama dan NIM kamu. Kemudian atur permission view-only pada file tersebut untuk user biasa. Tunjukkan bukti berupa screenshot yang menunjukkan bahwa file tersebut berhasil diatur permissionnya menjadi view-only untuk user biasa.**

**Screenshoot**

<p align="center">
  <img src="/workspaces/UAP-KINERJA_ADSIS/Screenshoot/1 Membuat Direktori UAP-Adsis.png" >
</p>
<p align="center">Membuat direktori baru UAP-Adsis dengan perintah mkdir</p>

<p align="center">
  <img src="/workspaces/UAP-KINERJA_ADSIS/Screenshoot/1 Membuat file.txt.png" >
</p>
<p align="center">Membuat file.txt dengan nama catatannya-fauzan.txt dan mengisinya dengan perintah sudo nano</p>

<p align="center">
  <img src="/workspaces/UAP-KINERJA_ADSIS/Screenshoot/1 Mengisi file.txt.png" >
</p>
<p align="center">Mengisi catatannya-fauzan.txt dengan NAMA dan NIM</p>

<p align="center">
  <img src="/workspaces/UAP-KINERJA_ADSIS/Screenshoot/1 Mengubah Permission.png" >
</p>
<p align="center">Mengubah Permission catatannya-fauzan.txt ke view-only dengan perintah chmod 400</p>

**2. Lakukan konfigurasi alamat IP address sementara pada sistem dan default gateway. (petunjuk 192.168.56.x | x adalah nomor absen)**

**Screenshoot**

<p align="center">
  <img src="/workspaces/UAP-KINERJA_ADSIS/Screenshoot/2 Melihat IP.png" >
</p>
<p align="center">Melihat ip dengan perintah ifconfig</p>

<p align="center">
  <img src="/workspaces/UAP-KINERJA_ADSIS/Screenshoot/2 Mengubah IP.png" >
</p>
<p align="center">Mengubah IP dengan perintah sudo ifconfig ens33 192.168.56.11 netmask 255.255.255.0</p>

<p align="center">
  <img src="/workspaces/UAP-KINERJA_ADSIS/Screenshoot/2 Menambahkan default gateway.png" >
</p>
<p align="center">Menambahkan default gateway dengan perintah sudo route add default gw 192.168.56.110 ens33</p>

**3. Lakukan Instalasi Webmin lalu buatlah user bernama nama anda, lalu buat group Adsis_(kelas masing-masing) dan masukkan nama anda di group**

**Screenshoot**

<p align="center">
  <img src="/workspaces/UAP-KINERJA_ADSIS/Screenshoot/3 Install Webmin.png" >
</p>
<p align="center">Menginstall Webmin</p>

<p align="center">
  <img src="/workspaces/UAP-KINERJA_ADSIS/Screenshoot/3 Membuat group dan memasukkan user.png" >
</p>
<p align="center">Membuat groups baru dengan nama Adsis_E lalu masukkan user fauzan didalamnya</p>

<p align="center">
  <img src="/workspaces/UAP-KINERJA_ADSIS/Screenshoot/3 Cek groups dan user.png" >
</p>
<p align="center">Groups Adsis_E dengan id 1009 dengan user fauzan berhasil ditambahkan</p>

**4. akukan ping ke alamat ip anda dan coba lakukan reject dan drop di webmin, lalu analisis apa yang terjadi?**

**Screenshoot**

<p align="center">
  <img src="/workspaces/UAP-KINERJA_ADSIS/Screenshoot/4 Setting.jpg" >
</p>
<p align="center">Mengubah konfigurasi reject dan drop</p>

<p align="center">
  <img src="/workspaces/UAP-KINERJA_ADSIS/Screenshoot/4 Test ping.jpg" >
</p>
<p align="center">Menjalankan test ping</p>

**Penjelasan**

Dapat disimpulkan saat kita merubah setting ke reject saat di lakukan test ping maka yang terjadi adalah Destination port unreachable. sedangkan kalau kita drop maka tidak akan terjadi balasan sama sekali karena pengiriman pake telah sepenuhnya di tolak

**5. Buatlah perintah otomatis yang berfungsi untuk ping www.filkom.ub.ac.id**

**Screenshoot**

<p align="center">
  <img src="/workspaces/UAP-KINERJA_ADSIS/Screenshoot/5 Memasukkan perintah.png" >
</p>
<p align="center">Menambahkan perintah */3 * * * * ping filkom.ub.ac.id</p>

<p align="center">
  <img src="/workspaces/UAP-KINERJA_ADSIS/Screenshoot/5 Hasilnya.png" >
</p>
<p align="center">Hasil dari perintah */3 * * * * ping filkom.ub.ac.id</p>

**Penjelasan**

Sistem akan secara otomatis melakukan ping ke filkom.ub.ac.id setiap 3 menit sekali. Gambar yang disertakan menunjukkan bahwa ada selisih waktu 3 menit di antara setiap pengiriman ping yang ditunjukkan dalam keterangan waktu