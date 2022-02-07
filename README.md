# HTTPS
<p>Hypertext Transfer Protocol Secure adalah ekstensi dari Hypertext Transfer Protocol. Ini digunakan untuk komunikasi aman melalui jaringan komputer, dan banyak digunakan di Internet. Dalam HTTPS, protokol komunikasi dienkripsi menggunakan Transport Layer Security atau, sebelumnya, Secure Sockets Layer.</p>
<h2>Cara mengaktifkan HTTPS di Apache</h2>
<p><code>apt-get update</code>
<p>Instal server Apache dan paket yang diperlukan.</p>
<p><code>apt-get install apache2 openssl</code></p>
<p>Aktifkan modul Apache bernama: Mod_ssl.</p>
<p><code>a2enmod ssl</code></p>
<p>Aktifkan modul Apache bernama: Mod_rewrite.</p>
<p><code>a2enmod rewrite</code><p>
<p>Edit file konfigurasi Apache.</p>
<p><code>nano /etc/apache2/apache2.conf</code><p>
<p>Tambahkan baris <a href="https://github.com/rofisikunyuk/HTTPS/blob/main/File%20konfigurasi%20apache.txt">berikut</a> di akhir file ini.</p>
