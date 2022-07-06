# Cok Boyutlu Diziler,  Fonksiyonlar, Oz-yineleme, Pointerlar ve Adresler

### Diziler Tekrar

```c
/*
    dizilerTekrar.c
    Prog 1 Ders 6
    2022/01/04
*/

#include <stdio.h>

int main() {
    int dizi1[10];
    int dizi2[10];

    int n;
    scanf("%d", &n);

    {
        int i = 0;

        for (i = 0; i < 4; i++) {
            scanf("%d", &dizi1[i]);
        }
    }

    for (int i = 0; i < 4; i++) {
        printf("%d", dizi1[i] * 10);
    }

    for (int i = 1; i <= 4; i++) {
        scanf("%d", &dizi2[i]);
    }

    for (int i = 1; i <= 4; i++) {
        printf("%d", dizi2[i] * 100);
    }

    return 0;
}
```

### Cok Boyutlu Diziler

```c
/*
    cokBoyutluDiziler.c
    Prog 1 Ders 6
    2022/01/04
*/

#include <stdio.h>

int main() {
    int dizi[10][10];
 
    int satirSayisi, sutunSayisi;
    scanf("%d %d", &satirSayisi, &sutunSayisi);

    for (int i = 0; i < satirSayisi; i++) {
        for (int j = 0; j < sutunSayisi; j++) {
            scanf("%d", &dizi[i][j]);
        }
    }

    for (int i = 0; i < satirSayisi; i++) {
        for (int j = 0; j < sutunSayisi; j++) {
            printf("%d ", dizi[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```

### Fonksiyonlar

```c
#include <stdio.h>

int faktoriyel(int x) {
    if (x > 0) {
        return x * faktoriyel(x-1);
    }

    return 1;
}


int main() {
    printf("%d", faktoriyel(5));
    return 0;
}
```


### Pointerlar

```c
/*
    pointerlar.c
    Prog 1 Ders 6
    2022/01/04
*/

#include <stdio.h>

int main() {
    int sayi = 4;

    int *sayiPointeri;

    sayiPointeri = &sayi;

    scanf("%d", sayiPointeri);
    printf("%d\n", sayi);

    if (sayi == *sayiPointeri) {
        printf("YAPILIYOR\n");
    }

    
    return 0;
}
```