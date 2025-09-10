# SQL injection UNION attack, retrieving multiple values in a single column

## Link Resource

https://portswigger.net/web-security/sql-injection/union-attacks/lab-retrieve-multiple-values-in-single-column

## Jawaban + Bukti

![sql](../../img/sqli-unioncolumn)

### Step-by-step

![sql](../../img/sqli-unioncolumn/soal.png)

1. pada lab ini kita diminta untuk:

- Menggunakan UNION-based SQL injection
- Menggabungkan (concatenate) nilai username dan password ke dalam satu kolom hasil query.
- Mendapatkan kredensial administrator.

![sql](../../img/sqli-unioncolumn/intercept.png)

2. kita dapat menggunakan burpsuite untuk melakukan intercept pada kategori gifts `GET /filter?category=Gifts`

![sql](../../img/sqli-unioncolumn/2.png)

3. kemudian kita dapat menentukan jumlah kolom dengan ORDER BY `/filter?category=Gifts'+ORDER+BY+2--` sesuai dengan gambar diatas yang mana jika tidak error berarti jumlah kolom minimal 2 kolom.

![sql](../../img/sqli-unioncolumn)

4. lalu Tes UNION SELECT valid `/filter?category=Gifts'+UNION+SELECT+NULL,NULL--`

![sql](../../img/sqli-unioncolumn)

5.

### Catatan

-
