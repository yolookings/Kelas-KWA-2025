## Christmas Special

## Link Resource

http://localhost:3000/#/score-board?categories=Injection&showDisabledChallenges=false

## Jawaban + Bukti

![christmas](../../img/christmas-special/done.png)

### Step-by-step

![christmas](../../img/christmas-special/list.png)

1. pada kasus kali ini kita diminta untuk menemukan produk tersembunyi yang tidak tertampil di katalog biasa, sehingga kita memakai `/rest/products/search?q=')`. Namun tetap tidak tertampil karena produk “Christmas Special” sebenarnya ada di database, tapi diberi flag deletedAt (soft-deleted), makanya pada saat dicari ?q=christmas hasilnya kosong. Maka kita perlu memasukkan payload.

![christmas](../../img/christmas-special/chris.png)

2. agar dapat mengetahui produk tersembunyi maka kita dapat memasukkan payload berikut ke dalam param q `test')) UNION SELECT \* FROM Products WHERE deletedAt IS NOT NULL--`

![christmas](../../img/christmas-special/id.png)

3. kemudian kita dapat menambahkan ke dalam bucket dengan melakukan injection pada id cristmas yakni = 10.

![christmas](../../img/christmas-special/bucket.png)

### Catatan

- Sukses Mendapatkan Produk Cristmas Special serta memesannya
