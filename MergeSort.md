**Proje 2 **

Merge Sort

[16,21,11,8,12,22] -> Merge Sort

Yukarıdaki dizinin sort türüne göre aşamalarını yazınız.
Big-O gösterimini yazınız.

*Merge Sort* Birleştirmeli Siralama anlamina gelmektedir. "divide and conquer" yaklasimini kullanmaktadir, etkili ve kararli bir siralama algoritmasidir.

**Merge Sort** algoritmasi bir diziyi surekli olarak ikiye bolmekte ve sonra bu kucuk parcalari sirali bir sekilde birlestirerek (merge) geri  toplamaktadir. 

**Zaman Karmasikligi(Time Complexity)**  En kotu, en iyi ve ortalama durumda O(n log(n))
**Kararli Siralama** Aynı değere sahip elemanların sirasi korunmaktadir.*Stable Sort*
Büyük veri kumeleri icin uygundur.
Rekursif ya da iteratif olarak uygulanabilmektedir.

dezavantaj olarak ekstra hafiza kullanımı ve kucuk diziler icin Insertion Sort gibi yontemlerden yavas olmasi sayilabilmektedir.

Baslangic Dizisi: [16,21,11,8,12,22]

    1. Dizi ikiye bolunur:
    [16,21,11] ile [8,12,22]
    
    2. Alt diziler tekrar bolunur:
    - [16,21,11] -> [16], [21,11]
        * [21,11] -> [21], [11] birlestirilir -> [11,21]
        * [16] ile [11,21] birlestirilir -> [11,16,21]

    - [8,12,22] -> [8], [12,22]
        * [12,22] -> [12], [22], birlestirilir -> [12,22]
        * [8] ile [12,22] birlestirilir -> [8,12,22]

    3. Son iki sıralı alt dizi birlestirilir:
    [11,16,21] ile [8,12,22]

    - MErge islemi ile siralanir:

    1. 8 < 11, 8
    2. 11 < 12, 11
    3. 12 < 16, 12
    4. 16 < 21, 16
    5. 21 < 22, 21
    6. 22 sona eklenir.

    Sonuc: [8,11,12,16,21,22]

Big-O Gosterimi: Merge Sort'un zaman karmasiklgi olup O(n logn) seklinde gosterilir.
Her bolme islemi logn derinliginde, her seviyede toplam n islem yapilir.

