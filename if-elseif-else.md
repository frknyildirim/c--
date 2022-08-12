### if
Bir koşul doğru olduğunda yürütülecek kod ve kod bloğunu belirtmek için if kullanılabilir.

if (koşul) 

{

  // koşul doğruysa yürütülecek kod bloğu
  
}

Örnek1:
```
#include <iostream>
using namespace std;

int main() 
{
  if (23 > 17) {
    cout << "23 sayısı 17'den daha büyüktür.";
  }  
  return 0;
}

Programın Çıktısı:

23 sayısı 17’den daha büyüktür.
```

Örnek2:
```
#include <iostream>
using namespace std;

int main() 
{
  int x = 20;
  int y = 18;
  if (x > y) 
  {
    cout << "x değişkeni y'den daha büyüktür.";
  }  
  return 0;
}

Programın Çıktısı:

X değişkeni y’den daha büyüktür.
```

### Else
Koşul veya koşullar yanlışsa yürütecek kod veya kod bloğunu belirtmek için kullanılabilir.

if (koşul) 

{

  // koşul doğru ise yürütülecek kod bloğu
  
}

else 

{

  // koşul yanlış ise yürütülecek kod bloğu
  
}

Örnek1:
```
#include <iostream>
using namespace std;

int main() 
{
  int notum = 85;
  if (notum < 50) 
  {
    cout << "başarısız.";
  } 
  else 
  {
    cout << "başarılı.";
  }
  return 0;
}

Programın Çıktısı:

Başarılı
```

### else if
Bir koşul yanlış ise başka bir koşul doğru olduğunda yürütülecek kod veya kod bloğunu belirtmek için kullanılabilir.

if (koşul1)

{

  // koşul1 doğru olduğunda yürütülecek kod bloğu
  
} 

else if (koşul2) 

{

  // koşul1 yanlış ve koşul2 doğru olduğunda yürütülecek kod bloğu
  
}

else

{

  // koşul1 yanlış ve koşul2 yanlış olduğunda yürütülecek kod bloğu
  
}


Örnek1:
```
#include <iostream>
using namespace std;

int main() 
{
int notum = 85;
if (notum <50) 
{
  cout << "Daha fazla çalışmalısın.";
} 
else if (notum < 85) 
{
  cout << "İyisin.";
}
else 
{
  cout << "Çok iyisin.";
}
return 0;
}

Programın Çıktısı:

Çok iyisin.
```


NOT: program koşulları yukarıdan aşağıya doğru koşulların doğru veya yanlış olduğuna karar verdiği için önce hangi koşul doğru ise o ifadenin ilgili kod veya kod bloğunu yürütür.

NOT: Mutlaka 1. İfade “if” olmalıdır. 1. İfade “else if” olamaz.

NOT: if, if, if…, else basamak yapısı şeklinde ise else hariç her ifadeye istisnasız bakılır ve doğruysa yürütülür.

NOT: if, else if, else if…, else basamak yapısı şeklinde ise her ifadeye bakılmayabilir. if doğru ise sadece o yürütülür ve diğerlerine bakılmaz . Eğer if doğru değil ise ilk else if ifadelerinden doğru olan yürütülür ve diğerlerine bakılmaz. Ancak if ve else if ifadelerinden hiçbiri doğru değil ise else yürütülür.

Kısaca: Eğer 1. İfade doğru değil ise else if ifadelerinden doğru olan koşul varsa o ifadenin ilgili kod veya kod bloğunu yürütür. Altındaki diğer else if ifadelerin koşulları doğru olsa bile değerlendirmeye tutulmaz ve yürütülmez. 
Ancak bir if yerine birden fazla if ifadesi kullanılırsa 1. İf ifade doğru olsa bile diğer if ifadelerinin koşullarına bakılır.

NOT: basamak yapısını if, else if, if, if…, else vs. gibi düzensiz bir basamak yapıları yapılırsa da program hata vermez ve üstteki kurallar çerçevesinde yürütülür. Tabii ki düzenli ve anlaşılması kolay olan bir kod yapısı olmaz.

NOT: basamak yapısında else ifadesi olmadan da olabilir ama genelde kullanılır. Kullanım yerine göre tercih değişebilir.


### İf- else kısa gösterim (üçlü operatör)
Üç oluştuğu için üçlü operatör denir. Birden çok kod satırını tek bir kod satırı ile değiştirmek için kullanılabilir. Genellikle basit if else ifadelerini değiştirmek için kullanılır.

değişken = koşul ? doğruİfade : yanlışİfade;

```
#include <iostream>
using namespace std;

int main() 
{
  int notum = 90;
  if( notum > 50) 
  { 
    cout << "başarılısın.";
  }
  else
  {
    cout << "başarısızsın.";
  }
  return 0;
}

Programın Çıktısı:

Başarılısın.
```
Yukarıdaki programın aynısını daha kısa şekilde üçlü operatör ile gösterdik.
```
#include <iostream>
using namespace std;

int main() 
{
  int notum = 90;
  string sonuç = notum > 50 ? "başarılısın." : "başarısızsın.";
  cout << sonuç;
  return 0;
}

Programın Çıktısı:

Başarılısın.
```


NOT: Birden fazla koşul gerekirse aşağıdakinin benzeri gibi yapılabilir, daha da koşul eklenilebilir. Ancak gittikçe kodun okunuşu zorlaşacaktır.
```
#include <iostream>
using namespace std;

int main() {
  int notum = 70;
  string sonuç = notum < 50 ? "daha fazla çalışmalısın." : notum <85 ? "iyisin." : "çok iyisin";
  cout << sonuç;
  return 0;
}

Programın Çıktısı:

İyisin
```
NOT: İstenilirse koşulu ve istenilen ifadeleri () içine alabiliriz böylece kodun okunuşu kolaylaşabilir.
```
#include <iostream>
using namespace std;

int main() {
  int notum = 70;
  string sonuç = (notum < 50) ? "daha fazla çalışmalısın." : (notum <85 ? "iyisin." : "çok iyisin");
  cout << sonuç;
  return 0;
}

Programın Çıktısı:

İyisin
```



