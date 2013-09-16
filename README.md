HTTPServer
==========

Tutorial cara pasang & penggunaan libevent
------------------------------------------

+ Download & extract libevent dari link : https://github.com/downloads/libevent/libevent/libevent-2.0.21-stable.tar.gz
+ Set suatu environment variable baru di UNIX, caranya adalah dengan buka .bashrc di home folder, ketik :

> export C_INCLUDE_PATH={Path menuju folder include di dalam libevent hasil extract}

+ Kalau belum menjadi root user, gunakan perintah su di terminal
+ Masuklah ke folder tempat libevent diextract, kemudian ketikkan 3 kode berikut ini (dari terminal):

> ./configure --prefix=/usr --disable-static <br/>
> make <br/>
> make install <br/>

+ Ketika kompilasi, kita harus menggunakan flag -levent pada linker. Sebagai contoh, untuk mengcompile suatu file hello.c, caranya adalah : 

> gcc hello.c -levent 

+ Sekarang seharusnya libevent sudah bisa diinclude dengan mudah :)
