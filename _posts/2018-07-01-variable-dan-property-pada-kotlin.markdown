---
layout: post
title:  "Kotlin 2 - Variable dan Property pada Kotlin"
date:   2018-07-01 20:57:51
---


# Variable dan Property pada Kotlin

<img src="https://justynaniemiecki.pl/wp-content/uploads/2017/12/apple-1868496_1920.jpg">

### Variable
Ada 2 macam pendefinisian variable pada kotlin, kamu bisa memakai `val` (immutable) ataupun `var` (mutable).

>**Immutable** berarti tidak dapat dirubah nilainya. ~read only<br>**Mutable** berarti dapat dirubah nilainya. ~read and write

{% highlight js %}
val nama : String = "Sudarmo"
{% endhighlight %}

{% highlight %}
val => Jenis immutable
nama => Nama varible
String => Tipe data
"Sudarmo" => Value
{% endhighlight %}

Agar lebih ringkas, kamu boleh menulisnya tanpa menggunakan tipe data.

{% highlight js %}
val nama = "Sudarmo"
{% endhighlight %}

Dengan sendirinya, kotlin akan mengetahui bahwa variabel tersebut bertipe string. Value “Sudarmo” tidak bisa dirubah karena jenis variablenya immutable.

{% highlight js %}
val nama = "Sudarmo"
nama = "Sukijah" //error, value tidak bisa dirubah
{% endhighlight %}

Jika ingin bisa dirubah maka gunakan variable mutable.

{% highlight js %}
var nama = "Sudarmo"
nama = "Sukijah" //berhasil dirubah
{% endhighlight %}

### Property
>**Property** /Atribut adalah variable yang dideklarasikan di dalam class.<br>**Locale** Variable adalah variable yang dideklarasikan di dalam method.<br>**Variable** adalah tempat menyimpan nilai sementara.

Sama seperti variable, kamu bisa mendefinisikan property menggunakan `val` ataupun `var`.

{% highlight js %}
class Motor {
    var namaMotor : String = ""
}
{% endhighlight %}

{% highlight %}
Dalam class motor terdapat satu property dengan nama namaMotor dan dengan tipe data String
{% endhighlight %}

Dalam pemograman berbasis OOP untuk mengakses property kamu diharuskan menggunakan method getter dan setter.

{% highlight js %}
class Motor {
    var namaMotor : String = ""
    
        //getter
        get() = field
        
        //setter
        set(value) {
            field = value
        }
}
{% endhighlight %}

Setelah membuat method getter dan setter kamu bisa akses property tersebut.

{% highlight js %}
val motor = Motor()

//akses setter untuk mengatur nilainya
motor.namaMotor = "Hondey"

//akses getter untuk mengambil nilainya
val nama = motor.namaMotor
{% endhighlight %}

>**Tips**<br>Ketika kamu mengimplementasikan multithreading kamu dianjurkan untuk menggunakan val (immutable) dalam mendeklarasikan varibel, agar thread yang lain tidak bisa merubah nilai varibel yang sudah kamu buat.






