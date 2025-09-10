# SQL Injection

## Link Resource

https://portswigger.net/web-security/sql-injection/lab-login-bypass

## Jawaban + Bukti

![sql](../../img/sql-injection/done.png)

### Step-by-step

![sql](../../img/sql-injection/before.png)

![sql](../../img/sql-injection/soal.png)

1. pada soal kali ini kita diminta untuk SQL Injection pada halaman login sehingga bisa masuk sebagai user administrator tanpa tahu password-nya.

![sql](../../img/sql-injection/login.png)

2. kita dapat menggunakan burpsuite untuk mengintercept request

![sql](../../img/sql-injection/ganti.png)

3. kemudian kita dapat mengganti username yang kita pakai login menjadi `administrator'--` sebagai payload untuk membypass system

4. kemudian setelah itu kita forward dan sukses melakukan bypass.

### Catatan

- sukses melakukan SQL Injection
