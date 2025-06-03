Proje 3

Binary Search Tree Projesi

[7, 5, 1, 8, 3, 6, 0, 9, 4, 2] dizisinin Binary-Search-Tree asamalarini yaziniz.

Ornek: root x'dir. root'un saginda y bulunur. Solunda z bulunur vb.

1. Dugum Yerlestirme Kuralı: Sol alt agac o dugumden kucuk elemanlari içerir, sag alt agac o dugumden buyuk elemanları icerir. 
2. Genellikle BST'de her eleman tektir, izin verilirse esit degerler genellikle saga veya sola belirli bir kurala gore eklenir.
3. Her yeni eleman, kokten baslanarak uygun yere kadar karsilastirilarak yerlestirilir. Kucukse sola, buyukse saga, uygun bos yere kadar devam et.
4. BST rekursif bir yapıdır. (Kendi icinde tekrar eder) Her alt agac da kendi icinde bir BST'dir.
5. Arama, Ekleme ve Silme için, 
    Arama (dengeliyse) O(logn)
    Ekleme (dengeliyse) O(logn)
    Silme daha karmasik, yaprak dugumse silinir, tek cocugu varsa cocuk yukari alinir, iki cocugu varsa sag alt agacin en kucuk elemani veya sol alt agacin en buyuk elemani yukari alinir.
    Verilen dizi:  
`[7, 5, 1, 8, 3, 6, 0, 9, 4, 2]`

Agac Olusumu Asamaları;

1. Ilk eleman root = 7,
2. İkinci eleman = 5, 5 < 7, 5 7'nin soluna yerlesir.
3. Ucuncu eleman = 1, 1 < 7, 1 < 5, 1 5'in soluna yerlesir.
4. Dorduncu eleman = 8, 8 > 7, 8 7'nin sagina yerlesir.
5. Besinci eleman = 3, 3 < 7, 3 < 5, 3 > 1, 3 1'in sagina yerlesir.
6. Altinci eleman = 6, 6 < 7, 6 > 5, 6 5'in sagina yerlesir.
7. Yedinci eleman = 0, 0 < 7, 0 < 5, 0 < 1 , 0 1'in soluna yerlesir.
8. Sekizinci eleman = 9, 9 > 7, 9 > 8, 9 8'in sagina yerlesir.
9. Dokuzuncu elema = 4, 4 < 7, 4 < 5, 4 > 1, 4 > 3. 4 3'un sagina yerlesir. 
10. Onuncu eleman = 2, 2 < 7, 2 < 5, 2 > 1, 2 < 3, 2 3'un soluna yerlesir.

Ağaç yapısı:

```
        7
      /   \
     5     8
    / \     \
   1   6     9
  / \
 0   3
    / \
   2   4