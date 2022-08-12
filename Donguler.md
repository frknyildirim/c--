### while döngüsü
while döngüsü, belirtilen koşul doğru olduğu sürece kod bloğunu dolaşır.

while (koşul) 

{

  // yürütülecek kod bloğu
  
}
```
#include <iostream>
using namespace std;

int main() 
{
  int i = 0;
  while (i < 5) 
  {
    cout << i << "\n";
    i++;  //  i değişkenini 1 arttırıyoruz eğer arttırmazsak döngü sonlanmaz.
  }
  return 0;
}

Programın Çıktısı:

0
1
2
3
4
```

### do/while döngüsü
do/while döngüsü, while döngüsünün bir çeşididir. Bu döngü, koşulun doğru olup olmadığını kontrol etmeden önce kod bloğunu bir kez çalıştırır, ardından koşul doğru olduğu sürece döngüyü tekrarlar.

do 

{

  // yürütülecek kod bloğu
  
}

while (koşul);

```
#include <iostream>
using namespace std;

int main() 
{
  int i = 0;
  do 
  {
    cout << i << "\n";
    i++;
  }
  while (i < 5);
  return 0;
}

Programın Çıktısı:
0
1
2
3
4
```

NOT: eğer koşulu (i<0) yapsaydık koşul doğru olmadığı halde yine de kod bloğu 1 kez çalışırdı programın çıktısı 0 olurdu.

### for döngüsü

for (ifade 1; ifade 2; ifade 3) 

{

  // yürütülecek kod bloğu
  
}

İfade 1, kod bloğunun yürütülmesinden önce (bir kez) yürütülür ve başlangıç değerini tanımlar.

İfade 2, kod bloğunun yürütülmesi için koşulu (bitiş değeri) tanımlar.

İfade 3, Kod bloğu yürütüldükten sonra (her seferinde) yürütülür ve artım veya azalım değerini tanımlar.


```
#include <iostream>
using namespace std;

int main() 
{
  for (int i = 0; i < 5; i++) 
  {
    cout << i << "\n";
  }
  return 0;
}

Programın Çıktısı:
0
1
2
3
4
```


