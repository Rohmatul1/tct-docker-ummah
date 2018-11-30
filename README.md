# Penggunaan Docker

Deploying your First Docker Container :

Step 1 - Running A Container 

Langkah pertama yang dilakukan yaitu menjalankan perintah running a container dengan menggunakan perintah  docker search redis seperti gambar di bawah. 

*Redis docker* images disebut dengan redis dan ingin menjalankan the *lates* release. Karena redis adalah database.
Kemudian docker akan menjalankan command di latar depan. untuk menjalankannya menggunakan perintah seperti dibawah.

Step 2 - Finding Running Containers 
Langkah kedua yaitu menggunakan perintah docker ps yang berfungsi untuk menjalankan container di latar belakang/background. Sehingga semua container yang dijalankan, gambar digunakan untuk dimulai di container dan dalam kondisi aktif. Setelah menggunakan perintah tersebut maka, hasilnya akan seperti gambar di bawah.

Step 3 - Accessing Redis 
Jika menemukan ada permasalahan saat menjalankan redis maka solusi terbaik yaitu dengan menggunakan perintah docker run -d --name redisHostPort -p 6379:6379 redis:latest dan hasilnya sebagai berikut :

Step 4 - Accessing Redis
Setelah itu, gunakan perintah docker run -d --name redisDynamic -p 6379 redis:latest. Setelah dijalankan maka, akan menemui hasil sebagai berikut :
Namun, hasil tak sesuai harapan maka lanjutkan dengan perintah docker port redisDynamic 6379 seperti di bawah ini dan hasilnya akan keluar *Thankfully*.
Step 5 - Persisting Data 
Langkah selanjutnya menggunakan perintah docker run -d --name redisMapped -v /opt/docker/data/redis:/data redis dan hasilnya sebagai berikut :

Step 6 - Running A Container In The Foreground 


Deploy Static HTML Website as Container :

Step 1 - Create Dockerfile
Step 2 - Build Docker Image
Step 3 - Run

Building Container Images :

Step 1 - Base Images
Step 2 - Running Commands
Step 3 - Exposing Ports
Step 4 - Default Commands
Step 5 - Building Containers
Step 6 - Launching New Image