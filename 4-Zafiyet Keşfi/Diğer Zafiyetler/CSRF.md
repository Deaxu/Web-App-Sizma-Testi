• CSRF (Cross-Site Request Forgery ) atağı websitesinin kullanıcıya (kullanıcının tarayıcısına) duyduğu güven ilişkisinden yararlanır.
• Tarayıcının hedef sitedeki aktif oturumundan yararlanır.
• CSRF (Cross-Site Request Forgery) atağı sayesinde yetkisiz kullanıcılar (saldırganlar), seçtiği kurbanın daha önceden giriş yaptığı bir siteye sanki kurbanın kendisi oturum yapmış gibi istek gönderebilir.
• Bu atak kullanıcının bir siteye oturum açtığı durumlarda, aynı anda saldırganın websitesini ziyaret etmesi ile ortaya çıkar.
•
İsteğin cevabı saldırgana dönmediği için, buradaki amaç daha çok sunucuda durumda değişiklik yapmaktır.
• Eğer kurban yönetici bir hesap ise sonuçlar sunucunun ele geçirilmesine kadar gidebilir. • XSS veya sosyal mühendislik saldırılarıyla birlikte kullanılır.

1. Kurban A Bankası’na giriş yapar 
2. A Bankası Kurbana Oturum Açar ve Cookie Yollar 
3. Kurban Zararlı Siteyi Ziyaret Eder 
4. Zararlı Site Üzerinde Çalışan Kod ile A Bankasına İstek Yapılır.
- Örneğin: http://www.abankasi.com.tr/havale/hesabaHavale.php?kullanici=saldirgan&hes apNo=1234567

• Sorgular daima çift adımda yapılmalı (Örneğin: Göndermek istediğinize emin misin?)
• Token kullanılmalıdır.