# Pengerjaan Level 1

oleh Muhammad Nabil Akhtar Raya Amoriza  

## Daftar Isi
- [Soal 1](#soal-1)
  - [a. Membuat sebuah repository](#a-membuat-sebuah-repository)
  - [b. Membuat sebuah remote repository](#b-membuat-sebuah-remote-repository)
  - [c. Menghubungkan local dan remote repository](#c-menghubungkan-local-dan-remote-repository)
  - [d. Melakukan Perubahan](#d-melakukan-perubahan)
- [Soal 2](#soal-2)
  - [a. Introduction](#a-introduction)
  - [b. Branching](#b-branching)
  - [c. Merging Branches (ft. Soal 5)](#c-merging-branches-soal-5-nyelak)
- [Soal 3](#soal-3)
  - [a. Git Stash](#a-git-stash)
  - [b. Git Reset](#b-git-reset)
  - [c. Git Push (ft. Git Stash Pop)](#c-git-push-ft-git-stash-pop)
  - [d. Git Diff](#d-git-diff)
  - [e. Git Merge](#e-git-merge)
  - [f. Git Pull (ft. Soal 4)](#f-git-pull-soal-4-nyelak)
- [Kendala dan Kesulitan](#kendala-dan-kesulitan)

</br>

## Soal 1

Membuat sebuah repository sesuai dengan struktur yang diperintahkan.

### a. Membuat sebuah local repository

Pertama-tama, pergilah ke folder yang ingin ditrack menggunakan git kemudian initialize git menggunakan perintah `git init`. Command ini dapat membantu initialize git ke dalam foldermu.

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207192432676970617/ajk-1.png?ex=65dec090&is=65cc4b90&hm=34f0eddafa895746fbbe2544a79fd5b3c8635f410bb01cf35d1614966ed399d5&)

### b. Membuat sebuah remote repository

Seusai menyiapkan local repository, saatnya untuk membuat sebuah repository di laman GitHub menggunakan browser pilihan anda yang tercinta (OperaGX)

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207194089959718932/operagxblahaj.png?ex=65dec21b&is=65cc4d1b&hm=c087da1bd1e1d2af22e770d7ab3d8025a02b78642167efbce9188ee8b2b3e26d&)

Setelah login menggunakan akun GitHubmu, buatlah sebuah repository dengan nama 'ajk-nabil-penugasan1'. Pastikan untuk mencentang opsi 'private' berhubung pengerjaan ini sebelum deadline pengumpulan. 

Kemudian, pastikan anda mencentang opsi 'add README.md' dan klik tombol 'create repository'

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207208059328266250/image.png?ex=65decf1e&is=65cc5a1e&hm=9df425047a1e52b1ac5e8f215162d98e29d0668c12dda2b7037a0b053141222e&)

### c. Menghubungkan local dan remote repository

Setelah selesai, copy link https yang ada di laman repository mu dan kemudian tambahkan sebuah remote pada terminal / vscode dengan command `git remote add <remote_name> <link>`. Command yang saya gunakan sebagai berikut.

```
git remote add origin https://github.com/reivertt/ajk-nabil-penugasan1.git
```

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207195896677142538/image.png?ex=65dec3ca&is=65cc4eca&hm=0b223a6ce1bedb8e3eee6e120079173d089f678f0861c189df41210c87e0d009&)

Setelah itu, lakukan `git pull <remote_name> <branch_name>` untuk menyinkronkan local repository ke branch yang sesuai dengan remote repository. Command yang saya gunakan sebagai berikut.

```
git pull origin master
```

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207231449330352179/image.png?ex=65dee4e6&is=65cc6fe6&hm=f0a3ab2fd839593a8075d521f0df50e5c6ab45be01ead9b7a991846dfd1c8bf3&)

### d. Melakukan perubahan

Buka folder tersebut menggunakan vscode dan buatlah struktur file seperti berikut.

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207192432450732052/ajk-2.png?ex=65dec090&is=65cc4b90&hm=55e5b25cf4fdfd4eae413a9185c643a6fbf3161cea950c26e1d4a4f62808623a&)

Setelah selesai, perubahan yang telah anda lakukan dapat dilihat menggunakan command `git status`. Command tersebut dapat menampilkan perubahan-perubahan yang terjadi dalam foldermu. 

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207200155233812480/ajk-4.png?ex=65dec7c1&is=65cc52c1&hm=5f5f4e14b3faa2cbdeaaacf5f6be7fb0c516f4279a5be8b0dfbc9ed852c075bb&)

Untuk mempermudah proses tracking, saya akan blacklist folder '.vscode' agar tidak teregistrasi dalam list perubahan dengan menambahkan folder tersebut ke sebuah file '.gitignore'. Hal tersebut dapat dilakukan seperti berikut.

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207233849600380948/image.png?ex=65dee723&is=65cc7223&hm=d652b35b128d6eaeaf97461c38bdb27dbbaaa8f75e20867d77b0d23a263e5df5&)

Dapat dilihat bahwa kita sedang berada pada branch 'master', kemudian perubahan yang telah anda lakukan dapat ditrack menggunakan `git add`. Penambahan file bisa dilakukan untuk lebih dari satu dengan perincian tanda '.' seperti berikut.

```
git add .
```

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207234232926347314/image.png?ex=65dee77e&is=65cc727e&hm=ee31e57b9b17f96e58ee07339a74e0593d45f8fd78a531987e26d7bfff404c25&)

Kemudian, file yang sudah ditrack dapat dicommit ke local repository menggunakan command `git commit -m '<message>'`. Keterangan `-m` disini berarti tambahan message untuk commit tersebut. Command yang saya gunakan sebagai berikut.

```
git commit -m 'first commit'
```

Hasil command tersebut dapat dilihat menggunakan command `git log`. Command tersebut akan menunjukkan log ataupun rekaman-rekaman mengenai perubahan yang anda lakukan.

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207234530528727070/image.png?ex=65dee7c5&is=65cc72c5&hm=6a7073b965c8b6c7ac90b01dd9e4c5d7a39dbd16b9b5c9179b55fcda169ada24&)

Seusainya hal tersebut, perubahan-perubahan tersebut dapat dipush ke remote `origin` yang berupa halaman repository di GitHub menggunakan command `git push -u <remote_name> <branch_name>`. Keterangan `-u` disini untuk menambahkan upstream tracking dengan referensi. Command yang saya gunakan sebagai berikut.

```
git push -u origin master
```

Menggunakan command `git log` kembali, perubahan dapat terlihat dengan munculnya `origin/master` di sebelah keterangan `HEAD` menandakan branch dan remote sudah up-to-date.

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207234888743391242/image.png?ex=65dee81a&is=65cc731a&hm=02bd5250e2497b2189ec29eae8b186bef946d2d3fd91c8542c5d77b8bd47162d&)

</br>

## Soal 2

Branching dan juga studi kasus.

### a. Introduction

Untuk penugasan kali ini, anda ditugasi untuk membantu penderita adhd ambis yang gabisa fokus dan juga memiliki dua monitor. Client anda ingin fokus terhadap suatu topik dan tidak lari kemana". Agar tidak mendistraksi, anda menentukan bahwa sebuah website yang dapat menampilkan waktu dan tugas yang sedang dilakukan sebagai pekerjaan yang ringan dan juga efektif.

Requirement yang anda perlukan:
- Website estetis
- Website mampu menampilkan waktu
- Website dapat diberi teks untuk menampilkan task yang sedang dilakukan

Tentu hal itu memerlukan beberapa branch.

### b. Branching

Disini kita perlu membuat beberapa branch untuk 3 fitur yang kita inginkan. Untuk membuat sebuah branch dapat menggunakan command berikut `git branch <branch_name>`. Command yang saya gunakan seperti berikut

```
git branch develop
git branch feat/aesthetics
```

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207241850986176543/image.png?ex=65deee96&is=65cc7996&hm=909aff5836772f8b85674b73e61d2142323a8894fb00fccc26a2fe6e96f6b51e&)

Untuk pindah dari branch `master` ke branch `develop`, dapat digunakan command `git checkout <branch_name>`. Berikut command yang saya gunakan.

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207242390394638406/image.png?ex=65deef17&is=65cc7a17&hm=9d6f622eefef1b5b822815abcdfbd2d5adc43981e5a550ae3fb578838ca5dc51&)

Namun, ternyata anda baru ingat bahwa kerangka website saja belum dibikin. Oleh karena itu, anda perlu mengubah branch 'feat/aesthetics' menjadi 'feat/core'. Untuk itu dapat menghapus dahulu yang salah dan membuat baru dengan command berikut.

```
git branch -D feat/aesthetics
git branch feat/core
```

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207243262314946640/image.png?ex=65deefe7&is=65cc7ae7&hm=c523bb6007d74675096d8bbe8017fbc5487a4ee2f99a8f5bb9877702161b57fe&)

Kemudian, development bisa dilanjutkan.

### c. Merging Branches (soal 5 nyelak)

Setelah melakukan beberapa perubahan, update selanjutnya akan seperti ini.

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207255160980635678/image.png?ex=65defafc&is=65cc85fc&hm=50cca50d2c3537eb03663310c6dd8165c4d0842191a2fc384ee83780c9765678&)

Berhubung feature tersebut sudah lengkap, maka branch feat/core akan digabungkan dengan branch develop. Untuk itu akan dilakukan merging. Sebelumnya, kita perlu pindah ke branch development terlebih dahulu dan kemudian melakukan command `git merge <branch_name>`. Command yang digunakan merupakan.

```
git checkout develop
git merge feat/core
```

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207259031518052393/image.png?ex=65defe96&is=65cc8996&hm=5b80277e320a51481f9f388c383136a1b38f0c4caf718a3d8450277dff5cd896&)

Waduh, ternyata pas dilihat branchnya udah ga keliatan dan langsung melakukan fast-forward. Nah ternyata untuk mengatasi itu bisa menggunakan `git merge --no-ff <branch_name>`.

Untuk mundur dalam waktu, kita bisa menggunakan command `git reset <branch_id>` dan kemudian mengulang kembali. Hasilnya akan seperti berikut.

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207261673266741278/ajk-6.png?ex=65df010c&is=65cc8c0c&hm=074fa92c7b7458867813f37b5135b5087050f414909c4f8ec360402402ced05c&)

</br>

## Soal 3

Beberapa instruksi git.

Pada bagian ini, akan diberi contoh mengenai beberapa instruksi:
- git push
- git pull
- git stash
- git reset
- git diff
- git merge
- dan lain lain

*time skip, project di fast forward deh*

### a. Git Stash

Kita sekarang sedang berada di branch style/aesthetics. Tiba-tiba, anda teringat untuk membuat perubahan pada branch feat/clock namun belum ingin ngepush perubahan. Kita bisa menggunakan git stash untuk mengatasi itu. 

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207274236423704646/image.png?ex=65df0cc0&is=65cc97c0&hm=cc8c71fa0a2d9efaf6a92f7c9ac6136af285fbb73eb9e09eb5251b9d6b4ce043&)

Perubahan branch dengan progress yg belum diatasi itu tidak mungkin tanpa adanya git stash. 

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207274435212746773/image.png?ex=65df0cef&is=65cc97ef&hm=01c1e248e8cad345164746fd5d86cd09f5b02e4d6a84eb2ab0efc62c0af162d9&)

### b. Git Reset

Pada branch feat/clock, anda ingin mengubah agar clock berada di bawah current task.

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207275542102024202/Layer_5_1.png?ex=65df0df7&is=65cc98f7&hm=228340f3f6ab01215b3827ca08b4812e130b9e57f956577d43bb588c61d9c364&)

Kemudian, anda push progress tersebut ke current branch.

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207276146337775686/image.png?ex=65df0e87&is=65cc9987&hm=d71d0dc33af6705f1b7b97e1820a226f25f55e917770c0341fe283fb09c759e5&)

Namun, ternyata pas dipikir-pikirin masih mending yang awal. Yasudah, tinggal di reset. Hal ini dapat menggunakan `git reset <commit-id>`. Hal ini akan memundurkan timeline ke log yang anda inginkan. Kemudian apabila masih tersisa file yang masih tracked, bisa dikembalikan ke kondisi sebelumnya dengan `git restore <file_name>`.

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207278247780290570/image.png?ex=65df107c&is=65cc9b7c&hm=c7260aff128b6bb5e251beb7a1bb2c0b6b4b9f2763c91e5a1e8fc7be44ff6b7d&)

### c. Git Push (ft. Git Stash Pop)

Seusai mengubah file di branch feat/clock, kita beralih kembali ke branch style/aesthetics. Untuk mengembalikan progress kita, bisa menggunakan command `git stash pop`. Kemudian, progress kita bisa ditrack dengan series `git add .` (untuk add semua file yg untracked), `git commit -m <commit-message>` untuk melakukan commit, dan terakhir `git push` ataupun `git push -u <remote_name> <branch_name>` untuk push ke remote.

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207279419639603220/image.png?ex=65df1193&is=65cc9c93&hm=f7ea190f281c772df941829a9bcc9b0fc435dbb1a5e89bcb6c1ab3edce214277&)

### e. Git Merge

Setelah selesai mengerjakan fitur feat/clock, kita akan merge dengan branch develop. Hal tersebut dilakukan dengan command berikut.

```
git checkout develop
git merge --no-ff feat/clock
```

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207337598662610994/image.png?ex=65df47c2&is=65ccd2c2&hm=5412577bf6beecc7d8a67370b0f9e3a54a434f79b942905c6196ac852dc2660b&)

### f. Git Pull (soal 4 nyelak)

Untuk melakukan pull, remote repository harus lebih maju / ahead dibanding local repository. Kita akan melakukan merge ataupun pull request fitur style/aesthetics menggunakan website GitHub. 

Pertama, kita bisa membuka halaman repository mu dan juga membuka branch yg ingin diajukan pull request

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207339746871873568/image.png?ex=65df49c2&is=65ccd4c2&hm=05986ac0ce40156ae83823a78f7eafc28a32ab4c25b7a47c038fd82920b652d3&)

Kemudian, klik 'Contribute' dan bukalah sebuah pull request. Atur target branch pull request dan juga sumbernya agar sesuai. Isi dokumentasi yang memadai dan ajukan.

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207340258203533322/image.png?ex=65df4a3c&is=65ccd53c&hm=418acc0eeb63b6c1d9454aaeca32336662832a0e4f31c9020f640446acbef895&)

ALHAMDULILLAH DAPET MERGE CONFLICT, okeh disini kita akan nyempilin nomer 4 okeh okeh

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207340479079907368/image.png?ex=65df4a71&is=65ccd571&hm=075bc470331af952d6f997554f9dc9b3952227151f5db4a3b4429ff892392c4f&)

berhubung kita mendapatkan sebuah merge conflict, tentu langkah selanjutnya ialah untuk menyelesaikan conflict tersebut.

before
![img](https://cdn.discordapp.com/attachments/718028750503280671/1207341212739047435/image.png?ex=65df4b20&is=65ccd620&hm=acac2ce0c18a1fc924f10455e9abc0ef5051b8c4a29b04893085172b3bc69821&)

after
![img](https://cdn.discordapp.com/attachments/718028750503280671/1207341491857391686/image.png?ex=65df4b62&is=65ccd662&hm=a4bd9b973b369b6025f36305660b236eb9ece942574391481cbf4701a474c283&)

Seusai memilih perubahan mana yang benar, conflict kemudian dapat diresolve dan merge dapat dilakukan.

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207341646438604810/image.png?ex=65df4b87&is=65ccd687&hm=8c13f2a332ec0fb7b65392424bc78f90429a22014698e2e07da11b8af238ef32&)

Apabila selesai, dapat merge kedua branch dan kemudian menghapus branch style/aesthetics.

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207342382270517258/image.png?ex=65df4c37&is=65ccd737&hm=3ea2c29b6caf0b5b7bab7fbca598638c201f004597004b3f558b586eb335961c&)

Pada saat ini, kondisi git pada remote repository lebih maju dibanding local repository. Oleh karena itu segala perubahan yang kita lakukan belum akan terlihat secara local. Untuk mengatasi itu, kita dapat melakukan `git pull`.

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207343050544783430/image.png?ex=65df4cd6&is=65ccd7d6&hm=e2210902fff310b17a9908546bf9f0601e669ba36b4e418ef6c6da25c9566d3d&)

### d. Git Diff

Ternyata, ukuran font pada website terhitung terlalu besar. Oleh karena itu anda akan membantu merubah itu.

Setelah melakukan perubahan, anda dapat melihat line mana saja yang berubah dengan command `git diff`.

![img](https://cdn.discordapp.com/attachments/718028750503280671/1207344424049184849/image.png?ex=65df4e1e&is=65ccd91e&hm=9a56be021c7f2df8ab65724950b696ee9b621ebc37b5f436164a20041abd37bf&)

</br>

## Kendala dan Kesulitan

Jujur, kesulitan yang saya alami dalam level ini itu bingung dalam pengelolaan local dan remote repository. Kapan buat push yang local ke remote, tapi ternyata sama aja wkwkwkw.  

Terus selain itu ada juga bingung cara merge itu gimana. Ternyata perlu ke branch tujuan dulu baru `git merge <branch_name>`.

Proses yang relatif tedious dan justru lebih bingung buat bikin alur yang masuk akal biar sesuai dengan nomer-nomer soal. Sepertinya saya perlu nanya-nanya kembali ke admin karena ini ada beberapa poin yang loncat loncat... Semoga dibolehkan :D 
