Didalam folder netplan terdapat file berekstensi .yaml 
Netplan memiliki konfigurasi default seperti ini

``` network:
     version:2
       renderer: networkd
        ethernets:
         enp0s3:
 	  dhcp:true```

# Penjelasan & Konfigurasi IP Dinamis
| Bagian    |              Fungsi            |
| network   | root konfigurasi jaringan      |
| version   | versi format netplan           |
| renderer  | sistem yang mengelola jaringan |
| ethernets | interface jaringan kabel       |
| enp0s3    | nama interface                 |
| dhcp4:true| ambil IP dari DHCP             |

Kalau kamu ingin Ubuntu mendapatkan ip secara otomatis dari router/hotspot maka
biarkan setinggan default setelahnya jalankan command 

``` sudo netplan apply```
lalu cek 
``` ip a```
jika terdapat tulisan inet maka sistem telah berhasil di setting otomatis dari router/hotspot


# Penjelasan & Konfigurasi IP Statis
```
 network:
   version: 2
    ethernets:
      enp0s3:
        dhcp4: false
        addresses: 10.69.180.92/24
         routes:
         - to: default 
           via: 10.69.180.1
          nameservers:
           addresses:
           - 8.8.8.8
           - 1.1.1.1```
|  Bagian     |   Fungsi  |
| addresses   | IP Statis |
|  routes     | Gateway   |
| nameservers |  DNS      |

