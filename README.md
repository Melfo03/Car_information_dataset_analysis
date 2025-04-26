# **Car Information Analysis**
### **Proje Genel Bakış**
---
**Automobile.csv** verisini analiz ederek veri setimizdeki yakıt tüketimi, yıl, ağırlık, marka gibi değişkenler hakkında bilgiler edinip çıkarımların elde edilmesi

### Veri Kaynağı
Analiz için kullandığımız veri seti **"Automobile.csv"** dosyasıdır. Bu veri seti çeşitli araçlara  ait **beygir gücü**, **ağırlık**, **yakıt tüketimi**, **motor hacmi**, **hızlanma**, **silindir**, **menşei**, **üretim yılları** verilerini içermektedir.
- [**Veri setinin Kaggle sayfası**](https://www.kaggle.com/datasets/tawfikelmetwally/automobile-dataset)
### Veri Temizliği ve Hazırlığı
1. Veri yüklenip incelediğinde ilk olarak analizi çeşitlendirmek amacıyla name değişkeninden yeni bir **"brand"** değişkeni oluşturuldu. Bu sayede araçların markaları baz alınarak çeşitli çıkarımların yapılabilmesi sağlandı.
2. **"mpg"** değişkenindeki değerler metrik bir değer olan **"100km/l"** değerine çevirildi. Değişekenin ismi **"fuel_efficiency"** olarak değiştirildi.
3. **"displacment"** değişkenindeki değerler metrik bir değer olan **"litre"** değerine çevirildi. Değişkenin ismi **"displacement(L)"** olarak değiştirildi.
4. **"weight"** değişkenindeki değerler metrik bir değer olan **"kg"** değerine çevirildi. Değişkenin ismi **"weight(kg)"** olarak değiştirildi.
5. **"brand"** değişkenindeki **"toyouta, maxda, chevroelt, mercedes, vokswagen, vw"** gibi yanlış değerler değiştirildi.
### Keşifsel Veri Analizi (EDA)
EDA, araç verilerini keşfederek aşağıdaki soruları yanıtlamayı içeriyordu:
1. Veri setindeki araçların markalara göre yüzdelik dağılışları nasıldır?
2. Yıllara göre ortalama yakıt tüketim değerleri nasıl değişmiştir?
3. Motor hacminin yakıt tüketimi üzerindeki etkisi nasıldır?
4. Markalara göre ortalama yakıt tüketim değerleri nedir?
5. Beygir gücünün ortalama yakıt tüketimi üzerindeki etkisi nedir?
6. Markalara göre ortalama beygir gücü değerleri nedir?
7. Yıllara göre beygir gücü değerleri nasıl değişmiştir?
8. Menşei ülkelere göre ortalama yakıt tüketim değerleri nedir?
9. Menşei ülkelere göre ortalama motor hacim değerleri nedir?
10. Ağırlığın yakıt tüketimi üzerindeki etkisi nedir?
### Sonuçlar/Bulgular
#### Tanımlayıcı İstatistikler
 ![](image/desc.png) 
#### Korelasyonlar
 ![](image/corr.png) 
#### Bulgular
- Aşağıdaki grafik incelendiğinde, veri setindeki araçların çoğunluğu **Ford**markadır.
  ![](image/brand_piee.png) 

- Aşağıdaki grafik incelendiğinde, yakıt tüketim değerleri yıllar içerisinde düşüş eğilimi göstermiştir.
  
  ![](image/consumption_by_year.png) 
- Aşağıdaki grafik ve korelasyon tablomuz incelendiğinde motor hacminin yakıt tüketimi üzerinde ciddi bir etkisi vardır.
  
  ![](image/displacment_consumption_relation.png.png) 
- Aşağıdaki grafik ve veri setindeki değerler incelendiğinde, yakıt tüketim değerleri en yüksek olan araç markası **Chevrolet** iken en düşük olanı **Volkswagen** marka araçlardır.
  
  ![](image/Fuel_consumption_by_brandss.png) 
- Aşağıdaki grafik ve korelasyon tablomuz incelendiğinde beygir gücünün yakıt tüketimi üzerinde ciddi bir etkisi vardır.
  
  ![](image/horse_power_consumption_relation.png) 
- Aşağıdaki grafik ve veri setindeki değerler incelendiğinde en yüksek beygir gücüne sahip araçlar **Chrysler** markadır.
  
  ![](image/horsepower_by_brandss.png) 
- Aşağıdaki grafik incelendiğinde, yıllar içerisinde beygir gücü azalma eğilimi göstermiştir.
  
  ![](image/horsepower_by_years.png) 
- Aşağıdaki grafik incelendiğinde, ortalama yakıt tüketimi en yüksek olan menşei ülke **usa** iken en düşük olan ise **japan** olarak karşımıza çıkmıştır.
  
  ![](image/origin_consumption.png) 
- Aşağıdaki grafik incelendiğinde ortalama motor hacmi en yüksek olan menşei ülke açık ara **usa** olarak gözükmektedir.
  
  ![](image/origin_displacement.png) 
- Aşağıdaki grafik ve korelasyon tablomuz incelendiğinde, yakıt tüketimi üzerindeki en yüksek etkiyi gösteren değişken **weight(kg)** değişkenidir.
  
  ![](image/weight_consumption_relation.png.png) 
  
### Sonuç
1. **Motor Hacmi ve Yakıt Tüketimi İlişkisi:** Motor hacmi arttıkça, genel olarak yakıt tüketiminin de arttığı görülmektedir. Daha büyük motor hacimlerine sahip araçların daha fazla yakıt tükettiği söylenebilir.
2. **Beygir Gücü ve Yakıt Tüketimi İlişkisi:** Beygir gücü arttıkça, yakıt tüketiminin de arttığı gözlemlenmektedir. Daha güçlü motorlara sahip araçların daha fazla yakıt tükettiği anlaşılmaktadır.
3. **Ağırlık ve Yakıt Tüketimi İlişkisi:** Araç ağırlığı arttıkça, yakıt tüketiminin de arttığı görülmektedir. Daha ağır araçların daha fazla yakıt tükettiği sonucuna varılabilir.
4. **Menşe Ülkelere Göre Özellikler:** Menşe ülkelere göre incelendiğinde, ABD menşeli araçların daha yüksek motor hacmi, beygir gücü ve ağırlığa sahip olduğu, buna bağlı olarak da daha yüksek yakıt tükettiği gözlemlenmektedir. Avrupa ve Japonya menşeli araçlar ise daha düşük motor hacmi, beygir gücü ve ağırlığa sahip olup, daha düşük yakıt tüketimi göstermektedir.
5. **Markalar Arası Farklılıklar:** Marka bazında incelendiğinde, bazı markaların (örneğin Chevrolet, Ford, Pontiac) diğer markalara göre daha yüksek motor hacmi, beygir gücü ve ağırlığa sahip olduğu, dolayısıyla daha yüksek yakıt tükettiği görülmektedir.
6. **Yıllar İtibariyle Değişim:** Yıllar içerisinde, araçların beygir gücü ve yakıt tüketimlerinde azalma gözlemlenmektedir. Bu, teknolojik gelişmeler ve emisyon standartlarındaki iyileşmeler sayesinde daha verimli motorların üretilmesi dışında baz aldığımız 1970-1982 yılları arasındaki petrol krizleride beygir gücü ve yakıt tüketimlerinin düşmesi konusunda etkin olmuştur
7. **Korelasyon Analizi:** Korelasyon matrisi incelendiğinde, motor hacmi, beygir gücü ve ağırlık gibi özelliklerin birbiriyle yüksek oranda ilişkili olduğu, ayrıca bu özelliklerin yakıt tüketimiyle de yüksek korelasyona sahip olduğu görülmektedir.
   
**Özetle**, veri setindeki grafiklerin analizi sonucunda, motor hacmi, beygir gücü ve ağırlık gibi araç özelliklerinin yakıt tüketimi üzerinde önemli bir etkiye sahip olduğu, ayrıca menşe ülke ve marka bazında da farklılıklar olduğu ortaya çıkmaktadır.
