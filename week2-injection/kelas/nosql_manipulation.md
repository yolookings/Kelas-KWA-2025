# NoSQL Manipulation

## Link Resource

https://juice-shop.herokuapp.com/#/score-board?categories=Injection&showDisabledChallenges=false

## Jawaban + Bukti

![nosql](../../img/nosql_manipulation/done.png)

### Step-by-step

![nosql](../../img/nosql_manipulation/soal.png)

1. pada soal kali ini kita diminta untuk memperbarui ulasan produk secara bersamaan, dimana kita dapat mengguakan burpsuite untuk melakuka update nya

![nosql](../../img/nosql_manipulation/comment.png) 2. pada bagian comment maka kita dapat menangkapnya menggunakan burpsuite

![nosql](../../img/nosql_manipulation/burp.png)

3. disini kita dapat mencari sebuah message yang ada dan juga diserta dengan bearer authenticaiton

![nosql](../../img/nosql_manipulation/edit.png) 4. yang mana pada saat kita send ke repeater maka pada inspector kita ubah yang awalnya PUT menjadi PATCH, serta memodif message dan menghapus id products sebagaiamana pada gambar.

### Catatan

- berhasil memperbarui ulasan produk
