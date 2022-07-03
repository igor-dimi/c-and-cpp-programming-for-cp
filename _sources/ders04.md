# Unary Operatorler ve Temel Donguler



## Unary Operatorler

```++x```, ```x++```, ```--x```, ```x--```  konstruktleri ayni anda hem komut(statement), hem de ifade (expression)'dir. 
Komut olarak **etkileri** x degiskenlerinin icerisinde tutulan degerleri birer arttirmak veya azaltmaktir. Ifade olarak **dondurdukleri deger** ise 
```++x``` ve ```--x``` icin arttirildiktan/azaltildiktan **sonraki** deger, ```x++``` ve ```x--``` icin arttirildiktan/azaltildiktan **onceki** degerdir.
Yani bu konstruktler komut olarak program durum uzayi uzerinde tamamen ozdes etkilere sahipken, ifade olarak farkli degerler alirlar.
Komut/Eylem ve Ifade/Deger kavramlari hakkinda daha detayli bilgi icin  [degiskenler](./degiskenler.md) bolumune bakiniz.

```c
/*
    statement-expression.c
    Prog 1 Ders 4
    2021/12/21
*/

#include <stdio.h>

int main() {
    int x = 5;
    printf("%d\n", x);
    
    // (x--)
    // ... = x
    // x--

    // (--x)
    // --x
    // ... = x

    int y = (x--);
    int z = (--x);

    printf("%d\n", x); // 3
    printf("%d\n", y); // 5
    printf("%d\n", z); // 3

    return 0;
}
```

**hatirlatma**: ```printf``` ve ```scanf``` ile temel girdi/cikti: 

```c
/*
    scanf-newline.c
    Prog 1 Ders 4
    2021/12/21
*/

#include <stdio.h>

int main() {
    int sayi;
    char ch;

    scanf("%d %c", &sayi, &ch);
    printf("%d %c\n", sayi, ch);

    return 0;
}
```

## For Dongusu

```c
/*
    for.c
    Prog 1 Ders 4
    2021/12/21
*/

#include <stdio.h>

int main() {
    // kisim1;
    // for( ; ; ) {
        // if (kisim2) {
        //      s1;
        //      kisim3;
        // }
        // else{
        //      foru bitir
        // }
    //  }

    // for(kisim1; kisim2; kisim3)
    //      s1

    // kisim1 -> baslangic
    // kisim2 -> kontrol
    // kisim3 -> guncelleme
    // s1 -> asil kisim


    // kisim1
    // if (kisim2) dogru
    // else         kes
    // s1
    // kisim3
    // if (kisim2) dogru
    // else         kes
    
    int sayi;

    for (sayi = 1; sayi <= 10; sayi++) {
        printf("%d\n", sayi);
    }

    return 0;
}
```

## While

```c
/*
    while.c
    Prog 1 Ders 4
    2021/12/21
*/

#include <stdio.h>

int main() {
    int sayi;

    sayi = 1;

    while (sayi <= 10) {
        printf("%d\n", sayi);
        sayi++;
    }

    // kisim1
    // while(kisim2) {
    //      s1
    //      kisim3
    // }

    return 0;
}
```

## Do-While

```c
/*
    do-while.c
    Prog 1 Ders 4
    2021/12/21
*/

#include <stdio.h>

int main() {
    int sayi;

    sayi = 1;
    if (sayi <= 10) {
        do {
            printf("%d\n", sayi);
            sayi++;
        }
        while (sayi <= 10);
    }

    return 0;
}
```

## Ornek Program

for-dongusune ornak olarak asallik kontrolu yapan program:


```c
/*
    isPrime.c
    Prog 1 Ders 4
    2021/12/21
*/

#include <stdio.h>

int main() {
    int sayi;
    scanf("%d", &sayi);

    if (sayi <= 1 || sayi > 10000) {
        printf("Girilen sayi [2, 10000] araliginda olmalidir.");
    }
    else {
        int asal = 1;

        int olasiBolen;

        for (olasiBolen = 2; olasiBolen < sayi; olasiBolen++) {
            if (sayi % olasiBolen == 0) {
                asal = 0;
                break;
            }
        }

        if (asal == 1) {
            printf("Sayimiz asal.");
        }
        else {
            printf("Sayimiz asal degil.");
        }
    }

    return 0;
}
```