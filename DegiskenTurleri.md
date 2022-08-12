## Veri Türleri (Değişken Türleri)
Değişkenlerin veri tipi (değişkenin türü) olmalıdır.
Veri türü, değişkenin depolayacağı bilgilerin boyutunu ve türünü belirtir.

Bazı veri türleri verilmiştir.
```
#include <iostream>
using namespace std;

int main() 
{
  int tamSayı = 5; //Tamsayı
  float floatSayı = 5.99; //
  double doubleSayı = 9.98; // 
  char karakter = 'D'; // Karakter
  bool boolean = true; // Boolean
  string metin = "Merhaba"; // karakter dizisi
  return 0;
}
```

 ![image](https://user-images.githubusercontent.com/111071776/184286650-4ec1693e-e370-400e-9a66-be3258e2a0cf.png)

Data type: veri türü

Size: boyut

Description: açıklama



Kayan noktalı sayı 10 nun kuvvetini belirtmek için “e” ile gösterilen bilimsel sayı da olabilir.
```
#include <iostream>
using namespace std;
 
int main () 
{
  float sayı1 = 35e3;
  double sayı2 = 12E4;
  cout << sayı1 << "\n";
  cout << sayı2;
  return 0;
}

Programın Çıktısı:

35000
120000
```

### Boolean
Bir boolean veri türü, bool anahtar sözcüğüyle bildirilir.
Boolean veri türü yalnızca true veya false değerlerini alabilir.

Değer döndürüldüğünde true = 1 ve false = 0 olur.
```
#include <iostream>
using namespace std;

int main() 
{
  bool durum1 = true;
  bool durum2 = false;
  cout << durum1 << "\n";
  cout << durum2;
  return 0;
}

Programın Çıktısı:

1
0
```


Bir ifadenin veya bir değişkenin doğru olup olmadığını öğrenmek için kullanılabilir.
```
#include <iostream>
using namespace std;

int main() 
{
  int a = 20;
  int b = 10;
  cout << (a < b);
  return 0;
}

Programın Çıktısı:

0
```



### Characters (Karakter)
Char veri türü, tek bir karakteri depolamak için kullanılır. 
Karakter, 'A' veya 'c' gibi tek tırnak içine alınmalıdır.

``` 
#include <iostream>
using namespace std;
 
int main () 
{
  char harf = 'B';
  cout << harf;
  return 0;
}

Programın Çıktısı:

B
```

NOT: Aynı zamanda belirli karakterleri görüntülemek için ASCII değerleri kullanılabilir.
```
#include <iostream>
using namespace std;
 
int main () 
{
  char a = 65, b = 66, c = 67;
  cout << a;
  cout << b;
  cout << c;
  return 0;
}

Programın Çıktısı:

ABC
```

ASCII (American Standard Code for Information Interchange)Tablosu
![image](https://user-images.githubusercontent.com/111071776/184287420-c2580809-c6b2-4aa0-816f-8f475f65fb73.png)

ASCII (Bilgi Değişimi için Amerikan Standart Kodu), 0 ile 127 arasında değerlere sahip 7 bitlik bir karakter kodudur. ASCII kodu, UTF-8 kodunun bir alt kümesidir. ASCII kodu, kontrol karakterlerini ve yazdırılabilir karakterleri içerir: digits, büyük harfler ve küçük harfler.
 
### Strings (Karakter Dizileri)
Dize türü, bir karakter dizisi (metin) depolamak için kullanılır. Bu yerleşik bir tür değildir, ancak en temel kullanımında bir tür gibi davranır. Dize değerleri çift tırnak içine alınmalıdır:
```
#include <iostream>
using namespace std;

int main() 
{
  string string1 = "Merhaba";
  cout << string1;
  return 0;
}

Programın Çıktısı:

Merhaba
```

Stringleri kullanmak için kaynak koduna ek bir başlık dosyası eklenmelidir. <string> kütüphanesi eklenmelidir.
  ```
#include <iostream>
#include <string>
using namespace std;

int main() 
{
  string string1 = "Merhaba";
  cout << string1;
  return 0;
}

Programın Çıktısı:

Merhaba
```



### String Birleştirme
```
#include <iostream>
using namespace std;
 
int main () {
  string isim = "Mehmet ";
  string soyisim = "Gündoğan";
  string tamisim = isim + soyisim;
  cout << tamisim;
  return 0;
}

Programın Çıktısı:

Mehmet Gündoğan
```

Yukarıdaki programdaki gibi isim ve soyisim arasında bir boşluk oluşturmak için isim değişkeninden sonra bir boşluk ekledik. Diğer alternatif olarak çift tırnak veya tek tırnak içeren bir boşlukta ekleyebilirdik.
  ```
#include <iostream>
using namespace std;
 
int main () {
  string isim = "Mehmet";
  string soyisim = "Gündoğan";
  string tamisim = isim + " " + soyisim;
  cout << tamisim;
  return 0;
}

Programın Çıktısı:

Mehmet Gündoğan
```



Stringler üzerinde belirli işlemler yapmayı sağlayan fonksiyonlar vardır.

Append() fonksiyonu ile stringleri birleştirebiliriz.
  ```
#include <iostream>
using namespace std;
 
int main () {
  string isim = "Mehmet ";
  string soyisim = "Gündoğan";
  string tamisim = isim.append(soyisim);
  cout << tamisim;
  return 0;
}

Programın Çıktısı:

Mehmet Gündoğan
```
  
Bir stringin uzunluğunu bulmak için length() veya size () fonksiyonu kullanılabilir.
  ```
#include <iostream>
using namespace std;

int main() 
{
  string alfabe = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
  cout << "alfabenin uzunluğu: " << alfabe.length();
  cout << "\nalfabenin uzunluğu: " << alfabe.size();
  return 0;
}

Programın Çıktısı:

Alfabenin uzunluğu: 26
Alfabenin uzunluğu: 26
```





Bir stringin karakterlerine erişmek için [ ] köşeli parantez kullanılabilir. 
  
NOT: Stringin Karakterleri 0 ile başlar. [0] ilk karakter demektir. [1] ise 2. Karakterdir vs.
  ```
#include <iostream>
using namespace std;

int main() 
{
  string stringx = "Merhaba";
  cout << stringx[0] << "\n";
  cout << stringx[1];
  return 0;
}

Programın Çıktısı:

M
e
```
  
Stringin karaktelerini değiştirmek için stringin karakter numarasına tek tırnak içinde karakter ataması yapılır.
  ```
#include <iostream>
using namespace std;

int main() 
{
  string stringx = "Merhaba";
  stringx[0] = 'S';
  cout << stringx;
  return 0;
}

Programın Çıktısı:

Serhaba
```



Stringi klavyeden kullanıcı girdisi ile almak için cin komutu ile >> operatörü birlikte kullanılır.
  ```
#include <iostream>
using namespace std;

int main() 
{
  string isim;
  cout << "ismini giriniz: ";
  cin >> isim;
  cout << "isminiz: " << isim;
  return 0;
}

Programın Çıktısı:

İsminizi giriniz: Göktuğ
İsminiz: Göktuğ
```
  
Cin komutu ve >> operatörü ile yalnızca tek bir kelimeyi kullanıcıdan alabilirsiniz çok fazla kelime yazsanız bile. Çünkü cin komutu bir boşluğu (boşluk, tab tuşlarını) sonlandırma olarak kabul eder.
  
Bu yüzden kullanıcıdan birden fazla girdi kelimesi almak için getline() fonksiyonu tercih edilir.
  ```
#include <iostream>
using namespace std;

int main() 
{
  string tamisim;
  cout << "isminizi ve soyisminizi aralarında bir boşluk bırakarak giriniz: ";
  getline(cin,tamisim);
  cout << "isminiz ve soyisminiz: " << tamisim;
  return 0;
}

Programın Çıktısı:

İsminizi ve soyisminizi aralarında bir boşluk bırakarak giriniz: Göktuğ Yücel
İsminiz ve soyisminiz: Göktuğ Yücel
```


