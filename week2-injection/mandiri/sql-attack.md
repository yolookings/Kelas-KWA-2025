# SQL Injection

## Link Resource

https://portswigger.net/web-security/sql-injection/lab-login-bypass

## Jawaban + Bukti

![sql](../../img/sql-attack/done.png)

### Step-by-step

![sql](../../img/sql-attack/soal.png)

1. pada soal kali ini kita diminta kamu menampilkan database version string dari server Oracle dengan teknik UNION SELECT injection.

![sql](../../img/sql-attack/burp.png)

2. kemudian kita intercept request menggunakan burpsuite pada kategori Tech gifts

![sql](../../img/sql-attack/attack.png)

3. Ubah parameter category jadi payload injection menggunakan `'+UNION+SELECT+BANNER,+NULL+FROM+v$version—`

![sql](../../img/sql-attack/version.png)

4. cek response di burpsuite apabila berhasil maka akan muncul database version string.

### Catatan

- SQL Injection
