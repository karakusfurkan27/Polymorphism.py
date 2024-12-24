## Polimorfizm Örneği - README

### Proje Açıklaması

Bu proje, Python programlamada polimorfizm kavramını göstermeyi amaçlamaktadır. Polimorfizm, bir nesnenin birden fazla formda davranmasını sağlayan bir nesne yönelimli programlama (OOP) özelliğidir. Bu örnekte, `Poligon` sınıfı temel sınıf olarak kullanılmakta ve ondan türetilen `Kare` ve `Yuvarlak` sınıfları farklı davranışlar sergilemektedir. 

### Kullanılan Sınıflar

1. **Poligon Sınıfı**:  
   - Bu sınıf, temel (super) sınıf olarak tanımlanmıştır. `render` fonksiyonu, genel bir "Poligon İşleniyor" mesajını basar.
   
   ```python
   class Poligon:
       def render(self):
           print("Poligon İşleniyor")
   ```

2. **Kare Sınıfı**:  
   - `Poligon` sınıfından türetilmiş olan bu sınıf, kendi `render` fonksiyonunu tanımlar ve "Kare işleniyor" mesajını basar.
   
   ```python
   class Kare(Poligon):
       def render(self):
           print("Kare işleniyor")
   ```

3. **Yuvarlak Sınıfı**:  
   - `Poligon` sınıfından türetilmiş başka bir sınıf olan `Yuvarlak`, yine kendi `render` fonksiyonunu tanımlar ve "Yuvarlak işleniyor" mesajını basar.
   
   ```python
   class Yuvarlak(Poligon):
       def render(self):
           print("Yuvarlak işleniyor")
   ```

### Polimorfizm

Polimorfizm, burada `Poligon` sınıfının farklı alt sınıflarında (`Kare`, `Yuvarlak`) aynı `render` fonksiyonunun farklı şekilde çalışmasını sağlamaktadır. Her bir alt sınıf, kendine özel `render` metodunu implement ederek farklı davranışlar gösterir.

### Kod Çalıştırma

Aşağıdaki örnek, polimorfizmi nasıl kullanabileceğimizi gösterir:

```python
x = Yuvarlak()
x.render()  # "Yuvarlak işleniyor" yazdırılır

y = Kare()
y.render()  # "Kare işleniyor" yazdırılır
```

Burada, `x` nesnesi `Yuvarlak` sınıfına ait ve `render` metodu çağrıldığında "Yuvarlak işleniyor" mesajı yazdırılır. Benzer şekilde, `y` nesnesi `Kare` sınıfına ait olup, "Kare işleniyor" mesajını yazdırır.

### Sonuç

Bu örnek, Python dilinde polimorfizmi kullanarak, aynı isimdeki metodun farklı sınıflarda farklı şekilde çalışmasını sağlamayı göstermektedir. Böylece, farklı sınıfların aynı temel sınıftan türemesi durumunda her birinin kendine özgü davranışlar sergilemesi mümkün olur.
