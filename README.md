# latihan1
# Apa itu VCS
* VCS atau Version Control System merupakan sebuah sistem yang merekam perubahan-perubahan dari sebuah berkas atau sekumpulan berkas dari waktu ke waktu sehingga Anda dapat melihat kembali setiap perubahannya. 
* Salah satu DVCS (Distributed Version Control System) yang sangat populer saat ini adalah **git.** 

# Apa itu Git?
* Git adalah salah satu sistem pengontrol versi (Version Control System) pada proyek perangkat lunak yang diciptakan oleh Linus Torvalds. 
* Pengontrol versi bertugas mencatat setiap perubahan pada file proyek yang dikerjakan oleh banyak orang maupun sendiri. 
* Git dikenal juga dengan distributed revision control (VCS terdistribusi), artinya penyimpanan database Git tidak hanya berada dalam satu tempat saja.

# Instalasi Git
* Download Git, buka website resminya Git [git-scm.com](https://git-scm.com) 
* Kemudian unduh Git sesuai dengan arsitektur komputer kita. Kalau menggunakan 64bit, unduh yang 64bit. Begitu juga kalau menggunakan 32bit. 
* Selamat, Git sudah terinstal di Windows. Untuk mencobanya, silahkan buka CMD atau PowerShell, kemudian ketik perintah 
git --version.

![IQBAL 1](https://user-images.githubusercontent.com/57259403/68079192-57f73600-fe18-11e9-85b5-431fe38e67a9.png)




# Menambahkan Global Config
* Pada saat pertama kali menggunakan git, perlu dilakukan konfigurasi user.name dan user.email 
 konfigurasi ini bisa dilakukan untuk global repostiry atau individual repository. 
* apabila belum dilakukan konfigurasi, akan mengakibatkan terjadi kegagalan saat menjalankan perintah git commit

``$ Config Global Repository $ git config --global user.name “nama_user”``
``$git config --global user.email “nama_user”``

# Perintah Dasar Git

* git init, perintah untuk membuat repository local 
* git add, perintah untuk menambahkan file baru, atau perubahan pada file pada staging sebelum proses commit. 
* git commit, perintah untuk menyimpan perubahan kedalam database git. 
* git push -u origin master, perintah untuk mengirim perubahan pada repository local menuju server repository. 
* git clone [url], perintah untuk membuat working directory yang diambil dari repositry sever. 
* git remote add origin [url], perintah untuk menambahkan remote server/reopsitory server pada local repositry (working directory) 
* git pull, perintah untuk mengambil/mendownload perubahan terbaru dari server repository ke local repository 

# Membuat Reposiory Local
* Buka direktory aktif, misal: d:\labs_pemrograman1 (buka menggunakan Windows Explorer) 
* klik kanan pada direktory aktif tersebut, dan pilih menu Git Bash, sehingga muncul git bash commad 
* Buat direktory project praktikum pertama dengan nama **latihan1**

``$ mkdir latihan1``
``$ cd latihan1``
* Sehingga terbentuk satu direktori baru dibawahnya, selanjutnya masuk kedalam direktori tersebut dengan perintah cd (change directory) * direktory aktif menjadi: d:\labs_pemrograman1\latihan1

# Membuat Reposiory Local
* Jalankan perintah git init, untuk membuat repository local.
* Repository baru berhasil di inisialisasi, dengan terbentuknya satu direktori hidden dengan nama .git
* Pada direktori tersebut, semua perubahan pada working directory akan disimpan. $ git init

# Menambahkan File baru pada repository
* Untuk membuat file dapat menggunakan text editor, lalu menyimpan filenya pada direktori aktif (repository) 
* disini kita akan coba buat satu file bernama README.md (text file)
* File README.md berhasil dibuat. ``$ echo “#Latihan 1” >> README.md``

![iqbal 3](https://user-images.githubusercontent.com/57259403/68079903-06ed3f00-fe24-11e9-93d4-807f528cc9ed.png)


# Menambahkan File baru pada repository
* Untuk menambahkan file yang baru saja dibuat tersebut gunakan perintah git add.
* File README.md berhasil ditambahkan. ``$ git add README.md``

![iqbal 4](https://user-images.githubusercontent.com/57259403/68079918-4caa0780-fe24-11e9-859e-21026256a951.png)

# Commit (Menyimpan perubahan ke database)
* Untuk menyimpan perubahan yang ada kedalam database repository local, gunakan perintah ``git commit -m “komentar commit”``
``$ git commit -m “File pertama saya”``
* Perubahan berhasil disimpan.

![iqbal 10](https://user-images.githubusercontent.com/57259403/68080016-db6b5400-fe25-11e9-9335-359341332edb.png)



# Membuat repository server
* Server reopsitory yang akan kita gunakan adalah http://github.com 
* Anda harus membuat akun terlebih dahulu. 
* Pada laman github, klik tombol start a project, atau 
* Dari menu (icon +) klik New Repository

![iqbal 66](https://user-images.githubusercontent.com/57259403/68079652-6f85ed00-fe1f-11e9-92e2-2d75609a31dc.png)

# Membuat repository server
* Isi nama repositorynya, misal: **labpy1.** 
* lalu klik tombol **Create repository**

![IQBAL 11](https://user-images.githubusercontent.com/57259403/68080139-8d575000-fe27-11e9-8587-04582bf60ae3.png)


# Menambahkan Remote Repository
* Remote Repository merupakan repository server yang akan digunakan untuk menyimpan setiap perubahan pada local repository, sehingga dapat diakses oleh banyak user. 
* Untuk menambahkan remote repository server, gunakan perintah git remote add origin [url]

# Push (Mengirim perubahan ke server)
* Untuk mengirim perubahan pada local repository ke server gunakan perintah git push.
* Perintah ini akan meminta memasukkan username dan password pada akun github.com $ git push -u origin master
$ git remote add origin https://github.com/abuazzam/labpy1.git

![iqbal 77](https://user-images.githubusercontent.com/57259403/68079713-7bbe7a00-fe20-11e9-8f3a-0a44eca9d92d.png)

# Melihat hasilnya pada server repository
* Buka laman github.com, arahkan pada repositorinya.             
* Maka perubahan akan terlihat pada laman tersebut.            

![iqbal 88](https://user-images.githubusercontent.com/57259403/68079759-52521e00-fe21-11e9-92f6-f775e3c6d73b.png)

# Clone Repository
* Clone repository, pada dasarnya adalah meng-copy repository server dan secara otomatis membuat satu direktory sesuai dengan nama repositorynya (working directory). 
* Untuk melakukan cloning, gunakan perintah git clone [url]

![iqbal 99](https://user-images.githubusercontent.com/57259403/68079860-26379c80-fe23-11e9-8c92-14bc62630579.png)
