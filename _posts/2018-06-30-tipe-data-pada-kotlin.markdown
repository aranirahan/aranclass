---
layout: post
title:  "Kotlin 1 - Tipe data pada kotlin"
date:   2018-06-30 16:57:51
---


# Tipe Data pada Kotlin

<img src="https://www.tag-cyber.com/images/uploads/blog_uploads/floppy.jpg">

Kamu pasti sudah tahu kalau ada dua macam tipe data, yang pertama adalah tipe data primitif (`int`, `boolean`, `long`, `char`, dll) dan kedua adalah adalah tipe data reference (`array`, `String`, dll).

Tipe data primitif adalah tipe data yang hanya menyimpan satu nilai pada setiap satu variabel. Sebaliknya tipe data reference dapat menyimpan banyak nilai.

Kotlin membuat semua tipe data tersebut bertindak sebagai objek. Berikut beberapa basis tipe data yang harus kamu ketahui:

### Number
Yang termasuk tipe data number: `int`, `long`, `float`, `double`, `short`, `byte`.

{% highlight js %}
val intNomer = 7
val longNomer = 2L
val floatNomer = 4.5F
val doubleNomer = 14.5
val hexaNomer = 0x0F
val byteNomer = 0b010101
{% endhighlight %}

Konversi antar tipe data bisa menggunakan fungsi : `toInt()`, `toDouble()`, `toFloat()`, `toLong()`, `toShort()`, `toByte()`.

Contoh konversi dari `int` ke `double`:

{% highlight js %}
val intNomer = 7
val doubleNomer = intNomer.toDouble()
{% endhighlight %}

Contoh konversi dari `String` ke `int`:

{% highlight js %}
val stringNomer = "333"
val intNomer = stringNomer.toInt()
{% endhighlight %}

Maka value intNomer adalah 333.

### Boolean
Boolean merupakan tipe data logika yang hanya bernilai `true` (benar) dan `false` (salah). Tipe data ini memakai memori paling kecil.

Ada 3 jenis operasi dalam boolean, yaitu : disjunction (`||`), conjunction (`&&`), dan negation (`!`).

{% highlight js %}
//contoh deklarasi pada boolean
val booleanBenar = true
val booleanSalah = false
 
//contoh operasi pada boolean
val a = 2
val b = 6
val c = 4
val x = a < b && b > c //true
val y = a > b && a < c //false
val z = a < b || a > b //true
{% endhighlight %}

### String
Kamu bisa menulis string untuk satu baris dengan tanda petik dua (“ ”). Sedangkan untuk lebih dari satu baris kamu bisa menggunakan triple petik dua (“““ ”””).

{% highlight js %}
val stringSatuBaris = "Hello guys"
val stringMultipleBaris = """ Hi, guys,
                Love you all!"""
{% endhighlight %}

Atau kamu juga bisa gunakan karakter escape untuk membuat baris baru pada string.

{% highlight js %}
val stringMultipleBaris = " Hi, guys, \n"+
      " Love you all!"
 
//atau
val stringMultipleBaris = " Hi, guys, \n Love you all!"
{% endhighlight %}

String bisa diakses sebagai `array` dan bisa diiterasi. Contoh ketika kamu mau mengambil satu karakter di dalam sebuah string “Hi, you!”


{% highlight js %}
val stringSatuBaris = "Hi, you"
val iterasiString = stringSatuBaris[0]
{% endhighlight %}

Maka value `iterasiString` adalah huruf pertama dari value `stringSatuBaris`, yaitu huruf H.

Kamu juga bisa menambahkan variabel dan expressions ke dalam sebuah `string`.

{% highlight js %}
val nomorKamar = 17
val kataKasir = "Nomor kamar kamu adalah $nomorKamar"
{% endhighlight %}

### Array
Untuk array yang berisi satu macam tipe data kamu bisa membuat array dengan fungsi `intArrayOf()`, `booleanArrayOf()`, `charArrayOf()`, `longArrayOf()`, `shortArrayOf()`, `byteArrayOf()`.

{% highlight js %}
val contohIntArray = intArrayOf(1, 3, 5)
{% endhighlight %}

Untuk array yang berisi campuran tipe data kamu gunakan `arrayOf()`.

{% highlight js %}
val campuranArray = arrayOf(1, 7, 8.6, "kata", true)
{% endhighlight %}

Kamu juga bisa membuat array dengan konstraktor array itu sendiri

{% highlight js %}
val nomerArray = Array(4, { i -> i * 2 })
{% endhighlight %}

Konstruktor `Array()` membutuhkan size dan fungsi lambda. Angka 4 pada contoh diatas berperan sebagai size. Sehingga hasil kodenya adalah 4 buah angka dengan kelipatan 2 ([0,2,4,6]).

