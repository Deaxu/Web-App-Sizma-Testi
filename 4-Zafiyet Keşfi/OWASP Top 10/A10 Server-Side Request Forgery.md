---
sticker: lucide//folder-closed
---
SSRF açıkları, bir web uygulaması kullanıcı tarafından sağlanan URL'yi doğrulamadan uzak bir kaynağı getirdiğinde ortaya çıkar. Bir saldırganın, bir güvenlik duvarı, VPN veya başka bir tür ağ erişim kontrol listesi (ACL) ile korunsa bile, uygulamayı beklenmedik bir hedefe hazırlanmış bir istek göndermeye zorlamasına olanak tanır.  
  
Modern web uygulamaları son kullanıcılara kullanışlı özellikler sağladıkça, bir URL'nin getirilmesi yaygın bir senaryo haline gelmektedir. Sonuç olarak, SSRF görülme sıklığı artmaktadır. Ayrıca, bulut hizmetleri ve mimarilerin karmaşıklığı nedeniyle SSRF'nin ciddiyeti daha yüksek hale gelmektedir.

Örnek Saldırı Senaryoları:

Saldırganlar SSRF'yi web uygulaması güvenlik duvarları, güvenlik duvarları veya ağ ACL'leri arkasında korunan sistemlere saldırmak için aşağıdaki gibi senaryolar kullanarak kullanabilir:  
  
Senaryo #1: Dahili sunucularda port taraması - Ağ mimarisi bölümlere ayrılmamışsa, saldırganlar dahili ağların haritasını çıkarabilir ve bağlantı sonuçlarından veya SSRF yük bağlantılarını bağlamak veya reddetmek için geçen süreden dahili sunucularda portların açık veya kapalı olup olmadığını belirleyebilir.  
  
Senaryo #2: Hassas verilere maruz kalma - Saldırganlar file:///etc/passwd ve http://localhost:28017/ gibi hassas bilgileri elde etmek için yerel dosyalara veya dahili hizmetlere erişebilir.  
  
Senaryo #3: Bulut hizmetlerinin meta veri deposuna erişim - Çoğu bulut sağlayıcısı http://169.254.169.254/ gibi meta veri deposuna sahiptir. Bir saldırgan hassas bilgiler elde etmek için meta verileri okuyabilir.  
  
Senaryo #4: Dahili hizmetleri tehlikeye atma - Saldırgan, Uzaktan Kod Yürütme (RCE) veya Hizmet Reddi (DoS) gibi başka saldırılar gerçekleştirmek için dahili hizmetleri kötüye kullanabilir.