# Sarah Palin Fanpage - 35 points
## Deskripsi

Are you a true fan of Alaska's most famous governor? Visit the [Sarah Palin fanpage](http://sarah_palin_fanpage.tjctf.org/).

## Flag

```
tjctf{wkDd2Pi4rxiRaM5lOcLo979rru8MFqVHKdTqPBm4k3iQd8n0sWbBkOfuq9vDTGN9suZgYlH3jq6QTp3tG3EYapzsTHL7ycqRTP5Qf6rQSB33DcQaaqwQhpbuqPBm4k3iQd8n0sWbBkOf}
```

## Penyelesaian

Pertama, buka VIP area dan akan terdapat tulisan bahwa hanya fans Sarah Palin yang sudah mengelike semua top 10 moment-nya lah yang bisa mengakses. Kemudian kita periksa cookie dan terdapat satu cookie bernama `data` yang nampak mencurigakan. kemudian kita decode value-nya menggunakan [Base64 Decoder](https://www.base64decode.org/). hasilnya adalah:

```
{"1":false,"2":false,"3":false,"4":false,"5":false,"6":false,"7":false,"8":false,"9":false,"10":false}
```

Selanjutnya adalah mengubah `false` menjadi `true`, lalu encode lagi menjadi Base64 dan masukkan kembali ke value cookie nya. terakhir, simpan cookie dan refresh page.