# HTTPS
<p>Hypertext Transfer Protocol Secure (HTTPS) adalah ekstensi dari Hypertext Transfer Protocol. Ini digunakan untuk komunikasi aman melalui jaringan komputer, dan banyak digunakan di Internet. Dalam HTTPS, protokol komunikasi dienkripsi menggunakan Transport Layer Security atau, sebelumnya, Secure Sockets Layer.</p>
<h2>Cara mengaktifkan HTTPS di Apache</h2>
<p>1. Update Debian</p>
<p><Li><code>apt-get update</code></li></p>
<p>2. Instal server Apache dan paket yang diperlukan.</p>
<p><Li><code>apt-get install apache2 openssl</code></Li></p>
<p>3. Aktifkan modul Apache bernama: Mod_ssl.</p>
<p><Li><code>a2enmod ssl</code></Li></p>
<p>4. Aktifkan modul Apache bernama: Mod_rewrite.</p>
<p><Li><code>a2enmod rewrite</code></Li><p>
<p>5. Edit file konfigurasi Apache.</p>
<p><Li><code>nano /etc/apache2/apache2.conf</code></Li><p>
<p>Tambahkan baris <a href="https://github.com/rofisikunyuk/HTTPS/blob/main/File%20konfigurasi%20apache.txt">berikut</a> di akhir file ini.</p>
<img src="https://github.com/rofisikunyuk/HTTPS/blob/main/Screenshot/file%20konfigurasi%20apache.png" width="250" height="150">
<p>6. Buat kunci pribadi dan sertifikat situs web menggunakan perintah OpenSSL.</p>
<p><Li><code>mkdir /etc/apache2/certificate</code></Li></p>
<p><Li><code>cd /etc/apache2/certificate</code></Li><p>
<p><Li><code>openssl req -new -newkey rsa:4096 -x509 -sha256 -days 365 -nodes -out apache-certificate.crt -keyout apache.key</code></li></p>
<p>Masukkan informasi yang diminta.</p>
<p>Pada opsi bernama COMMON_NAME, Anda harus memasukkan alamat IP atau nama host.</p>
<p>7. Edit file konfigurasi Apache untuk situs web default.</p>
<p><Li><code>nano /etc/apache2/sites-enabled/000-default.conf</code></Li></p>
<p>Secara opsional, Anda mungkin ingin mengarahkan pengguna HTTP ke versi HTTPS situs web Anda. Dalam hal ini, gunakan konfigurasi <a href="https://github.com/rofisikunyuk/HTTPS/blob/main/HTTP%20to%20HTTPS">berikut</a>.</p>
<img src="https://github.com/rofisikunyuk/HTTPS/blob/main/Screenshot/http%20to%20https.png" width="250" height="150">
<p>8. Mulai ulang layanan Apache.</p>
<p><Li><code>systemctl restart apache2</code></Li></p>
<p>9. Buka browser ketikan https://ip host.</p>
<img src="https://github.com/rofisikunyuk/HTTPS/blob/main/Screenshot/client.png" width="250" height="150"><hr>
<p>"Kalau gambarnya kurang jelas di zoom aja ya broo"</p>
