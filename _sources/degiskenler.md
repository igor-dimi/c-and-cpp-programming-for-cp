# Degiskenler


Dogada ve evrendeki objelerin degisime ugramasi ve bu degisime sebep olan eylemler. 


Imperative Programlama paradigmasi, Von Neuman modeli ve programlama tarihcesi hakkinda genel kisa bilgiler, ve bu baglamda degiskenler ile ilgili genel aciklama ve bilgiler.

Program durum uzayi, program durum uzayinda degiskenlerin programin islemi suresince ugradiklari degisim, program sureci degiskenlerin tablosu kavramlarinin
aciklanmasi. On-kosul ve Ard-kosul kavramlarina deginilmesi. Bir programin bir on-kosulu saglayan girdi ve bir ard-kosulu saglayan cikti seklinde tanimlanan bir spesifikasyonu gerceklestiren bir fonksiyon olarak tanimlanmasi

Komut/Eylem vs Ifade/Deger. C ve C++'a ozel olarak bazi dil konstruktlerinin hem ifade hem de komut olabilmesi 

```c
/*
    degiskenler.c
    Prog 1 Ders 2
    2021/12/11
*/

#include <stdio.h>

int main() {
    int yumurtaSayisi = 6;

    printf("Sepette ");
    printf("%d", yumurtaSayisi);
    printf(" tane yumurta var.\n");

    yumurtaSayisi = yumurtaSayisi - 1;

    printf("Birisi dustu... ");
    printf("%d",  yumurtaSayisi);
    printf(" tane kaldi.\n");

    return 0;
}

```

## Degisken Tipleri

Sinif, kume, tip, eslik sinifi ve predikat kavramlarinin icgudusel aciklmasi, bu kavramlar arasindaki baglantilar. Evrendeki farkli benzer objelerin ayni tip sinifi siniflandirilmasi ve bunun programlama dillerindeki degisken tipi kavrami ile olan baglantisinin aciklanmasi. Degisken tiplerinin alabilecegi degerler ve bu degerler uzerine uygulanabilen temel islemler. c ve c++' temel degisken tipleri. Int, 2's complement. 2's complement 3 bitlik basit aciklamasi ve sematik gosterimi. Unsigned int. Float, char

```c
/*
    degiskenTurleri.c
    Prog 1 Ders 2
    2021/12/11
*/

#include <stdio.h>

int main() {
    int yusufYas = 19;

    printf("Yusuf ");
    printf("%d", yusufYas);
    printf(" yasinda.\n");

    long long evrenYas =  13800000000;

    printf("Evren ");
    printf("%lld", evrenYas);
    printf(" yasinda, olmasi gerektigi gibi.\n");

    int yalanciKesir = 1/4;

    double gercekKesir = 1.0/4;

    printf("%d", yalanciKesir);
    printf(" yanlis, ama ");
    printf("%lf", gercekKesir);
    printf(" dogru.\n");
}
```


## Integer Overflow

```c
/*
    integerOverflow.c
    Prog 1 Ders 2
    2021/12/11
*/

#include <stdio.h>

int main() {
    int yusufYas = 19;

    printf("Yusuf ");
    printf("%d", yusufYas);
    printf(" yasinda.");

    printf("Yusuf %d yasinda.\n", yusufYas);

    int evrenYas =  13800000000;

    printf("Evren ");
    printf("%d", evrenYas);
    printf(" yasinda??\n");
}

```

