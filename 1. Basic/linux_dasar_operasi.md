# Operasi Dasar Penggunaan Linux

## Create, Read, Update, Delete File dan Folder di Linux
1. Cara membuat file 
	- Membuat file saja 
	```bash touch <nama_file>```
	- Membuat dan mengedit file tersebut 
	```bash nano <nama_file> ```
	- Membuat file sekaligus mengisi isi file tersebut
	```bash echo <nama_file> ```
	- Membuat file dan melihat isinya tanpa mengedit file tersebut
	```bash cat <nama_file> ```
2. Cara pindah direktori
	```bash cd ./<direktori_dituju>/<dir2>/<dir3>```
3. Cara Scroll up dan scroll down di terminal 
	```bash  ctrl+pageUp``` atau ```bash ctrl+pageDown```
4. Cara melihat isi dari direktori
 	- Umum
	```bash ls```
	- Melihat isi Folder Detail
	```bash ls -l``` atau ```bash ls -la```
5. Cara melihat isi File
	- Melihat file dan mengeditnya
	```bash nano <nama_file>```
	- melihat file panjang
	```bash less <nama_file> ```
	- Hanya melihat file
	```bash cat <nama_file> ```
	- Melihat Beberapa Baris Pertama file
	```bash head <nama_file>```
	- Melihat beberapa baris terakhir file
	```bash tail <nama_file>```
6. Memindahkan Direktori dan File
	- Memindahkan file ke folder
	```bash mv <nama_file> <direktori_nama_folder>/```
	- Memindahkan file ke direktori lain
	```bash mv <nama_file> /home/radjikin/public```
	- Mengganti nama file
	```bash mv <nama_file_lama> <nama_file_baru>``` 
	- Memindahkan folder 
	```bash mv <folder1> <folder2>```
	- Mengganti nama folder
	```bash mv <nama_folder_lama> <nama_folder_baru>```
7. Melihat lokasi direktori 
	```bash pwd```
8. Membersihkan log terminal
	```bash clear``` atau ```bash ctrl+ L```
9. Menyalin Folder atau file 
	```bash cp folder1 folder2``` atau ```bash cp file1.txt folder/```
10.Menjalankan perintah dengan hak administrator
	- ```bash sudo apt update``` = refresh daftar paket terbaru
	- ```bash sudo apt upgrade``` = update semua paket yang terinstall
	- ```bash sudo apt install``` = menginstall software
	- ```bash sudo apt remove``` = menghapus software
11. ubah permission file/folder
	- ```bash chmod```
	tipe tipe chamod 
		- u = user = pemilik file
		- g = group = group pemilik file
		- o = others = semua orang lain
12. ubah pemilik folder atau file
	- ```bash sudo chown radjikin:radjikin file.txt``` = file txt sekarang menjadi miliki radjikin dan grup radjikin```
