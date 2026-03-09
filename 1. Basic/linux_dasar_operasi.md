# Operasi Dasar Penggunaan Linux

## Create, Read, Update, Delete File dan Folder di Linux
1. Cara membuat file 
	- Membuat file saja 
	``` touch <nama_file>```
	- Membuat dan mengedit file tersebut 
	``` nano <nama_file> ```
	- Membuat file sekaligus mengisi isi file tersebut
	``` echo <nama_file> ```
	- Membuat file dan melihat isinya tanpa mengedit file tersebut
	``` cat <nama_file> ```
2. Cara pindah direktori
	``` cd ./<direktori_dituju>/<dir2>/<dir3>```
3. Cara Scroll up dan scroll down di terminal 
	``` ctrl+pageUp``` atau ```ctrl+pageDown```
4. Cara melihat isi dari direktori
 	- Umum
	``` ls```
	- Melihat isi Folder Detail
	``` ls -l``` atau ```ls -la```
5. Cara melihat isi File
	- Melihat file dan mengeditnya
	``` nano <nama_file>```
	- melihat file panjang
	``` less <nama_file> ```
	- Hanya melihat file
	``` cat <nama_file> ```
	- Melihat Beberapa Baris Pertama file
	``` head <nama_file>```
	- Melihat beberapa baris terakhir file
	``` tail <nama_file>```
6. Memindahkan Direktori dan File
	- Memindahkan file ke folder
	``` mv <nama_file> <direktori_nama_folder>/```
	- Memindahkan file ke direktori lain
	``` mv <nama_file> /home/radjikin/public```
	- Mengganti nama file
	``` mv <nama_file_lama> <nama_file_baru>``` 
	- Memindahkan folder 
	``` mv <folder1> <folder2>```
	- Mengganti nama folder
	``` mv <nama_folder_lama> <nama_folder_baru>```
7. Melihat lokasi direktori 
	``` pwd```
8. Membersihkan log terminal
	``` clear``` atau ```bash ctrl+ L```
9. Menyalin Folder atau file 
	``` cp folder1 folder2``` atau ```cp file1.txt folder/```
10. Menjalankan perintah dengan hak administrator
	- ``` sudo apt update``` = refresh daftar paket terbaru
	- ``` sudo apt upgrade``` = update semua paket yang terinstall
	- ``` sudo apt install``` = menginstall software
	- ``` sudo apt remove``` = menghapus software
11. ubah permission file/folder
	- ```chmod```
	tipe tipe chamod 
		- u = user = pemilik file
		- g = group = group pemilik file
		- o = others = semua orang lain
12. ubah pemilik folder atau file
	- ```sudo chown radjikin:radjikin file.txt``` = file txt sekarang menjadi miliki radjikin dan grup radjikin```

