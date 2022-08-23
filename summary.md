Materi Aqua Developer Day- 2
Berikut rangkuman materi yang didapat saat pertemuan hari ke-2 berlangsung di indigo space, malang

- pengertian git dan sejarahnya

git adalah sebuah tools yang membantu developer dalam mengelola repository project dan bisa juga mengatur jalannya kolaborasi antar developer saat membangun sebuah aplikasi secara bersama-sama.
git dulunya dicetuskan oleh linus torvalds (penemu os linux) ketika beliau membuat project linux-nya menjadi open source. hingga banyak orang tertarik untuk berkontribusi dalam mengembangkan project tersebut sehingga sering terjadi perubahan code yang kurang jelas asal muasalnya dan menyebabkan terjadinya misscellaneous dari source code tersebut. untuk mengatasi problem tersebut, linux akhirnya membuat suatu inovasi berupa aplikasi bernama git yang digunakan sampai sekarang dalam membantu kinerja developer mengelola project yang sedang dikembangkan baik secara personal maupun kelompok.

- cara kerja git

ketika menggunakan git, folder akan tersimpan di dalam project yang dibuat dengan 4 tahap seperti:

1. working directory = sebuah direktori yang menyimpan code yang masih dalam tahap pengembangan
2. staging area = sebuah tempat yang digunakan sebagai pusat berkumpulnya file yang telah digubah sebelumnya
3. local repository = suatu tahap dimana perubahan yang sudah ditetapkan tapi masih berjalan di lokal komputer dan belum diunggah ke cloud
4. romye repository = suatu tahap dimana perubahan code sudah diunggah ke cloud dan dapat diakses oleh developer lain.

- command di dalam git

berikut beberapa commands yang sering digunakan sebagai berikut.

1. git status : untuk melihat u[pdate dokumen yang terdapat di repository
2. git pull : untuk menarik code yang ditulis oleh user/dev lainnya
3. git commit : sebagai penanda sebelum melakukan git push

4. branches
   a. git branch : untuk melihat isi branch lokal
   b. git branch -a : untuk melihat isi semua branch lokal dan remote repo
   c. git checkout -b (branch_name) : membuat branch lokal baru dan bisa langsung pindah ke brach baru tersebut
   d. git checkout (branch_name)) : pindah ke sebuah branch
   e. git push origin (branch_name) : upload semua perubahan pada lokal brach ke remote branch
   f. git branch -m (new_name) : mengubah nama sebuah local branch
   g. git branch -d (branch_name) : menghapus lokal branch
   h. git push origin :(branch_name) : menghapus remote branch

5. logs
   a. git log --oneline : melihat riwayat commit secara singkat
   b. git diff : melihat semua changes
   c. git diff myfile : melihat changes pada file tertentu

6. cleanup
   a. git clean -f : menghapus semua file yang tidak terlacak
   b. git clean -df : menghapus semua file dan folder yang tidak terlacak
   c. git checkout -- . : membatalkan semua perubahan yang dilakukan di lokal

7. git merge (branch_name): menggabungkan beberapa urutan commit menjadi satu
8. git stash (command) : menyimpan perubahan
9. git fetch (remote) [options] : mengambil infometa-data terbaru dari yang asli ke git lokal
10. git remote [option] : menghubungkan repo secara remote
11. git init : membuat git repo baru
12. git add [file] <or> git add [directory] : menambahkan file atau direktori pada repo
13. git quiet : menyembunyikan file repo yang kurang penting

- commit convertion

commit convertion adalah sebuah cara dalam membawakan productive testing environmet kepada developer lain karena bertujuan untuk memudahkan developer lain dalam mengembangkan project yang sedang dibangun bersama. selain fungsi tersebut, commit convertion memiliki fungsi lain sebagai automatic geberating pada changelog dan navigasi sederhanda lewat git history.
contoh commit convertion pada git adalah git karma convertion yang memiloki format seperti berikut.

<type> [optional scope]: <description>

[optional body]

[optional footer(s)]

commit berisi elemen struktural berikut, untuk mengomunikasikan maksud kepada konsumen library user:

1. fix: commit dari jenis perbaikan memperbaiki bug di basis kode Anda (ini berkorelasi dengan PATCH dalam Versi Semantik).
2. feat: commit dari tipe feat memperkenalkan fitur baru ke basis kode (ini berkorelasi dengan MINOR dalam Versi Semantik).
3. BREAKING CHANGE: commit yang memiliki footer BREAKING CHANGE:, atau menambahkan ! setelah tipe/cakupan, memperkenalkan perubahan API yang melanggar (berkaitan dengan UTAMA dalam Versi Semantik). PERUBAHAN BREAKING dapat menjadi bagian dari komit jenis apa pun.
4. types other tahn fix: andfeat: diperbolehkan, misalnya @commitlint/config-conventional (berdasarkan konvensi Angular) merekomendasikan build:, chore:, ci:, docs:, style:, refactor:, perf:, test :, dan lain-lain.
5. footer other BREAKING CHANGE: <description> dapat disediakan dan mengikuti konvensi yang mirip dengan format trailer git.

- semantic versioning

v<major>, <minor>, <patch>

example : v.2.0.0
patch : fix, perf
minor : feat
major : breaking change in the API

- git management

trunk based management adalah sebuah metode yang menerapkan kolaborasi code dalam satu cabang yang disebut trunk pada mainatau master. selain jtu untuk menghindari penggunaan branches yang panjang durasinya.
