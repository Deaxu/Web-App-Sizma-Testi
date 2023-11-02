Nmap ("Network Mapper") ağ keşfi ve güvenlik denetimi için ücretsiz ve açık kaynaklı bir yardımcı programdır. Birçok sistem ve ağ yöneticisi, ağ envanteri, hizmet yükseltme programlarını yönetme ve ana bilgisayar veya hizmet çalışma süresini izleme gibi görevler için de yararlı bulmaktadır.

1) IP veya ana bilgisayara karşı Temel Nmap Taraması
- nmap x.x.x.x

2) Nmap Ping Taraması
- nmap -sp x.x.x.0/24

3) Yerel veya uzak bir sunucuda belirli portları veya tüm port aralıklarını tarayın
- nmap -p 1-65535 x.x.x.x
- nmap -p 80,443 x.x.x.x

4) Birden fazla IP adresini tarayın
- nmap x.x.x.x y.y.y.y

5) En popüler portları tarayın
- nmap --top-ports 20 x.x.x.x

6) Bir metin dosyasından okuyarak hostları ve IP adreslerini tarama
- nmap -iL list.txt

7) Nmap tarama sonuçlarınızı bir dosyaya kaydedin
- nmap -oN output.txt x.x.x.x

8) Servis/daemon sürümlerini algılama
- nmap -sV x.x.x.x

9) TCP veya UDP protokollerini kullanarak tarama
- TCP : nmap -sT x.x.x.x
- UDP:  nmap -sU x.x.x.x

10) Nmap kullanarak CVE tespiti
CVE:  (Common Vulnerabilities and Exposures), halka açık olarak sunulan bir zafiyet sözlüğüdür.Bu sözlüğün yaratılma amacı zafiyetler hakkında yapılan bilgi paylaşımını kolaylaştırmaktır. Bir CVE kaydı, zafiyet hakkında bir açıklama, bir zafiyet kimlik numarası ve en az bir halka açık referanstan oluşur.

- nmap -Pn --script vuln http://x.x.x.x

11) Uzak ana bilgisayarlardaki kötü amaçlı yazılım bulaşmalarını tespit etme
Yaygın bir kötü amaçlı yazılım taraması kullanılarak gerçekleştirilebilir:  
- nmap -sV --script=http-malware-host http://x.x.x.x

12) Nmap İşletim Sistemi Tespiti (-O)

- nmap -O x.x.x.x

![[Pasted image 20231102183843.png]]

Soru: Bu kadar komut arasından en iyisi hangisi?
Cevap: Her durumda en iyisi sayılan bir komut yok. Her komutun farklı durumlar için üstünlüğü olabilir.

Ancak genelde yapılması gereken: 
nmap -sn IP > aktif_ipler.txt komutu ile aktif sunucuların tespit edilmesi ve bir dosyaya aktarılması
nmap -sS -sU -T4 -A -v -iL aktif_ipler.txt komutu ile TCP ve UDP portlarının taranması