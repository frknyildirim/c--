## Değişkenler (Variables)
Değişken, bellekte (RAM-Random Access Memory) kendisine bir isim verilen ve bir değer taşıyan (tutan, depolayan) veri yapısıdır.
C++ dilinde birden fazla değişken türleri vardır. Bu değişken türleri farklı anahtar sözcüklerle tanımlanırlar.

int - 123 veya -123 gibi tam sayıları ondalık olmadan saklar.

double - kayan noktalı sayıları 19.99 veya -19,99 gibi ondalık sayılarla saklar.

float -

char - 'a' veya 'B' gibi tek karakterleri saklar. Karakter değerleri tek tırnak içine alınır.

string - "Merhaba Dünya" gibi metinleri saklar. Dize değerleri çift tırnak içine alınır.

bool - değerleri iki durumla depolar: true veya false

### Değişkene Değer Atama ve Yazdırma
C++ dilinde, eşit sembolü(=)  atama sembolüdür.

Genel gösterimi:           Değişken türü    Değişken=İfade;  

Örnek gösterimi:           int   c=(f-32)/1.8;

Sağ taraftaki ifade, C++’da geçerli herhangi bir ifade olabilir.

Atama deyiminin çalışma prensibi şu şekildedir: 
“Sağ taraftaki ifadenin değerini hesapla! Bulduğun sonucu sol taraftaki değişkenin lokasyonuna yerleştir!”

Değişkeni oluşturup peşinden değeri atanabilir veya değişkeni oluşturup daha sonra bu değişkene değer atanabilir. Değişkeni ekrana yazdırmak için de cout komutu ve << operatörü kullanılabilir.
```
#include <iostream>
using namespace std;

int main() 
{
  int sayı=10;
  cout<<sayı;
  return 0;
}

Programın Çıktısı:
10
```

Aynı türden birden fazla değişkene değer ataması için değişkenler arasına virgül konularak atanabilir.
```
#include <iostream>
using namespace std;

int main() 
{
  int x = 5, y = 6, z = 50;  
  cout << x + y + z;
  return 0;
}

Programın Çıktısı:
61
```
Bir satırda, aynı değer birden fazla değişkene atanabilir.
```
#include <iostream>
using namespace std;

int main() 
{
  int x, y, z;
  x = y = z = 50;
  cout << x + y + z;
  return 0;
}

Programın Çıktısı:
150
```
Değişkenler adı üstünde değişkendir ve program içinde değeri değişebilmektedir. Mevcut bir değişkene yeni bir değer atanırsa eski değerin üzerine yazılır yani eski değer silinir.
```
#include <iostream>
using namespace std;

int main() 
{
  int sayı=10;
  sayı=23;
  cout<<sayı;
  return 0;
}

Programın Çıktısı:
23
```

### Diğer Değişken türlerine değer atama ve yazdırma 
```
#include <iostream>
using namespace std;

int main() 
{
  int sayı = 10;               
  double floatsayi= 23.22;    
  char karakter = 'F';         
  string metin = "Dünya";     
  bool boolean = true;    

  cout<<sayı<<"\n";
  cout<<floatsayi<<"\n";
  cout<<karakter<<"\n";
  cout<<metin<<"\n";
  cout<<boolean<<"\n";
  return 0;
}

Programın Çıktısı:
10
23.22
F
Dünya
1
```

### Tanımlayıcılar (Identifiers)
Tüm değişkenler benzersiz isimlerle tanımlanmalıdır.
Bu benzersiz adlara “tanımlayıcılar” denir.
Tanımlayıcılar kısa adlar (x, y, z vs.) veya daha açıklayıcı adlar (yaş, toplam, çevre, alan vs.) olabilir.
Yazılan kodun, hem kendinizin hem de başka kod okuyucularının koda baktığında daha iyi anlaması için daha açıklayıcı adların kullanılması tavsiye edilmektedir.
```
#include <iostream>
using namespace std;

int main() 
{
  int x=15;
  //yukarıdaki gibi tanımlamak yerine aşağıdaki gibi tanımlamak daha iyi olacaktır.
  int kısaKenar=15;
  return 0;
}
```


**C++’da değişkenlere isim verirken aşağıdaki kurallara uyulmalıdır.
1.	Alt tire (_) veya harf ile başlar. ad, _yas
2.	Harf, alt tire veya sayıları içerir. Ad, sayi1, ad_soyad
3.	Özel karakterleri (!, #, %, vb. ) içeremez. 
4.	Boşluk içeremez.
5.	Program tarafından kullanılan rezerve kelimeleri (int, return vs. gibi) içeremez.
6.	C++ büyük küçük harf duyarlıdır. Yani İSİM ve isim farklı değişken isimleridir.

