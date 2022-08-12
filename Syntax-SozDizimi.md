###Syntax (Söz Dizimi): 
Bir dilin kendine özgü yazım kurallarına “Syntax” denir. Her dilin kendine özgü Syntax’ı vardır. Cümleyi oluşturan kelime türlerinin sistematik ve anlamlı bir cümle olması için Syntax’a uygun cümle kurulumu yapılır. Bu kavram yazılım dillerinde ise daha da önem kazanır.


Basit bir C++ programı

```
#include <iostream>
using namespace std;

int main()
{
     cout << "Merhaba Dünya";
     return 0;
}

Programın çıktısı:

Merhaba Dünya
```


Yukarıdaki basit programın kodlarının ne anlama geldiğine yani c++ dilinin Syntax’ına bakalım.

Satır 1: #include <iostream>  giriş çıkış komutlarını içeren bir kütüphanedir. Daha detaylı bakacağız. (Header file library nedir, komut yerine giriş ve çıkış nesnesi mi yazmalıyım?)

Satır 2: using namespace std; std alan adını her defasında yazmamak için yoksa std:cout şeklinde yazılır.

Satır 3: Boş satırdır. Boş satırlar derleyici tarafından yok sayılır. Sadece yazdığımız kodu daha okunabilir hale getirmek için kullanırız.

Satır 4: int main() c++ ana fonksiyonu yani fonksiyonlar fonksiyonu diyebiliriz. Bir programda birden fazla fonksiyon olabilir ama ana fonksiyon main fonksiyonudur. Ana program gövdesi int main ile başlar. Daha detaylı bakacağız.

Satır 5: { fonksiyon başlangıcıdır. Kodlar bu iki köşeli parantez içine yazılır.

Satır 6: cout << "Merhaba Dünya"; konsola (ekrana) bilgi yazmak için cout komutu ile << operatörü birlikte kullanılır. Ekrana yazdırılacak bilgiler çift tırnaklar arasına yazılır. Her bir c++ ifadesi noktalı virgül ile biter. (Komut yerine nesne mi demeliyim?)

Satır 7: return 0; //



Satır8: } fonksiyonun bitişi

Not1: programın gövdesi bu şekilde de yazılabilirdi ama elbette okunması ve anlaşılması daha zorlaşacaktı. int main () {cout << "Merbaha Dünya"; return 0;} 

  
Örnekler
```
#include <iostream>
using namespace std;
int main()
{
	int a = 10, b = 5, c = 32;
	cout << "islem sonucu=" << a * b / c << endl;
       system("pause");
}
Programın Çıktısı:
islem sonucu=1

```

```
#include <iostream>
using namespace std;
int main()
{
	char t = 'c';
	t = t + 5;
	cout << "islem sonucu=" << t << endl;
	system("pause");
}
Programın Çıktısı: 
islem sonucu=h
```
Şimdiye kadar cout komutu ile konsola bir şeyler yazdırdık. Şimdi sıra konsoldan bilgi almakta. Cin komutu ile konsola girilen bilgileri alabiliriz. Cin komutunda sonra >> şeklinde ters yönde olur.

```
#include <iostream>
using namespace std;
int main()
{
	int x;
	cout << "x değişkeni için bir tam sayı giriniz:" << endl;
	cin >> x;
	cout << "girdiğiniz x değişkeni=" << x << endl;
	system("pause");
}
Programın Çıktısı:
X değişkeni için bir tam sayı giriniz:
40
Girdiğiniz x değişkeni=40
```
```  
       #include <iostream>
using namespace std;
int main()
{
	int x=5;
	cout << "ilk x=" << x << endl;
	cout << "x++=" << x++ << endl; 
	cout << "yeni x=" << x << endl;
	cout << "++x=" << ++x << endl;
	cout << "yeni x=" << x << endl;
	cout << "x--=" << x-- << endl;
	cout << "yeni x=" << x << endl;
	cout << "--x=" << --x << endl;
	cout << "yeni x=" << x << endl;
	system("pause");
}
Programın Çıktısı:
ilk x=5
x++=5
yeni x=6
++x=7
yeni x=7
x--=7
yeni x=6
--x=5
yeni x=5
```

