# Web-App-Sizma-Testi
## 1) Sızma Testi
### Bilgilendirme

Kendim için notlar alırken çok fazla yazı yazınca bir kaynağa dönüştüğünu fark ettim, neden insanlarla paylaşmayayım diye düşündüm ve bir repository hazırlamak istedim. Elimden geldiğince temiz hazırlamaya çalıştım. Bu deponun amatör biri tarafından hazırlandığını lütfen unutmayın. Bu yüzden tabi ki eksikler içerebilir.

Genel olarak hiç bir bilgiye sahip değil ve buraya ulaştıysanız muhtemelen burada bahsedilenleri kavramakta zorlanabilirsiniz. Benim de sıkça takip ettiğim sevgili Can Değer'in, aynı zamanda içinde bir çok kaynağın da yer aldığı sizi şöyle bir repo'ya yönlendirebilirim. Buradan bir yol haritası çıkarabilirsiniz :
https://github.com/LuNiZz/siber-guvenlik-sss/blob/master/Belgeler/SikcaSorulanSorular.md#top

Bu repository'de Exploitation (istismar) aşamasına değinilmeyecektir ancak bu zafiyetlere çalışabilmeniz için kaynak paylaşacağım.

Repository'yi incelendikten sonra buraya dönün, aşağıdaki kaynaklardan devam edebilirsiniz:

İçerisinde laboratuvarların bulunduğu hem zafiyetlerin açıklandığı hem de uygulamalı olarak test edebildiğiniz site. İleride de bahsedeceğim Owasp Top 10 zafiyetlerine ek bir çok zafiyeti de içeriyor. (Bana göre en iyi kaynak):
https://portswigger.net/web-security/dashboard

İçerisinde eğitimlerin (anlatım teknikleri oldukça iyi), zafiyetli makinelerin bulunduğu başlangıç için uygun bir site. Öğrenmek istediğiniz araçları (tool) buradan daha detaylı öğrenebilirsiniz :
https://tryhackme.com/

### Sızma Testi Adımları

> 1) Kapsam Belirleme 
> 2) Bilgi Toplama
> 3) Servis Analizi 
> 4) Zafiyet Keşfi 
> 5) İstismar Etme (Exploitation)
> 6) Erişimi Koruma 
> 7) Temizleme 
> 8) Sızma Testi Raporu

### Sızma Testine Giriş

Sızma Testi Nedir? 
Bilişim Sistemleri üzerinde yer alan zafiyetleri tespit etmek amacıyla yapılan güvenlik denetimi sızma testi olarak adlandırılır.

## Sızma Testine Giriş
Sızma Testi Çeşitleri Nelerdir?

- Black Box 
-Testi yapacak kişiye çok az bilgi veya hiçbir bilgi sağlanmaz.
-Hedef, çözülmesi gereken bir kara kutu olarak görülebilir.
-Gözden kaçan uygulamalar olabilir.

- Grey Box
-Belli bilgiler dışındaki bilgiler verilmez ve testi yapan kişinin bulması beklenir.
-Bu testte bilgi toplama aşaması çok önemlidir.

- White Box 
-Kimlik bilgileri, hedef URLler, uygulama haritası bilgileri sağlanır.
-Gözden kaçan uygulama kalmaz.

## Sızma Testi Standartları
-PTES (Penetration Testing Execution Standard)
-ISSAF (Information Systems Security Assessment Framework)
-Open Source Security Testing Methodology Manual (OSSTMM)
-OWASP

## Sızma Testi Bilgi Toplama - Keşif -
- Toplanabilecek Bilgiler:
-Alan Adı Adresleri 
-Ağ Mimarisi
-Aktif Sunucular / Kişisel Bilgisayarlar 
-Açık Portlar
-Çalışan Uygulamalar ve Versiyonları
-Switch / Router gibi ağ cihazlarının listesi
-Güvenlik duvarı IP adresi

- Bilgi Toplama Yöntemleri iki kategoride sınıflandırılır:
Pasif Bilgi Toplama
Aktif Bilgi Toplama

- IP Adresi Tespiti:
ARIN, RIPE, LACNIC, AFRINIC, APNIC
Kurum, şirket ismi ile bilgi edinme 
IP adresi sorgulayarak kurum-şirket tespiti

- Alan Adı Bilgileri
WHOIS Bilgileri:
	WHOIS komutu ile hedefin alan adı kaydı sırasında verdiği bilgilere ulaşılabilir.
		whois hedef.com

  ![Pasted image 20231024151214](https://github.com/Deaxu/Web-App-Sizma-Testi/assets/116658892/62c2b898-fc30-4c0f-b565-aa85acc58904)


- IP Aralığı Bilgisi
Hedefe ait IP aralığı belirlenerek sızma testi kapsamı genişletilebilir. 
https://myip.ms/

- Google Dorking

Verilen etki alanına yönelik sonuçları filtrelemek için "site:"" operatörünü kullanın. Genel olarak, herhangi bir belirteçle, yani boşluksuz bir terimin tamamıyla eşleşir.

Arama motorlarına özel sorgu yöntemleri ile hedef hakkında bilgi elde edilir 
-Hassas dizin
-Kullanıcı giriş sayfaları

site:*.example.com

- Shodan
Arama parametreleri:
country: ülke kodu
city: şehir 
geo: koordinat 
hostname: Hostname/domain 
os: İşletim sistemine 
port: Port numarası

![Pasted image 20231024151641](https://github.com/Deaxu/Web-App-Sizma-Testi/assets/116658892/d8da199d-ee27-40ab-82ef-5e6de53ba143)


