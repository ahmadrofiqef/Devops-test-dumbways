2. Bagaimana cara kamu mencari sebuah file di sistem linux, tetapi kamu hanya mengetahui isi dari file tersebut? Praktikkan serta berikan screenshotnya! 

Jawaban : 

Langkah pertama saya membuat file bernama file1.txt di dalam folder bernama “baru” di direktori /etc/ seperti gambar dibawah

<img src="images/2.1.png">

Langkah selanjutnya adalah kita keluar dari direktori tersebut dengan perintah cd ..
Seperti dibawah

<img src="images/2.2.png">

Kemudian jalankan perintah sudo grep –Ril “Halo semua” /etc/ 

<img src="images/2.3.png">

Menggunakan keyword lain

<img src="images/2.4.png">

Dari gambar diatas dapat dilihat bahwa file yang mengandung keyword tadi bisa terlacak posisinya.
