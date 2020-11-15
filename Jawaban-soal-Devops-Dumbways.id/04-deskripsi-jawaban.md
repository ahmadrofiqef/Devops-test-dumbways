4.Jelaskan perbedaan mencolok antara Docker dengan VMware, serta berikan penjelasan kapan kita harus menggunakan Docker dan VMware?

Jawaban :

Docker adalah OS virtual yang performanya tergantung pada hardware fisik, jika PC/laptop kita mempunyai spesifikasi yang tinggi maka performa untuk menjalankan docker akan 
sangat baik sedangkan VMWare merupakan virtual machine/emulator dimana kita membagikan resource hardware seperti ram & cpu yang kita punya menjadi beberapa system computer, 
perbedaan lainnya yaitu docker tidak memerlukan system operasi secara penuh karena docker hanya bergantung pada kernel Linux OS (yang mana hampir semua kernel linux 
menggunakan kernel standard) sedangkan VMware menggunakan OS secara keseluruhan.

Kita dapat menggunakan VMware jika kita ingin membuat system yang terisolasi dan tidak akan merusak system utama yang kita miliki, dan menggunakan VMware terpaut lebih aman.
Sedangkan kita dapat menggunakan docker untuk software development yang memungkinkan kita dapat membuat, menguji dan menerapkan aplikasi dengan cepat. 
