# Penggunaan Docker

Docker adalah salah satu platform yang dibangun berdasarkan teknologi container. Docker merupakan sebuah project 
open-source yang menyediakan platform terbuka untuk developer maupun sysadmin untuk dapat membangun, mengemas, dan 
menjalankan aplikasi dimanapun sebagai sebuah wadah (container) yang ringan. Dengan sangat populernya docker, sebagian 
orang sering menganggap docker adalah sebutan lain untuk container.

# Deploying your First Docker Container :
* Step 1 - Running A Container 

Langkah pertama yang dilakukan yaitu menjalankan perintah running a container dengan menggunakan perintah docker search redis seperti gambar di bawah. 
![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/1.png)
 
*Hasil dari perintah docker search redis adalah*
![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/2.png)
![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/3.png)
![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/4.png)

*Redis docker* images disebut dengan redis dan ingin menjalankan the *lates* release. Karena redis adalah database.
Kemudian docker akan menjalankan command di latar depan. untuk menjalankannya menggunakan perintah seperti dibawah.
![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/5.png)

*hasilnya :*

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/6.png)

* Step 2 - Finding Running Containers 

Langkah kedua yaitu menggunakan perintah docker ps yang berfungsi untuk menjalankan container di latar belakang/background. 
Sehingga semua container yang dijalankan, gambar digunakan untuk dimulai di container dan dalam kondisi aktif. Setelah menggunakan 
perintah tersebut maka, hasilnya akan seperti gambar di bawah.

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/7.png)

*hasilnya :*
![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/8.png)

* Step 3 - Accessing Redis 

Jika menemukan ada permasalahan saat menjalankan redis maka solusi terbaik yaitu dengan menggunakan perintah docker run -d --name 
redisHostPort -p 6379:6379 redis:latest dan hasilnya sebagai berikut :
![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/9.png)

*hasilnya :*

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/10.png)

* Step 4 - Accessing Redis

Setelah itu, gunakan perintah docker run -d --name redisDynamic -p 6379 redis:latest. Setelah dijalankan maka, akan menemui hasil sebagai berikut :
Namun, hasil tak sesuai harapan maka lanjutkan dengan perintah docker port redisDynamic 6379 seperti di bawah ini.

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/11.png)

*hasilnya :*

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/12.png)

Setelah itu, lakukan seperti gambar di bawah ini

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/13.png)

*hasilnya :*

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/14.png)

Setelah itu, lakukan seperti gambar di bawah ini

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/15.png)

*hasilnya :*
![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/16.png)

* Step 5 - Persisting Data 

Langkah selanjutnya menggunakan perintah docker run -d --name redisMapped -v /opt/docker/data/redis:/data redis :
Setelah itu, lakukan seperti gambar di bawah ini

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/17.png)

*hasilnya :*

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/18.png)

* Step 6 - Running A Container In The Foreground 
Setelah itu, lakukan seperti gambar di bawah ini

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/19.png)

*hasilnya :*

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/20.png)

Setelah itu, lakukan seperti gambar di bawah ini
![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/21.png)

*hasilnya :*
![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/22.png)

Setelah semua langkah dikerjakan maka, klik summary maka akan keluar hasil :

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/1/23.png)


# Deploy Static HTML Website as Container :

* Step 1 - Create Dockerfile
Langkah pertama yang dilakukan adalah copy paste soure code yang nantinya akan tampil pada sebelah kanan
ketika diklik copiest. Hasilnya seperti di bawah :
![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/2/1.png)

* Step 2 - Build Docker Image
Kemudian untuk membuat static html gambar maka menggunakan command  dan perintah berikut :

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/2/2.png)

*hasilnya*

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/2/3.png)

Selanjutnya kamu dapat melihat gambarnya melalui perintah berikut:

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/2/4.png)

*hasilnya*

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/2/5.png)

* Step 3 - Run

Berikut langkah selanjutnya :

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/2/6.png)

*hasilnya*
![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/2/7.png)

Untuk memulainya maka, dapat menggunakan akses dengan port 80, berikut langkahnya :

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/2/8.png)

*hasilnya*

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/2/9.png)

Setelah semua langkah dikerjakan maka, klik summary maka akan keluar hasil :
![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/2/10.png)

# Building Container Images :

* Step 1 - Base Images

Berikut langkah selanjutnya yaitu di copas :

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/3/14.png)

* Step 2 - Running Commands

Berikut langkah selanjutnya yaitu di copas :

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/3/15.png)

* Step 3 - Exposing Ports

Berikut langkah selanjutnya yaitu di copas :

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/3/16.png)

* Step 4 - Default Commands

Berikut langkah selanjutnya yaitu di copas :

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/3/17.png)

* Step 5 - Building Containers

Berikut langkah selanjutnya :

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/3/1.png)

*hasilnya*

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/3/2.png)

Berikut langkah selanjutnya :

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/3/3.png)

*hasilnya*

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/3/4.png)
![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/3/5.png)

* Step 6 - Launching New Image

Berikut langkah selanjutnya :

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/3/6.png)

*hasilnya*

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/3/7.png)

Berikut langkah selanjutnya :

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/3/8.png)

*hasilnya*

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/3/9.png)

Berikut langkah selanjutnya :

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/3/10.png)

*hasilnya*

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/3/11.png)

Setelah semua langkah dikerjakan maka, klik summary maka akan keluar hasil :

![On Demand](https://github.com/Rohmatul1/tct-docker-ummah/blob/master/3/12.png)
