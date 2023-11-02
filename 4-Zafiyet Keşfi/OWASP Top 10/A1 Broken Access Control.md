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