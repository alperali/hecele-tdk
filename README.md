# Türkçe Heceleme - TDK
Türk Dil Kurumunun [sitesinde belirttiği kurallara](https://www.tdk.gov.tr/icerik/yazim-kurallari/hece-yapisi-ve-satir-sonunda-kelimelerin-bolunmesi/) göre heceleme yapan bir uygulamadır.

## Kurallar
Kurum, üç adet kural belirtmiştir:
1. Türkçede kelime içinde iki ünlü arasındaki ünsüz, kendinden sonraki ünlüyle hece kurar: _a-ra-ba, bi-çi-mi-ne, in-sa-nın, ka-ra-ca_ vb.
2. Kelime içinde yan yana gelen iki ünsüzden ilki kendinden önceki ünlüyle, ikincisi kendinden sonraki ünlüyle hece kurar: _al-dı, bir-lik, sev-mek_ vb.
3. Kelime içinde yan yana gelen üç ünsüz harften ilk ikisi kendinden önceki ünlüyle, üçüncüsü kendinden sonraki ünlüyle hece kurar: _alt-lık, Türk-çe, kork-mak_ vb.

### Analiz
Kuralların girmediği detaylar var. Bu detayları kendimiz doldurmak durumundayız.
1. **Sözcüğe baştan mı yoksa sondan mı bakılarak heceler kurulacak? Belli değil.**  
   Kurallar bir tür kümeleme (_clustering_) tekniği ima etmektedir. Halbuki bilgisayarda metinler _string_ olarak tutulur, yani kümeli değil sıralı (_sequential_) bir veri yapısıdır, iteratif işlenirler. Kümeleyici anlatımı bu yapıya uyarlamak durumundayız.
   Baştan veya sondan fark etmez. Baştan yani okuma yönünde giderek heceleme yapan bir çözüm olsun.
   
1. **“Hece yapar” demek, “hecedir” demek değil.**  
   _Somurtkan_ sözcüğünü ele alalım. Birinci kurala göre **m** harfi **u** ile hece yapar, ancak **-mu** doğru hece değildir.
   Üçünü kurala göre **rt** de **u** ile hece yapar. Bu ikisi birleştirilecek ve nihai **-murt** hecesi saptanacak. Yani iki adımda bir hece bulundu.
   Fakat _a-ra-ba_ örneğinde bu durum yok, tek adımda hece bulunuyor.
   
1. **Ünlüler arasında olmayan ünsüz nasıl işlenecek?**  
   Sözcük başında ve sonunda bulunan ünsüzler hiçbir kurala uymuyor. Bunlar kendine en yakın heceye eklemlenecek gibi kabul ediyoruz.
   
1. **Ünsüzler arasında olmayan ünlü (yanyana iki ünlü) nasıl işlenecek?**  
   _Kaide_ sözcüğünü ele alalım. Hiçbir kurala uymadığı için **K** harfini atladık. **d** harfi birinci kurala göre **e** ile hece yaptı.
   Geriye kalan **Kai** hangi kurala göre hecelenecek? Benzer durum **fiil**, **şiir**, **nail** gibi sözcüklerde de var: hiçbir kurala uymadıkları için baştaki ve sondaki ünsüzleri atladık, geriye yanyana iki ünlü kaldı, hangi kurala göre heceleme yapılacak?
