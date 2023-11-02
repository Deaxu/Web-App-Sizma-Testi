OWASP Top 10 2021'e dönecek olursak, bu kategori aktif ihlallerin tespit edilmesine, artırılmasına ve bunlara yanıt verilmesine yardımcı olmak içindir. Günlük kaydı ve izleme olmadan ihlaller tespit edilemez. Yetersiz günlük kaydı, tespit, izleme ve aktif müdahale her zaman gerçekleşir:  
  
Girişler, başarısız girişler ve yüksek değerli işlemler gibi denetlenebilir olaylar günlüğe kaydedilmez.  
  
Uyarılar ve hatalar hiç, yetersiz veya belirsiz günlük mesajları oluşturur.  
  
Uygulamaların ve API'lerin günlükleri şüpheli etkinliklere karşı izlenmez.  
  
Günlükler yalnızca yerel olarak saklanır.  
  
Uygun uyarı eşikleri ve yanıt eskalasyon süreçleri mevcut veya etkili değildir.  
  
Dinamik uygulama güvenlik testi (DAST) araçları (OWASP ZAP gibi) tarafından yapılan sızma testleri ve taramalar uyarıları tetiklemez.  
  
Uygulama gerçek zamanlı veya gerçek zamana yakın aktif saldırıları tespit edemez, yükseltemez veya uyarı veremez.

Örnek Saldırı Senaryoları:

Senaryo #1: Bir çocuk sağlık planı sağlayıcısının web sitesi operatörü, izleme ve günlük kaydı eksikliği nedeniyle bir ihlali tespit edemedi. Bir dış taraf, sağlık planı sağlayıcısına bir saldırganın 3,5 milyondan fazla çocuğa ait binlerce hassas sağlık kaydına eriştiğini ve bunları değiştirdiğini bildirdi. Olay sonrası yapılan incelemede, web sitesi geliştiricilerinin önemli güvenlik açıklarını ele almadıkları tespit edilmiştir. Sistemde herhangi bir kayıt ya da izleme olmadığından, veri ihlali 2013 yılından beri, yani yedi yıldan uzun bir süredir devam ediyor olabilir.  
  
Senaryo #2: Büyük bir Hint havayolu şirketi, pasaport ve kredi kartı verileri de dahil olmak üzere milyonlarca yolcunun on yılı aşkın kişisel verilerini içeren bir veri ihlali yaşadı. Veri ihlali üçüncü taraf bir bulut barındırma sağlayıcısında meydana gelmiş ve bu sağlayıcı bir süre sonra ihlali havayolu şirketine bildirmiştir.