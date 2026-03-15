# Networking Basic
Module ini menjelaskan tentang segala hal yg penulis alami dalam mengulik networking pada Ubuntu server. 

1. folder /etc
folder etc pada ubuntu adalah direktori pusat sistem yang menyimpan berbagai
berkas konfigurasi sistem-wide(berlaku untuk seluruh sistem), seperti pengaturan
jaringan, akun pengguna, konfigurasi layanan dan skrip startup. ini sering
disebut sebagai pusah konfigurasi sistm dimana perubahan d sini memengaruhi
perilaku aplikasi dan OS

Dalam Konfigurasi jaringan didalam folder etc ini terdapat 5 folder yang berkaitan dengan jaringan 
folder folder tersebut diantaranya adalah 
## Konfigurasi Jaringan di Ubuntu
1. Netplan 
	- Netplan 
	Folder netplan pada ubuntu terletak di /etc/netplan/, direktori ini 
	menyimpan file konfigurasi jaringan berbasis YAML yang digunakan oleh 
	networkd atau NetworkManager. perubahan konfigurasi diterapkan 
	menggunakan perintah 
	``` sudo netplan apply```

	netplan adalah utilitas konfigurasi jaringan open-source yang dikembangkan
	oleh Canonical untuk menyederhanakan pengaturan jaringan pada sistem
	operasi Linux, terutama mulai dari Ubuntu 18.04 LTS ke atas
	

2. Netconfig
	File netconfig diubuntu terletak didalam folder /etc/, file ini merupakan 
	sebuah database konfigurasi jaringan yang mendefinisikan daftar protokol
	transpor seperti TCP, UDP yang terseia di sistem

	Fungsi utama dari file ini adlaah digunakan oleh library RPC (remote 
	procedural call) untuk memilih protokol transpor yang akan digunakan
	saat aplikasi melakukan koneksi jaringan, isi file nya berisi kolom-kolom
	yang menjelaskan ID jaringan, semantik seperti connection-oriented 
	atau connectionlss, protokol dan pustaka pemetaan alamat terkait.

	File ini tidak digunakan untuk mengatur alamat IP statis, gateway 
	atau Wifi. pengaturan tersebut tetap dilakukan melalui Netplan
3. Network
	Dalam sistem Ubuntu, folder /etc/network adalah lokasi penyimpanan
	konfigurasi jaringan yang digunakan oleh metode ifupdown (sistem 	
	manajemen jaringan tradisional Debian) mesikpun Ubuntu modern sudah 
	beralih ke Netplan, folder ini tetap ada di sistem karena alasan 
	kompatibilitas atau jika anda sengaja menginstall paket ifupdown

	di dalam /etc/network/ anda akan menemukan beberapa folder yang 
	menjalankan skrip secara otomatis berdasarkan status koneksi
	- if-pre-up.d/ : skrip yang jalan sebelum interface menyala
	- if-up.d/: skrip yang jalan setelah inteface aktif
	- if-down.d/ : skrip yang jalan setelah interface dimatikan
	- if-post-down.d/: skrip yang jalan setelah interface benar-benar berhenti

	Folder ini biasany digunakan untuk mengatur jaringna pada ubuntu server
	lama. ubuntu moder biasanya berisi folder kosong atau hanya berisi 
	konfigurasi loopback lo, karena pengaturan utama sudah pindah ke 
	/etc/netplan
4. Network-dispatcher
	network-dispatcher atau NetworkManager-Dispatcher adalah sebuah layanan
	atau daemon yang bertugas untuk menjalankan skrip tertentu secara 
	otomatis ketika terjadi perubahan status pada koneksi jaringan anda
	
	Layanan ini sangat berguna unutk melakukan otomatisasi tugas-tugas 
	pasca koneksi seperti:
	- menjalankan VPN secara otomatis sesaat setelah terhubung internet
	- mengubah aturan firewall berdasarkan jaringan mana yang sedang digunakan 
	- me-mount drive jaringan hanya saat masuk ke wifi kantor
	- mengirim notifikasi ke sistem atau email saat koneksi server terputus
	
	Folder ini penting karna neplan tidak lagi mendukung fitur hooks scripts
	seperti pre-up atau post-up langsung didalam file konfigurasinya, maka
	Network Dispatcher menjadi cara standar untuk menjalankan skrip otomatis
	tersbut di versi Ubuntu Modern

5. Networks

	Dalam sistem Ubuntu modern, folder /etc/network berfungsi sebagai pusat
	kendali skrip otomatis untuk antarmuka jaringan anda. meskipun pengaturan
	alamat IP sekarang sudah pindah ke Netplan, folder ini tetap penting
	karenan berisi pemicu untuk menjalankan perintah tertentu saat status 
	internet berubah
	1. Eksekusi Skrip otomatis: folder ini berisi sub-direktori yang 
	   menjalankan skrip berdasarkan kondisi kartu jaringan
	  - if-up.d/: menjalankan perintah segera setelah internet tersambung 
	  - if-down.d/: menjalankan perintah saat internet terputus
	  - if-pre-up.d/ & if-post-down.d/: untuk tugas persiapan sebelum menyala atau pembersihan setelah
	    benar benar mati
	2. Tempat File interface tradisional: didalamnya terdapat file bernama interfaces
	    Dulu ini adlaah tempat utama untuk menulis IP statis atau DHCP. di Ubuntu
	    versi terbaru, file ini biasanya hanya berisi konfigurasi loopback 
	    karena tugas utamanya sudah digantikan netplan 
	3. Manajemen interface virtual: Digunakan untuk mengatur konfigurasi tingkat lanjut
	    seperti bridge atau VLAN jika anda tidak menggunakan NetworkManager
	Singkatnya jika netplan adalah tempat mendaftar alamat IP maka folder 
	networks adalah tempat menaruh skrip yang harus jalan otomatis saat koneksi
	itu nyalah atau mati
 
Berikut tadi sudah kita ulas tentang 5 items didalam direktori etc yang berkaitan dengan internet. silahkan ditunggu 
part selanjutnya 
