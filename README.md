# JAWABAN UTS

## DESKRIPSI
* Nama	 : Robby Hermando Remen
* Nim	 : 195610118
* Matkul : Cloud Computing
* Sks	 : 2

## PENJELASAN
### <b>1. Buat Account Docker Hub</b>
* Login Dari website
![img](/acc1.PNG)
<br>
<br>
* Login Dari Aplikasi<br>
![img](/acc2.PNG)
<br>
<br>
### <b>2. Pilih Image Docker, Pull, dan Run</b>
* Docker yang dipilih 
https://hub.docker.com/_/nextcloud
<br>(Jenis image : Application Frameworks)
<br>
<br>
* Pull Image
<br>> docker pull nextcloud
![img](/imgpull1.PNG)
<br>
<br>
* Image to Container
<br>> docker run -d -p 8080:80 nextcloud
![img](/imgpull2.PNG)
<br>
<br>
* Run Container
<br>> http://localhost:8080/
![img](/imgpull3.PNG)
<br>
<br>
* Stop Container
<br>> docker container ls
<br>(melihat list container yg ada)
![img](/imgpull5.PNG)
<br>
<br>> docker stop competent_merkle
<br>("competent_merkle" adalah nama dari image container jika image tidak di beri nama saat membuat "--name [NAME]" maka akan otomatis dibuat)
![img](/imgpull4.PNG)
<br>
<br>(Saat container di stop atau hapus, maka webserver akan mati)
![img](/imgpull6.PNG)
<br>
<br>
### <b>3. Buat Dockerfile untuk Docker Image</b>
* Membuat folder "docker-195610118"
![img](/push1.PNG)

* Membuat file "Dockerfile" didalam folder
![img](/push2.PNG)

* Isi dari file Dockerfile
![img](/push3.PNG)

* buat folder "html"
![img](/push4.PNG)

* isi folder html <br>
![img](/push5.PNG)

* isi file dari index.html (disesuaikan selera)
![img](/push6.PNG)

* isi file dari style.css (disesuaikan selera)
![img](/push7.PNG)

* Melakukan build dengan image "utsrobbyhermando" dan tag "195610118"
<br>> docker build -t utsrobbyhermando:195610118 .
![img](/push8.PNG)

* Melihat apakah image yg kita buat berhasil masuk atau tidak
<br>> docker image ls
![img](/push9.PNG)

* Lakukan run container pada image yang di buat dengan port 80
<br>> docker run -d -p 80:80 utsrobbyhermando:195610118
![img](/push10.PNG)

* Selanjutnya tes apakah container berjalan atau tidak
<br>> docker ps
![img](/push12.PNG)

* Tes hasil dari container menggunakan localhost CLI
<br>> curl -XGET localhost
![img](/push13.PNG)

* Tes hasil container menggunakan localhost browser
<br>> localhost:80
![img](/push11.PNG)

* Selanjutnya push image yang kita buat ke repository Docker
<br>> docker tag utsrobbyhermando:195610118 robbyhermando/utsrobbyhermando
<br>> docker push robbyhermando/utsrobbyhermando:195610118
![img](/push15.PNG)

* Cek Repository
![img](/push14.PNG)

* Hasil Repository "Public view" <br>
https://hub.docker.com/r/robbyhermando/utsrobbyhermando

* SELESAI, TERMAKASIH BAPAK BAMBANG TERCINTA