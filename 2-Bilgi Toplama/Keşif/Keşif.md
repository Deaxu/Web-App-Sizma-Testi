- HTML Kaynak Kodu
-Web sayfasına ait kaynak kodu görüntülenerek içinde hassas bilgi barındırıp barındırmadığı kontrol edilir.
![[Pasted image 20231024152645.png]]

- GİRDİ KABUL EDEN SAYFALAR
-Web sitesinde yer alan ve girdi kabul eden veya form içeren sayfalar bulunarak bu sayfalara yönelik "kaba kuvvet", "şifre tahmini", SQL injection, Insecure Direct Object References gibi saldırı yöntemleri denenebilir.
-Kullanıcı adı ve parola kabul eden bir sayfa ise bu sayfalar taklit edilerek "Phishing" saldırılarında çalışanların kullanıcı adları ve parolaları çalınabilir. Bu sayfalarda kaba kuvvet ve sözlük saldırıları gerçekleştirilebilir
![[Pasted image 20231024152822.png]]

- PARAMETRİK URL’LER
-Kullanıcıdan girdi kabul eden sayfalar gibi, parametrik URL’ler de bulunarak bu URL’lerdeki parametrelere yönelik SQL injection, XSS, dosya ekleme gibi saldırı vektörleri düzenlenebilir.
-http://www.ornek.com/login.php?username=user1&password=sifre123 
-http://example.com/getUserProfile.jsp?item=../../../../etc/passwd 
-http://www.mysite.com/accounts/id=51741054

- HATA SAYFALARI
-Hata sayfaları saldırgana hedef sistem hakkında web sunucusu adı, yazılımı, versiyonu, kullanılan programlar, dosya yolu gibi kritik bilgiler verebilir. Hata sayfalarının kritik bilgi vermeyecek şekilde özelleştirilmesi önerilmektedir.
![[Pasted image 20231024153134.png]]
