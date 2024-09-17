[Power BI Raporunu Görüntüle]( https://app.powerbi.com/links/3SA2Tgpo78?ctid=048e1d7c-5205-48c0-88ae-7a05c05e0151&pbi_source=linkShare)

# HOTEL BOOKİNG

Veri setinde adults sütununda 5 ve üzeri değerlerde 16 kayıt hatalı bulunmuştur. Bu verileri anlamak için segmentleri, iptal durumu, agentı ve depozito durumları incelenmiştir. İnceleme sonucunda segment sütunuda iki farklı kırılım ( 'Direct', 'Ofline TA/TO'), iptal durumunda hepsinin iptal edildiği, agentta 96 numaralı agent ve NULL değer olduğu, depozito durumunda da herhangi bir depozito ödenmediği görülmüştür. Bu sonuçlar doğrultusunda veriler silinmeden, hazırlanan ölçülerde hesaplamalara dahil edilmeyerek ilerlenmiştir. 4 yetişkine kadar olan veriler normaldir.
 
Adults,Children ve Babies sütununda 0 olan, kalma süresi 1 den fazla olan ve ADR si de 0 olan veriler toplam veri setini çok fazla etkilemeyeceği için ve bu verilerle sağlıklı sonuçlar çıkarılmayacağı için silinmiştir. Fakat ADR sinde veri olan değerler bırakılmıştır. Çalışan hatalı girişi olabileceği ya da parti için gelen misafirlerden kalmaya karar verenler olabileceği ve çalışanların girişleri düzeltmediği yönünde bir sonuca varılmıştır. Yine bu verilerin City Otel içinde olduğu görülmüştür. 

Bunlar haricinde yetişkin olmadan otelde konaklayan ya da günü birlik gelen çocuklar olduğu ve bu çocukların yanında sadece iki veride bebek olduğu görünmekte, bu verilerde de ADR olduğu için ve yine çocuk-bebek yaşının veride net bir şekilde belirli olamamasından ötürü durum normal kabul edilmiştir. Ve yine bu verilerin City Otele ait olduğu sonucuna varılmıştır. 
    
Market segment sütununda tanımsız 2 veriyle karşılaşılmış olup bu verilerin distrubution channel sütunuyla karşılaştırma yapıldığında burada da tanımsız olduğu görülmüştür. Rezervasyon durumu iptal olarak gözükmektedir ancak kalınan gün verileri 0 üzeridir. Hatalı veri kabul edilip silinmiştir.
   
ADR sütunları 0 olan veriler bulunmaktadır. Gelir ile alakalı hesaplamalarda veriler silinmemiş olup sayıca fazla olduğu için hesaplamalar yapılırken ‘ >0 ‘ filtresi kullanılmıştır. ADR si 0 dan büyük fakat genel ortalamaya göre düşük veriler saptanmıştır. Bu verilerin promosyon olduğu varsayılmıştır.

Ülke harf kodları bir web sitesi üzerinden eşleme yapılarak Country Name adında bir tabloya aktarılmış olup bu tablo üzerinden ülke isimlerine çevrilmiştir.

Date tablosu oluşturulmuştur.

City Hotel, Resort Hotel, Measure olmak üzere üç farklı ölçü tablosu oluşturulmuş kullanılan ölçüler içerilerinde yer almaktadır.

## 1- Monthly Hotel Data Dashboard

![monthly](https://github.com/Kubra1s1kbozkurt/HOTEL-BOOKING-POWER-BI/blob/main/image/monthly%20and%20dashboard.png)

## 2- Hotel and Segment Dashboard

![hotel](https://github.com/Kubra1s1kbozkurt/HOTEL-BOOKING-POWER-BI/blob/main/image/hotel%20and%20segment.png)

## 3- Country and Room Type Dashboard

![country](https://github.com/Kubra1s1kbozkurt/HOTEL-BOOKING-POWER-BI/blob/main/image/country%20and%20room%20type.png)

## 4- Guest Dashboard

![guest](https://github.com/Kubra1s1kbozkurt/HOTEL-BOOKING-POWER-BI/blob/main/image/guest.png)

## Rapor

![rapor](https://github.com/Kubra1s1kbozkurt/HOTEL-BOOKING-POWER-BI/blob/main/image/analiz.png)

### İçgörü ve Analizler

Farklı ülkelerden gelen misafirlerin otel tercihi iki otel açısından da gayet tatmin edici görünmektedir. Çeşitlilik açısından City otel daha fazla farklı ülkeye ev sahipliği yapmaktadır. Bunun sebebi şehir merkezlerindeki otellerin konumu olabilir. Hem kültürel hem gezi hem de konaklama açısından avantaj sağlıyor olabilir. Gelir olarak, City ve Resort Otele ait toplam gelirin çoğunu Portekiz, Fransa, Birleşik Krallık, Almanya ve İrlanda’dan gelen misafirler karşılıyor görünmektedir. Türkiye’den giden misafirler ise küçük bir katkı sağladığı sonucuna ulaşılmıştır Toplam gelire en fazla Portekiz katkı sağlamış görünmekte olup total de 35 bin yetişkin, 2 bin çocuk konaklama sağlamıştır. Yine Portekiz’den gelen misafirlerin 3250 si tekrar otelde konaklama sağlamıştır. Toplam gelen misafirlerin içerisinde en fazla iptal oranına Portekiz sahiptir. 

Sezonluk olarak misafir sayısının artıp azaldığı saptanmıştır ve bu durum normal kabul edilmiştir. Gelir açısından en fazla getirisi olan aylar ağustos, temmuz aylarından elde edilmiştir. Doluluk oranı olarak yine ağustos, temmuz ayları ilk sıralardadır. Ancak Resort otel bağlamında şöyle bir durumla karşılaşılmıştır; eylül, ekim, kasım aylarında City Otelde düşüşte olan doluluk oranı Resort Otelde sezon doluluk oranıyla neredeyse başa baş gitmektedir. Bu durumu incelemek için ADR si kontrol edilmiş olup daha düşük oda fiyatlarına misafirlerine kapılarını açtıkları sonucuna ulaşılmıştır. En fazla iptal oranı ocak, aralık, şubat ve kasım aylarında görünmektedir. Ortalama konaklama süresi yine yaz aylarında artış göstermektedir.

A tipi oda en çok tercih edilen oda olmuştur ve toplamda 93 bin misafir bu odayı tercih etmiştir. En az tercih edilen L tipi oda olup gelire katkı olarak da L ve P tipi odalar çok küçük katkı sağlamıştır. Tekrar gelen müşteriler yine en fazla A tipi oda tercih etmiştir. 

Distrubition Chanel bağlamında en fazla müşteri getirenlerin ve gelire en fazla katkı sağlayanların Seyehat Acenteleri ve Tur Operatörleri olduğu saptanmıştır. Sonrasında direkt gelen müşterilerin ikinci sırada yer aldığı görülmüştür.

Özel istekleri fazla olan müşteri sayısının her iki otel içinde de ters orantılı olarak ilerlediği görülmektedir. İstek sayısı arttıkça müşteri sayısı azalmaktadır.

İlk kez gelen müşteri oranı City otelde daha fazla görünmektedir. Resort otel bu anlamda müşteri kazanımı açısından aksiyon almalıdır.

### Tavsiyeler

İptal oranları ile alakalı depozito ödemesi ve iptal süresi ile bir sınırlandırma getirilebilir. Müşterilerin tekrar otelleri tercih etmesi için ek indirim uygulanabilir.

Çocuklu konaklamaların az olduğu görülmüştür bunun için çocuk alanları ve aktiviteleri daha aktif sağlanabilir.

Gelire katkısı olmayan odalar  promosyon olarak yeni müşteri kazanımı için misafirlere hediye edilebilir. 

İlk kez gelen müşteri oranını artırmak adına özel teklifler ve indirimler uygulanabilir.

Tekrar gelen müşteriler için özel teklifler  ve indirimler teklif edilebilir.

Ülke bazlı hareketliliği artırmak adına ülke bazlı teklifler hazırlanabilir. Yine ülke bazlı etkinlikler, faaliyetler o ülkelerden gelen misafir sayısını artırabilir.

