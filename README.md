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

# Menambahkan File baru pada repository
* Untuk menambahkan file yang baru saja dibuat tersebut gunakan perintah git add.
* File README.md berhasil ditambahkan. ``$ git add README.md``

![iqbal 4](https://user-images.githubusercontent.com/57259403/68079450-4021b100-fe1c-11e9-952f-1dff50081d5f.png)


# Membuat repository server
* Server reopsitory yang akan kita gunakan adalah http://github.com 
* Anda harus membuat akun terlebih dahulu. 
* Pada laman github, klik tombol start a project, atau 
* Dari menu (icon +) klik New Repository
