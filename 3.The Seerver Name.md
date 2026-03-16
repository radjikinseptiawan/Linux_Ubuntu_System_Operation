Server name adalah label unik yang diberikan kepada sebuah perangkat dalam suatu jaringan jika diibaratkan IP address adalah nomor KTP 
sedangkan server nam adalah nama panggilan orang tersebut agar mudah diingat

# Server Name pada level sistem
Ini adalah identitas komputer anda didalam jaringan lokal. saat anda membuka terminal di Ubuntu, nama yang muncul setelah tanda @ adalah Server Name/Hostname
sistem anda.

# Server Name pada Web Server
Jika anda menggunakan web server sepertin Nginx atau Apache, server_name adalah direktif yang menentukan domain mana yang akan dilayani oleh blok konfigurasi
tersebut. satu server dengan satu IP bisa menampung banyak Website. Web Server menggunakan Server Name yang dikirim oleh browser untuk menentukan website
mana yang harus ditampilkan
```
	server{
		listen 80;
		server_name www.bisnis-saya.com;
		root /var/www/bisnisl
	}
```

# Server Name dalam Local DNS Mapping
Dalam file ``` /etc/hosts/ ```. Server name adalah alias yang anda buat untk sebuah IP
misalnya anda punya server database dengan 10.0.0.5 daripada menghapal IP nya anda memilih untuk 
memberinya server name 

```bash 
	10.0.0.5 db-produksi
```
