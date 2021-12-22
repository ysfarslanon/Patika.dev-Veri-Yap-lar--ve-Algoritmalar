# Soru

1. [22,27,16,2,18,6] -> Insertion Sort
- Yukarı verilen dizinin sort türüne göre aşamalarını yazınız.
- Big-O gösterimini yazınız.
- Time Complexity:
  - Average case: Aradığımız sayının ortada olması,
  - Worst case: Aradığımız sayının sonda olması,
  - Best case: Aradığımız sayının dizinin en başında olması.
  - Dizi sıralandıktan sonra 18 sayısı hangi case kapsamına girer? Yazınız.

2. [7,3,5,8,2,9,4,15,6] dizisinin Insertion Sort'a göre ilk 4 adımını yazınız.

## Cevap 1

### İşlem aşamaları

[22,27,16,2,18,6] n adet işlem sayısı

[2,27,16,22,18,6] n-1 adet işlem sayısı

[2,6,16,22,18,27] n-2 adet işlem sayısı

[2,6,16,18,22,27] 1 adet işlem sayısı

### Big O gösterimi

n + (n - 1) + (n - 2) + ... + 1 = (n * (n - 1)) / 2 (1 den n'e kadar olan sayıların toplamı formülü)  

Formülü açarsak: (n^2 + n ) / 2 olacaktır. Dominant olan ifade n^2 olacaktır.

Big O gösterimi de dominant ifade olacağından  O(n^2) olur.

### Time Complexity

Best Case: Sıralamak istediğimiz dizinin zaten sıralanmış olarak gelmesidir. Tekrar en küçük sayı(ları) bulmak için diziyi baştan sona doğru kontrol edeceğimiz için verilen dizinin uzunluğu kadar olacaktır.  Big O gösterimi ise O(n) olacaktır.

Worst Case : Sıralamak istediğimiz dizinin sırasız ve karışık biçimde verilme durumudur. Bu durumda dizideki küçük elemanı bulabilmek için diziyi dizi uzunluğunca(n adet) gezecektir. Daha sonra tekrar gezecektir(n-1). Bu şekilde sıralayıncaya kadar devam edecektir. n + (n - 1) + (n - 2) + ... + 1 defa olacaktır. Sonu ise (n^2 + n) / 2 olarak karşımıza çıkar bu da Big O gösteriminde O(n^2) ifadesine denk gelmektedir.

Average Case : O(n^2)

### 18 Sayısı hangi case kapsamına girmektedir

Dizi sıralandıktan sonra 18, average case kapsamındadır.

## Cevap 2

[7, 3, 5, 8, 2, 9, 4, 15, 6]

[2, 3, 5, 8, 7, 9, 4, 15, 6]

[2, 3, 4, 8, 7, 9, 5, 15, 6]

[2, 3, 4, 5, 7, 9, 8, 15, 6]

[2, 3, 4, 5, 6, 9, 8, 15, 7]

[2, 3, 4, 5, 6, 7, 8, 15, 9]

[2, 3, 4, 5, 6, 7, 8, 9, 15]
