### Referanslar (References)
1) Mevcut değişkene referans oluşturma
2) Bellekteki adresi alma

Referans değişkeni, mevcut bir değişkene bir "referans"tır ve & operatörü ile oluşturulur.
```
#include <iostream>
using namespace std;

int main() 
{
  string yiyecek = "ekmek"; //yiyecek değişkeni
  string &gıda = yiyecek; //yiyeceğin referansı

  cout << yiyecek << "\n";
  cout << gıda << "\n";
  return 0;
}

Programın Çıktısı:

ekmek
ekmek
```

Yukarıda, bir referans değişkeni oluşturmak için & operatörü kullandık. 

& operatörü ile aynı zamanda bir değişkenin bellekteki adresini (değişkenin bilgisayarın belleğinde depolandığı konumunu) almak için de kullanabiliriz.
```
#include <iostream>
using namespace std;

int main() 
{
  string yiyecek = "ekmek"; //yiyecek değişkeni

  cout << &yiyecek << "\n";
  return 0;
}

Programın Çıktısı:

0x3aef9ff670
```
NOT: Bir değişken oluşturulduğunda, değişkene bir bellek adresi atanır. Değişkene bir değer atadığımızda ise bu bellek adresine kaydedilir. Erişmek için & operatörünü kullanılır ve değişkenin nerede depolandığı gösterilir. Bellek adresleri heksadesimaldır.

NOT:Bellek adresini bilmek neden yararlıdır?

Referanslar ve Göstergeler) C++'da önemlidir, çünkü bunlar programcıya bilgisayarın belleğindeki verileri işleme yeteneği sağlar. Bu da kodu azaltabilir ve performansı arttırabilir.

Bu iki özellik, C++'ı Python ve Java gibi diğer programlama dillerinden ayıran şeylerden biridir.

### Göstergeler (Pointers)
Bir gösterge, mevcut değişkenin bellek adresini değeri olarak saklayan bir değişkendir.

Bir gösterge değişkeni, aynı türden bir veri türüne (int veya string gibi) işaret eder ve * operatörüyle oluşturulur. Yani mevcut değişkenin bellekteki adresini işaretçi değişkene atama yapar.
```
#include <iostream>
#include <string>
using namespace std;

int main() 
{
  string yiyecek = "ekmek";  // string değişkeni
  string* ptr = &yiyecek;  // yiyecek değişkeninin bellekteki adresini saklayan ptr adında bir gösterge değişkeni

  
  cout << yiyecek << "\n";  // yiyecek değişkeninin değeri

  
  cout << &yiyecek << "\n";  // yiyecek değişkenin bellekteki adresi

  
  cout << ptr << "\n";  // yiyecek değişkeninin bellekteki adresi
  return 0; 
}

Programın Çıktısı:
ekmek
0x3a7cbff670
0x3a7cbff670
```
Yıldız (asteriks) işaretini * (string* ptr) kullanarak, bir string değişkenini işaret eden ptr adında bir işaretçi değişkeni oluşturduk. Göstergenin türünün mevcut değişkenin türüyle aynı olması gerektiğini unutmayın.

yiyecek değişkenin bellek adresini saklamak için & operatörünü kullandık ve bunu göstergeye atadık.

Böylece ptr gösterge değişkeni, yiyeceğin bellek adresini tutar.

NOT: Göstergeyi bildirmenin 3 yolu vardır (genelde 1. Tercih edilir.):

 string* string1; 
 
 string *string1;
  
 string * string1;


Yukarıda, bir değişkenin bellek adresini almak için gösterge değişkenini kullandık. 

Aynı zamanda * operatörünü dereferans (değişkenin değerini almak) için göstergeyi de kullanabiliriz.
```
#include <iostream>
using namespace std;

int main() 
{
  string yiyecek = "ekmek";  // string değişkeni
  string* ptr = &yiyecek;  // yiyecek değişkeninin bellekteki adresini saklayan ptr adında bir gösterge değişkeni
  
  cout << ptr << "\n";  // yiyecek değişkeninin bellekteki adresi

  cout << *ptr << "\n";  // yiyecek değişkeninin değeri
  return 0; 
}

Programın Çıktısı:

0xd14ddff610
ekmek
```
Not: * işareti burada kafa karıştırıcı olabilir kısaca: 

Atama (string* ptr) yapıldığında, bir gösterge değişkeni oluşturuluyor.

Atamada kullanılmadığında, dereferans operatörü olarak işlev görüyor.





Göstergenin değerine yeni değer atama
```
#include <iostream>
using namespace std;

int main() 
{
  string yiyecek = "ekmek";  // string değişkeni
  string* ptr = &yiyecek;  // yiyecek değişkeninin bellekteki adresini saklayan ptr adında bir gösterge değişkeni

  cout << yiyecek << "\n";  //yiyecek değişkeninin değeri

  cout << &yiyecek << "\n";  //yiyecek değişkenimin bellekteki adresi

  cout << ptr << "\n";  // yiyecek değişkeninin bellekteki adresi

  cout << *ptr << "\n\n";  // yiyecek değişkeninin değeri

  *ptr= "simit";  //göstergenin değerine başka değer atama

  cout << *ptr << "\n";  // yiyeceğin değişkeninin yeni değeri

  cout << yiyecek << "\n";  //yiyeceğin değişkeninin yeni değeri
  return 0; 
}

Programın Çıktısı:

ekmek
0xde603ffb90
0xde603ffb90
ekmek

simit
simit
```


