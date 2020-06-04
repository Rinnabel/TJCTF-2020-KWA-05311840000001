# Login - 30 points
## Deskripsi

Could you login into this [very secure site](http://login.tjctf.org/)? Best of luck!

## Flag

```
tjctf{inevitable890898}
```

## Penyelesaian

Ketika kita mencoba login dengan nama dan password acak, pasti akan gagal. oleh karena itu, coba kita gunakan inspect elemen dan lihat code untuk box login. Maka di line 70 kita akan menemukan sebagai berikut:

```
var _0xb31c=['value','c2a094f7d35f2299b414b6a1b3bd595a','Sorry.\x20Wrong\x20username\x20o \x20password.','admin','tjctf{','getElementsByName','toString'];
```

dapat dilihat jika username-nya adalah `admin` dan passwornya berbentuk hash md5. kita bisa menggunakan [online decryptor](https://www.md5online.org/md5-decrypt.html). dan akan kita dapatkan passwornya yaitu inevitable. Lalu tinggal login dan muncul flag

![md5](./md5.png)
