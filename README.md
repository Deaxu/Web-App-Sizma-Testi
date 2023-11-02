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

### Araçlar (Tools) Hakkında

Araçların bir çok özelliği ve parametreleri vardır. Bu repo'da gösterilen komutlar dışında
kullanmaya çalıştığınız aracı nasıl kullanacağınızı bilmiyorsanız:

örneğin:
```
nmap -h
```
çıktısı ile bir çok araçta olan "help" komutunu kullanarak yardım alabilirsiniz:

![Pasted image 20231024154337](https://github.com/Deaxu/Web-App-Sizma-Testi/assets/116658892/9386147f-498d-4f35-a1d1-6964f5d8d7da)

# 2) Bilgi Toplama

## Keşif

- HTML Kaynak Kodu
-Web sayfasına ait kaynak kodu görüntülenerek içinde hassas bilgi barındırıp barındırmadığı kontrol edilir.

![Pasted image 20231024152645](https://github.com/Deaxu/Web-App-Sizma-Testi/assets/116658892/884ab334-579e-4d5e-956a-1a296ad61b7f)

- GİRDİ KABUL EDEN SAYFALAR
-Web sitesinde yer alan ve girdi kabul eden veya form içeren sayfalar bulunarak bu sayfalara yönelik "kaba kuvvet", "şifre tahmini", SQL injection, Insecure Direct Object References gibi saldırı yöntemleri denenebilir.
-Kullanıcı adı ve parola kabul eden bir sayfa ise bu sayfalar taklit edilerek "Phishing" saldırılarında çalışanların kullanıcı adları ve parolaları çalınabilir. Bu sayfalarda kaba kuvvet ve sözlük saldırıları gerçekleştirilebilir.

![Pasted image 20231024152822](https://github.com/Deaxu/Web-App-Sizma-Testi/assets/116658892/916b542e-28e9-4247-a8a2-3d74333f7df2)


- PARAMETRİK URL’LER
-Kullanıcıdan girdi kabul eden sayfalar gibi, parametrik URL’ler de bulunarak bu URL’lerdeki parametrelere yönelik SQL injection, XSS, dosya ekleme gibi saldırı vektörleri düzenlenebilir.
-http://www.ornek.com/login.php?username=user1&password=sifre123 
-http://example.com/getUserProfile.jsp?item=../../../../etc/passwd 
-http://www.mysite.com/accounts/id=51741054


- HATA SAYFALARI
-Hata sayfaları saldırgana hedef sistem hakkında web sunucusu adı, yazılımı, versiyonu, kullanılan programlar, dosya yolu gibi kritik bilgiler verebilir. Hata sayfalarının kritik bilgi vermeyecek şekilde özelleştirilmesi önerilmektedir.

![Pasted image 20231024153134](https://github.com/Deaxu/Web-App-Sizma-Testi/assets/116658892/6ae9c0e1-9b9e-4325-b88d-32f80b9e5568)

# 3) Servis Analizi

## Enumaration

Keşif aşaması yalnızca belirli bir dereceye kadar güvenlik açıklarını belirlemeye yardımcı olur, ancak Numaralandırma, kullanıcılar, gruplar ve hatta sistem düzeyinde ayrıntılar - yönlendirme tabloları gibi tüm ayrıntıları öğrenmemize yardımcı olur. Etik hacking'in bu aşaması, hedef ortamda neyin test edileceğine dair uçtan uca bilgi edinmektir. Sistem üzerinde tam kontrol elde etmek için araçlar kullanılır.

## Kullanılan Web Teknolojileri

Hedef Web sitemizin hangi teknolojileri kullandığını bilmek faydalı olacaktır. Daha sonra aşağıdaki araçları kullanarak tanımlayın:  
  
- Whatweb:
```
whatweb http://x.x.x.x
```
![Pasted image 20231025191134](https://github.com/Deaxu/Web-App-Sizma-Testi/assets/116658892/228d55b9-104c-4b6c-9de8-bcc7d9323fe5)
