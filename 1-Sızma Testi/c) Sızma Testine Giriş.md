
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
	![[Pasted image 20231024151214.png]]

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

![[Pasted image 20231024151641.png]]
