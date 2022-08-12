## Cout
Cout komutu, konsola (ekrana) bilgi yazmak için << operatörü ile birlikte kullanılır. Ekrana yazdırılacak bilgiler çift tırnaklar arasına yazılır. Her bir c++ ifadesi noktalı virgül ile biter.

Syntax kavramını anlatırken kullandığımız programını tekrar inceleyelim.
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

Bir programa birden fazla cout komutu eklenebilir.
```
#include <iostream>
using namespace std;

int main() 
{
  cout << "Merhaba Dünya";
  cout << "Bugün hava güneşli.";
  return 0;
}

Programın Çıktısı:

Merhaba DünyaBügün Hava güneşli
```

Yukarıdaki gibi iki cout komutu ile iki bilgi yazdırdık ama aynı satırda oldu. Yeni satır eklemek için 2 yol var. Daha çok \n kullanılır.
1) \n karekterini kullanmak
2) endl manipülatörünü kullanmak



1)
```
#include <iostream>
using namespace std;

int main() 
{
  cout << "Merhaba Dünya \n";
  cout << "Bugün hava güneşli.";
  return 0;
}

Programın Çıktısı:
Merhaba Dünya
Bugün hava güneşli.
```
NOT: Peş peşe gelen iki \n karakteri boş bir satır oluşturur. Ne kadar (\n karakteri -1) o kadar boş satır oluşturur.
```
#include <iostream>
using namespace std;

int main() 
{
  cout << "Merhaba Dünya \n\n";
  cout << "Bugün hava güneşli.";
  return 0;
}

Programın Çıktısı:
Merhaba Dünya

Bugün hava güneşli.
```
NOT: Yeni satır karakterine (\n) kaçış dizisi denir ve imleci ekrandaki bir sonraki satırın başlangıcına doğru konumunu değiştirmeye zorlar. Böylece yeni bir satır oluşturulmuş olunur.



2)
```
#include <iostream>
using namespace std;

int main() 
{
  cout << "Merhaba Dünya" << endl;
  cout << "Bugün hava güneşli.";
  return 0;
}
```


