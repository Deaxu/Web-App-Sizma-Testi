# Web-App-Sizma-Testi

## 1) Sızma Testi

### Bilgilendirme

> Kendim için notlar alırken çok fazla yazı yazınca bir kaynağa dönüştüğünu fark ettim, neden insanlarla paylaşmayayım diye düşündüm ve bir repository hazırlamak istedim. Elimden geldiğince temiz hazırlamaya > > çalıştım. Bu deponun amatör biri tarafından hazırlandığını lütfen unutmayın. Bu yüzden tabi ki eksikler içerebilir.

Genel olarak hiç bir bilgiye sahip değil ve buraya ulaştıysanız muhtemelen burada bahsedilenleri kavramakta zorlanabilirsiniz. Benim de sıkça takip ettiğim sevgili Can Değer'e ait aynı zamanda içinde bir çok kaynağın da yer aldığı bir repo'ya yönlendirebilirim. Buradan bir yol haritası çıkarabilirsiniz:
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

- Wappalyzer:
Tarayıcı uzantısıdır. İncelemek için hedef siteyi ziyaret etmek yeterlidir.

![Pasted image 20231025190755](https://github.com/Deaxu/Web-App-Sizma-Testi/assets/116658892/673a59c6-ece8-4081-b3fa-8a46ac2ee4f9)

## Bilinen Dosyalar

Tarayıcı üzerinden erişebileceğiniz iyi bilinen dosyaları kontrol edin, bunlar hedefte mevcut olabilir:

- robots.txt Dosyası
-Otomatik spidering araçları robot veya bot olarak adlandırılır.
-Robotların sitede indexleyeceği sayfaları kontrol etmek amacıyla robots.txt dosyası kullanılır.
-Web uygulama sayfasının ana dizininde herkesin ulaşabileceği şekilde bulunur.
-Bu dosya sayesinde kritik dizinler bulunabilir

![image](https://github.com/Deaxu/Web-App-Sizma-Testi/assets/116658892/1bd1c5a3-898a-4dcb-953e-ac6d2ed9c63a)

- .git: Çok az sayıda web sitesi kaynak kodlarını bu uç nokta aracılığıyla yanlışlıkla ifşa edebilir. Bunu tespit ederseniz, gerçek dünyada bir P1 sorunu vardır, çünkü özel bir kaynak kodunun bu şekilde ifşa edilmesi kabul edilemez ve birçok ilginç bilgiyi açığa çıkarabilir.

## Subdomain Enumeration

Subdomain Enumeration (Alt alan adı numaralandırma) nedir?  

Alt alan adı numaralandırma, bir veya daha fazla alan adı için alt alan adları bulma işlemidir. Keşif aşamasının önemli bir parçasıdır.

 - Brute Force Enumeration
 
```
gobuster dns -t 30 -w <wordlist dosya yolu> -d x.x.x.x
```

-dns: DNS subdomain bruteforcing mode.

-d: target domain.

-t <n>: number of concurrent threads (default 10).

-w <wordlist>`: path to the wordlist.

```
amass enum -brute -w subdomains.txt -d example.com -o results.txt
```
 
-brute: Execute brute forcing after searches.

-w: Path to wordlist file.

-d: Domain names separated by commas.

-o`: Path to the text file containing terminal stdout/stderr

## Directory Bruteforce

Hedef web sitesinde gezinirken bazı dosya ve dizinleri bulabilirsiniz, ancak kullanıcı için o kadar belirgin olmayan daha gizli şeyleri bulmak için Directory Busting gibi araçları kullanabiliriz:
## Wfuzz

WFuzz, Kali Linux'ta bulunan bir komut satırı yardımcı programıdır. Web uygulamalarındaki yaygın güvenlik açıklarını fuzzing yöntemiyle keşfetmek için kullanılır. Fuzzing, herhangi bir girdinin web uygulamasını tehlikeye atıp atmadığını belirlemek için bir web uygulamasıyla bilinen birçok savunmasız girdiyi deneme kavramıdır.

``` wfuzz -c -W /usr/share/wfuzz/wordlist/dir/common.txt --hc 400,404,403 http://x.x.x.x ```

Burada -c seçeneği renkli çıktı için; -W kelime listesi için; -hc belirtilen kod/satır/kelimeler/harfler ile yanıtları gizlemek için kullanılır. Ayrıca Kali Linux'unuzda yerleşik olarak bulunur.

![Pasted image 20231102193807](https://github.com/Deaxu/Web-App-Sizma-Testi/assets/116658892/7da16147-58ce-442c-8376-fb48d2091c04)

## DirBuster

DirBuster, web / uygulama sunucularındaki dizinleri ve dosya adlarını kaba kuvvetle bulmak için tasarlanmış çok iş parçacıklı bir java uygulamasıdır. DirBuster toplam 9 farklı liste ile birlikte gelir; bu da DirBuster'ı gizli dosya ve dizinleri bulmada son derece etkili kılar.

Benzer şekilde, terminali açın ve Dirbuster yazın, ardından aşağıdaki resimde gösterildiği gibi hedef URL'yi girin ve kaba kuvvet saldırısı için /usr/share/dirbuster/wordlis/ directory-list-2-3-medium.txt dosyasına göz atın.  
  
Dir seçeneğini /dvwa ile başlatmak için seçin, aracı saldırı için yapılandırdıktan sonra başlat'a tıklayın.

![Pasted image 20231024115047](https://github.com/Deaxu/Web-App-Sizma-Testi/assets/116658892/98d0aa4a-62d5-4c3f-a0d5-b0fcd19a9250)

![Pasted image 20231024115126](https://github.com/Deaxu/Web-App-Sizma-Testi/assets/116658892/9ab4248b-8ba2-4ff8-b755-728b1d69df94)

## Port Scanning(Tarama)
### Biraz Ağ Bilgisi
#### TCP Nedir? (kaynak: https://berqnet.com/blog/port)

**TCP**; bilgisayarlar arası iletişimde veri alışverişinin yanı sıra kimlik doğrulaması da sağlayan bir port türüdür.

Açılımı **_Transmission Control Protocol_** olan [TCP,](https://berqnet.com/blog/tcp-ip) Amerika Savunma Bakanlığı tarafından bilgisayarlar arası iletişimde kaybı önlemek üzere geliştirilmiştir. Anlaşılır bir örnekle betimleyecek olursak TCP, akıllı telefonunuzdan Bluetooth, Airdrop, WhatsApp gibi bir aracı ile veri paylaşmaya benzer. Paylaşmanız gereken verileri paylaşırsınız ve telefonun kontrolü tamamen sizdedir.

Günümüzün bilgisayarlar arası iletişim protokollerinden en popüler olan HTTP, HTTPS, POP3, SSH, SMTP, TELNET ve FTP gibi protokoller TCP protokolünü kullanır ve her birinin kendine özel bir 0-65535 arası numarası bulunur.

#### UDP Nedir?

UDP; ağırlıklı olarak ses ve video iletişiminde kullanılmak üzere geliştirilmiş bir port türüdür ve açılımı User Datagram Protocol olup Türkçe’ye Kullanıcı Veri Bloğu İletişim Kuralları olarak çevrilebilir.

TCP gibi veri bütünlüğü ve kimlik doğrulaması sorumluluğu olmamasından dolayı TCP’ye göre daha hızlı olan UDP, bu özelliğinden dolayı ne kadar hızlı olsa da daha az güvenilir olduğu anlamına geldiğinden TCP’ye bir alternatif olarak değerlendirilir. Yine basit bir örnekle anlatacak olursak TCP, bir videoyu izlemek veya bir şarkıyı dinlemek için telefonunuzu arkadaşınıza vermektir. O an telefon elinizde olmadığı için arkadaşınız eğer art niyetli ise size özel olan tüm bilgilere erişebilecektir.

#### TCP ve UDP Arasındaki Farklar Nelerdir?

Yukarıda TCP ve UDP ile ilgili yapılan açıklamalarda bahsedilmiş olmakla birlikte TCP ve UDP arasındaki farkları aşağıdaki gibi özetlemek mümkündür:

- TCP, veri bütünlüğü ve kimlik doğrulaması sağladığı için UDP’ye göre biraz daha yavaştır ancak güvenilirlik açısından UDP’ten önce gelir,
- TCP, iletişim esnasında verileri paketler halinde ve sırayla gönderirken UDP’de bu yönetim akış sistemiyle sağlanır.
- TCP, bütünsel ve kayıpsız veri akışlarında tercih edilirken UDP ise ses ve video iletişiminde tercih edilir.
- 
#### Port Ne İşe Yarar?

Ne işe yaradığını tek bir cümle ile özetleyecek olursak port; **bilgisayar IP adreslerinin birden çok amaçla veri alışverişi yapabilmesini sağlayan kapılardır.**

#### En Popüler Portlar

> - 21 FTP
> - 22 SSH
> - 23 TELNET
> - 25 SMTP
> - 53 DNS
> - 80 HTTP
> - 110 POP3
> - 115 SFTP
> - 135 RPC
> - 143 IMAP
> - 194 IRC
> - 443 SSL
> - 445 SMB
> - 1433 MSSQL
> - 3306 MYSQL
> - 3389 Remote Desktop

#### HTTP Durum Kodları ve Anlamları:

https://learning.mlytics.com/the-internet/http-response-status-codes/

## Nmap 
("Network Mapper") ağ keşfi ve güvenlik denetimi için ücretsiz ve açık kaynaklı bir yardımcı programdır. Birçok sistem ve ağ yöneticisi, ağ envanteri, hizmet yükseltme programlarını yönetme ve ana bilgisayar veya hizmet çalışma süresini izleme gibi görevler için de yararlı bulmaktadır.

1) IP veya ana bilgisayara karşı Temel Nmap Taraması
```
nmap x.x.x.x
```
2) Nmap Ping Taraması
```
nmap -sp x.x.x.0/24
```
3) Yerel veya uzak bir sunucuda belirli portları veya tüm port aralıklarını tarayın
```
nmap -p 1-65535 x.x.x.x
```
```
nmap -p 80,443 x.x.x.x
```
4) Birden fazla IP adresini tarayın
```
nmap x.x.x.x y.y.y.y
```
5) En popüler portları tarayın
```
nmap --top-ports 20 x.x.x.x
```
6) Bir metin dosyasından okuyarak hostları ve IP adreslerini tarama
```
nmap -iL list.txt
```
7) Nmap tarama sonuçlarınızı bir dosyaya kaydedin
```
nmap -oN output.txt x.x.x.x
```
8) Servis/daemon sürümlerini algılama
```
nmap -sV x.x.x.x
```
9) TCP veya UDP protokollerini kullanarak tarama
```
TCP : nmap -sT x.x.x.x
```
```
UDP:  nmap -sU x.x.x.x
```
10) Nmap kullanarak CVE tespiti
CVE:  (Common Vulnerabilities and Exposures), halka açık olarak sunulan bir zafiyet sözlüğüdür.Bu sözlüğün yaratılma amacı zafiyetler hakkında yapılan bilgi paylaşımını kolaylaştırmaktır. Bir CVE kaydı, zafiyet hakkında bir açıklama, bir zafiyet kimlik numarası ve en az bir halka açık referanstan oluşur.
```
nmap -Pn --script vuln http://x.x.x.x
```
11) Uzak ana bilgisayarlardaki kötü amaçlı yazılım bulaşmalarını tespit etme
Yaygın bir kötü amaçlı yazılım taraması kullanılarak gerçekleştirilebilir:
```
nmap -sV --script=http-malware-host http://x.x.x.x
```
12) Nmap İşletim Sistemi Tespiti (-O)
```
nmap -O x.x.x.x
```
![Pasted image 20231102183843](https://github.com/Deaxu/Web-App-Sizma-Testi/assets/116658892/c5696eb7-ad8c-44d7-b52e-6a0d31dbef9b)

Soru: Bu kadar komut arasından en iyisi hangisi?
Cevap: Her durumda en iyisi sayılan bir komut yok. Her komutun farklı durumlar için üstünlüğü olabilir.

Ancak genelde yapılması gereken: 
```
nmap -sn IP > aktif_ipler.txt 
```
komutu ile aktif sunucuların tespit edilmesi ve bir dosyaya aktarılması
```
nmap -sS -sU -T4 -A -v -iL aktif_ipler.txt 
```
komutu ile TCP ve UDP portlarının taranması

## Zafiyetler 

### OWASP Top 10

OWASP Top 10 (Open Web Application Security Project) , geliştiriciler ve uygulama güvenliği uzmanları için farkındalık yaratmak amacıyla yayınlanan bir belgedir. Her yıl bir önceki yıl gerçekleştirilen atakların analizlerini yaparak geliştiricileri uyarmak ve yazılım geliştirme kültürünü değiştirmeyi amaçlamaktadır. Bu yazıda en son yayınlanan 2021 kategorisini inceleyeceğiz.

Bu repo'da açıkların nasıl bulunacağından bahsetmeyeceğim ancak öğrenebilmeniz için en iyi kaynakları sizinle paylaşacağım.


Bu kısımda bahsedilecek zafiyetler üzerine çalışmak ve nasıl bulunacağını öğrenmek için en iyi kaynak Burpsuite'in içinde laboratuvarların da bulunduğu akademisidir. 
https://portswigger.net/web-security/dashboard

#### Broken Access Control

Broken Access Control (Bozuk Erişim Kontrolü):
  
Broken Access Control, bir uygulama veya sistem hassas verilere veya işlevlere erişimi düzgün bir şekilde kısıtlayamadığında ortaya çıkan bir güvenlik açığı türüdür. Bu güvenlik açığı, saldırganların kullanıcı hesapları, dosyalar, veritabanları veya yönetim işlevleri gibi kısıtlanması gereken kaynaklara yetkisiz erişim elde etmesine olanak tanır. Broken Access Control, kötü tasarım, yapılandırma hataları veya kodlama hataları gibi çeşitli faktörler nedeniyle ortaya çıkabilir.

Erişim Kontrolü Nedir?  

Erişim kontrolü, hangi kullanıcıların veya sistemlerin belirli bir kaynağa veya sisteme erişmesine izin verildiğini kontrol etmek için kullanılan bir güvenlik mekanizmasıdır. Erişim kontrolü, bilgisayar sistemlerinde yalnızca yetkili kullanıcıların dosyalar, dizinler, veritabanları ve web sayfaları gibi kaynaklara erişebilmesini sağlamak için uygulanır. Erişim kontrolünün birincil amacı hassas verileri korumak ve bu verilere yalnızca erişim yetkisi olan kişilerin erişebilmesini sağlamaktır.

Örnek: Bir uygulama bir birincil anahtarın (primary key) değiştirilmesine izin verir ve bu anahtar başka bir kullanıcının kaydına değiştirildiğinde, o kullanıcının hesabı görüntülenebilir veya değiştirilebilir.

- Dikey erişim kontrolleri:

Dikey erişim kontrolleri, hassas işlevlere erişimi belirli kullanıcı türleriyle kısıtlayan mekanizmalardır. 

Dikey erişim kontrolleri ile farklı kullanıcı türleri farklı uygulama işlevlerine erişebilir. Örneğin, bir yönetici herhangi bir kullanıcının hesabını değiştirebilir veya silebilirken sıradan bir kullanıcının bu işlemlere erişimi olmayabilir. Dikey erişim kontrolleri, görevler ayrılığı ve en az ayrıcalık gibi iş politikalarını uygulamak için tasarlanmış güvenlik modellerinin daha ince taneli uygulamaları olabilir.

- Yatay erişim kontrolleri:

Yatay erişim kontrolleri, kaynaklara erişimi belirli kullanıcılarla kısıtlayan mekanizmalardır.  

Yatay erişim kontrolleri ile farklı kullanıcılar aynı türdeki kaynakların bir alt kümesine erişebilir. Örneğin, bir bankacılık uygulaması bir kullanıcının kendi hesaplarından işlemleri görüntülemesine ve ödeme yapmasına izin verir, ancak başka bir kullanıcının hesaplarına izin vermez.

- Context-dependent access controls (Bağlama bağlı erişim kontrolleri):

Bağlama bağlı erişim kontrolleri, uygulamanın durumuna veya kullanıcının onunla etkileşimine bağlı olarak işlevlere ve kaynaklara erişimi kısıtlar.  
  
Bağlama bağlı erişim kontrolleri, kullanıcının yanlış sırada eylem gerçekleştirmesini önler. Örneğin, bir perakende web sitesi, kullanıcıların ödeme yaptıktan sonra alışveriş sepetlerinin içeriğini değiştirmelerini engelleyebilir.
