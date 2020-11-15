8. Buatlah sebuah server sederhana menggunakan web server di komputer kamu, kemudian setting web server tersebut menjadi domain dumbways-namakamu.xyz!  
Dilarang menggunakan XAMPP, IIS, Laragon, AMPPS dan aplikasi sejenisnya . Sertakan screenshot step by step-nya atau record menjadi sebuah video

Jawaban : 

a. Pertama-tama kita menginstall apache2 Web Server terlebih dahulu di WSL(Windows Subsystem Linux) Ubuntu 18.0.4 LTS, 
dengan perintah sudo apt install apache2 seperti dibawah

<img src="images/8.1.png">

b. Jika apache web server sudah terinstall kita bisa mengecek apakah web server tersebut sudah online atau tidak, 
kita dapat menggunakan systemctl status apache2, disini saya menggunakan perintah ip a untuk mengecek ip address atau localhost dari PC. 
Dari gambar dibawah dapat dilihat bahwa 192.168.4.204 merupakan ip addresnya.

<img src="images/8.2.png">

c. Disini saya mencoba cek apakah apache sudah terinstall tanpa masalah dengan cara memasukkan ip address kita ke web browser, 
jika berhasil maka tampilannya akan seperti gambar dibawah ini.

<img src="images/8.3.png">

d. Jika sudah, selanjutnya ubah index.html dengan cara sudo nano index.html

<img src="images/8.4.png">

e. Lalu disini saya coba mengubah menjadi tampilan html seperti dibawah.

<img src="images/8.5.png">

f. Hingga hasilnya menjadi seperti ini. 

<img src="images/8.6.png">

g. Langkah selanjutnya yang saya lakukan adalah mengkonfigurasi server dengan cara menginstall bind9 terlebih dahulu seperti dibawah.

<img src="images/8.7.png">

h. Jika bind9 sudah berhasil terinstall, langkah selanjutnya kita masuk folder /etc/bind dengan cara CD /etc/bind lalu sudo nano named.conf.options 
disini kita akan memasukkan ip address server kita yaitu 192.168.4.204

<img src="images/8.8.png">

i. Setelah itu save & exit, selanjutnya lakukan perintah yang sama pada file named.conf.local dengan cara sudo nano named.conf.local seperti dibawah 
dan tambahkan perintah seperti dibawah. Perlu diperhatikan di zone kedua adalah nama ip address kita tetapi posisinya dibalik dan yang diambil hanya 3 oktet ip address awal,
misal 192.168.4.204 akan terbalik menjadi 4.168.192 tanpa menyisipkan oktet terakhir yaitu 204.

<img src="images/8.9.png">

j. Jika sudah selanjutnya adalah kita masuk ke dalam file db.domain dan juga db.ip seperti dibawah

<img src="images/8.10.png">

k. Di file db.domain ini kita isi DNS dan ip address kita seperti diatas

<img src="images/8.11.png">

l. Selanjutnya di file db.id kita juga perlu mengubah DNS seperti diatas dan juga kita harus menambahkan ip address oktet ke 4 yaitu 204. 
Jika langkah semua sudah dilakukan selanjutnya kita masuk ke /etc/resolv/conf untuk menambahkan DNS dan IP server seperti dibawah.

<img src="images/8.12.png">

m. Jika semua langkah diatas telah dilakukan, kita restart apache dengan service apache2 restart perintah atau sudo /etc/init.d/apache2 restart

<img src="images/8.13.png">

n. Selanjutnya kita coba ping ke DNS dumbways-achmadrofiqelfakih.xyz dan juga menggunakan perintah nslookup untuk mengetahui ip dari domain tersebut, 
Hasilnya seperti dibawah.

<img src="images/8.14.png">
