# Degiskenler


Objeler, eylemler ve islemler 

Imperative Programlama paradigmasi, Von Neuman modeli ve programlama tarihcesi hakkinda genel kisa bilgiler

Program durum uzayi, program sureci ve islem izi, degiskenlerin program sureci boyunca aldiklari farkli degerler. On-kosul ve Ard-kosul kavramlari. Bir programin bir on-kosulu saglayan girdi ve bir ard-kosulu saglayan cikti seklinde tanimlanan bir spesifikasyonu gerceklestiren bir fonksiyon olarak tanimlanmasi

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

Sinif, kume, tip, eslik sinifi ve predikat kavramlari ve bu kavramlar arasindaki baglantilar. Benzer ozellikler gosteren objelerin ayni sinif veya tip altinda siniflandirilarak olusturulan matematiksel uzay. Degisken tiplerinin alabilecegi degerler ve bu degerler uzerine uygulanabilen temel islemler.  c ve c++'de temel degisken tipleri. Int, 2's complement. 2's complement 3 bitlik basit aciklamasi ve sematik gosterimi. Unsigned int. Float, char

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

