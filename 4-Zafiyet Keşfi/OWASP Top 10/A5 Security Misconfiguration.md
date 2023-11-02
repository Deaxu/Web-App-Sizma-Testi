
Uygulama güvenlik açığına sahip olabilir:  
  
- Uygulama yığınının herhangi bir bölümünde uygun güvenlik sağlamlaştırmasının olmaması veya bulut hizmetlerinde izinlerin yanlış yapılandırılması.  
  
- Gereksiz özellikler etkinleştirilir veya yüklenir (örneğin, gereksiz bağlantı noktaları, hizmetler, sayfalar, hesaplar veya ayrıcalıklar).  
  
- Varsayılan hesaplar ve parolaları hala etkin ve değişmemiş durumdadır.  
  
- Hata işleme, kullanıcılara yığın izlerini veya diğer aşırı bilgilendirici hata mesajlarını gösterir.  
  
- Yükseltilmiş sistemler için en son güvenlik özellikleri devre dışı bırakılır veya güvenli bir şekilde yapılandırılmaz.  
  
- Uygulama sunucuları, uygulama çerçeveleri (örn. Struts, Spring, ASP.NET), kütüphaneler, veritabanları vb. içindeki güvenlik ayarları güvenli değerlere ayarlanmamıştır.  
  
- Sunucu güvenlik üstbilgileri veya yönergeleri göndermiyor ya da bunlar güvenli değerlere ayarlanmamış.

Örnek Saldırı Senaryoları:

Senaryo #1: Uygulama sunucusu, üretim sunucusundan kaldırılmamış örnek uygulamalarla birlikte gelir. Bu örnek uygulamalar, saldırganların sunucuyu ele geçirmek için kullandığı bilinen güvenlik açıklarına sahiptir. Bu uygulamalardan birinin yönetici konsolu olduğunu ve varsayılan hesapların değiştirilmediğini varsayalım. Bu durumda, saldırgan varsayılan parolalarla oturum açar ve yönetimi ele geçirir.  
  
Senaryo #2: Dizin listeleme sunucuda devre dışı bırakılmamıştır. Bir saldırgan dizinleri kolayca listeleyebileceğini keşfeder. Saldırgan derlenmiş Java sınıflarını bulur ve indirir, kodu görüntülemek için derlemeyi açar ve tersine mühendislik yapar. Saldırgan daha sonra uygulamada ciddi bir erişim kontrolü açığı bulur.  
  
Senaryo #3: Uygulama sunucusunun yapılandırması, yığın izleri gibi ayrıntılı hata mesajlarının kullanıcılara döndürülmesine izin verir. Bu, hassas bilgileri veya güvenlik açığı olduğu bilinen bileşen sürümleri gibi temel kusurları potansiyel olarak açığa çıkarır.  
  
Senaryo #4: Bir bulut hizmet sağlayıcısı (CSP), diğer CSP kullanıcıları tarafından internete açık varsayılan paylaşım izinlerine sahiptir. Bu, bulut depolama alanında saklanan hassas verilere erişilmesini sağlar.