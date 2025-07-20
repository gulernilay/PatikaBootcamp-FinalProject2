# Power BI Satış Dashboardu – BEBAK Markası

## Proje Özeti

Bu Power BI dashboardu, **BEBAK** markasına ait satış ve müşteri verilerini analiz etmek, yönetime ve ilgili ekiplere içgörü sağlamak amacıyla hazırlanmıştır.

## Veri Modeli

- **kullanıcılar**: Müşteri bilgileri (isim, yaş, cinsiyet, vb.)
- **adres**: Müşterilerin şehir ve bölge bilgisi
- **ürünler**: Ürün detayları (ID, kategori, marka vb.)
- **siparis**: Sipariş ana verisi (kullanıcı, tarih, adres, toplam tutar)
- **siparisdetay**: Sipariş satırları (ürün, adet, fiyat, siparişID)
- **bölgeler**: Şehir-bölge eşleşmeleri

### İlişkiler

- ürünler[ID] → siparisdetay[ITEMID]
- kullanıcılar[ID] → siparis[USERID]
- adres[ID] → siparis[ADDRESSID]
- bölgeler[IL] → adres[CITY]

Tüm ilişkiler **tek yönlü** ve **bire-çoğa** olarak kurulmuştur.

## Dashboard Sayfaları

- **Özet**  
  Toplam satış adeti, toplam ciro, toplam müşteri ve sipariş sayısı, haftaiçi/haftasonu karşılaştırması, saatlik ve bölgesel analizler, müşteri başına ciro/adet.
- **Müşteri Perspektifi**  
  Tekil müşteri sayısı, kadın/erkek müşteri sayısı, yaş grubuna göre satışlar, İstanbul’daki top 10 müşteri tablosu.
- **Kategori Perspektifi**  
  Seçili şehir ve yaş grubunda toplam ciroyu kategorilere göre ağaç haritası (treemap).

## Filtreleme & Dinamizm
- BRAND (Marka) seçimiyle dashboard dinamik olarak filtrelenir.
- Şehir, yaş grubu ve kategori gibi ek filtreler de kullanıcıya sunulmuştur.
- Top N müşteri/kategori tabloları, ilgili filtrelere göre anlık güncellenir.

## Kullanım
- Raporu Power BI Desktop’ta açın.
- BRAND filtresinden “BEBAK” seçili olduğundan emin olun.
- Farklı filtrelerle analiz yapabilir, raporu Dosya > Dışa Aktar > PDF olarak dışa aktar seçeneğiyle PDF olarak kaydedebilirsiniz.

## Bilinen Sınırlamalar
- Dashboardda tüm ölçüler BEBAK markası odaklıdır. Diğer markalar için filtreyi güncelleyebilirsiniz.
- Büyük veri setlerinde performans için filtre kullanılması tavsiye edilir.

