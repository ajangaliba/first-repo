PRoje 1 - Siralama Algoritmalari

Insertion Sort

[22,27,16,2,18,6] dizinin sort turune gore asamalarini yaziniz.

Big-O gösterimini yaziniz.

Time Complexity: Dizi siralandiktan sonra 18 sayisi asagidaki case'lerden hangisinin kapsamina  girer? Yaziniz.

    1. Avarage case: 
    2. Worst case: 
    3. Best case:

[7,3,5,8,2,9,4,15,6] dizisinin Selection Sort'a göre ilk 4 adımını yazınız.

Cevaplar:

Insertion Sort: dizideki her elemani alir ve oncesindeki sirali kisimla karsilastirarak dogru konumuna yerlestirilir yani her eleman, kendisinden once gelenlerle karsilastirilir.

Ornegin, n elemanli bir dizi varsa 2. eleman icin 1 karsilastirma yapilir. 3. eleman icin 2 karsilastirma, ...., n. eleman icin en fazla (n-1) karsilastirma yailir. Toplam karsilastirma sayısı;

    1 + 2 + 3 + ... + (n-1) = n(n-1)/2 = O($n^2$)

Bu en kotu durumda gerceklesir, mesela dizi tamamen ters siraliysa ,her eleman tum oncekilerle karsilastirilir. bu da O(n^2) islem demektir.

[22,27,16,2,18,6] dizisi icin;
1. adim, 2. terime bakılır,
    27 > 22 yerinde kalır -> [22,27,16,2,18,6]

2. adim, 
    27 > 16, 27 saga kayar,
    22 > 16, 22 saga kayar,
    16 yerine yerlesir -> [16,22,27,2,18,6]

3. adim,
    27 > 2, 27saga kayar,
    22 > 2, 22 saga kayar,
    16 > 2, 16 saga kayar,
    2 yerine yerlesir -> [2,16,22,27,18,6]

4. adim,
    27 > 18, 27 sağa kayar,
    22 > 18, 22 saga kayar,,
    18 yerine yerlesir -> [2,16,18,22,27,6]

5. adim,
    27 > 6, 27 saga kayar,
    22 > 6, 22 saga kayar,
    18 > 6, 18 saga kayar,
    16 > 6, 16 saga kayar,
    6 yerine yerlesir -> [2,6,16,18,22,27]


Big-O Notation, en kotu senaryodaki islem sayisini belirtmektedir. Yani bir algoritmanin olceklendikce nasıl davrandığını gostermektedir.

18 sirali dizide avarage case kapsamına girmektedir bu sebeple Big-O gosterimi O(n^2)

    Best Case (dizi zaten sıralı):
    Her eleman sadece bir kez karşılaştırılır → O(n)

    Worst Case (ters sıralı):
    Her eleman, tüm öncekilerle karşılaştırılır → O(n²)

    Average Case:
    Karışık dizi → Ortalama olarak yine O(n²)

Time Complexity - 18'in konumu sirali dizi içinde dizinin ortasinda bulunmakta.
[,26,16,18,22,27]

[7,3,5,8,2,9,4,15,6] dizisinin selection sort'a gore  ilk 4 adimi;

Selection Sort (Secmeli Siralama): siralanmamais diziden her seferinde en kucuk veya en buyuk elemani bulup onu sirali dizinin sonuna veya basina yerlestiren basit ama verimsiz bir siralama algoritmasidir.

    1. Ilk elemandan baslanir.
    2. Dizinin geri kalanindaki enkucuk eleman bulunur.
    3. Bu en kucuk eleman ile mevcut elemanin yeri degistirilir.
    4. Bir sonraki indeks icin aynı islem tekrar edilir. 
    5. Dizi tamamen siralanana kadar devam edilir.

Zaman Karmasikligi (big-O):

    Best Case: O(n²)
    Average Case: O(n²)
    Worst Case: O(n²)
    
    Her durumda iç içe iki döngü olduğu için verimsizdir. 

Basit ve kolay anlasilir, Ekstra bellek gerektirmez.

1. Adim,

Aranan en kucuk deger: 2,
7 ile yer degistirecek,
[2,3,5,8,7,9,4,15,6]

2. Adim,

Geriye kalan dizi [3,5,8,7,9,4,15,6]
En kucuk 3, zaten yerinde,
[2,3,5,8,7,9,4,15,6]

3. Adim,

Geriye kalan dizi [5,8,7,9,4,15,6]
En kucuk 4, 4 ile 5 yer degisitrir,
[2,3,4,8,7,9,5,15,6]

4. Adim,

Geriye kalan dizi [8,7,9,5,15,6]
En kucuk 5, 5 ile 8 yer degistirir,
[2,3,4,5,7,9,8,15,6]