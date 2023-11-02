Açıklama  
Kullanıcının kimliğinin doğrulanması, kimlik doğrulama ve oturum yönetimi, kimlik doğrulama ile ilgili saldırılara karşı koruma sağlamak için kritik öneme sahiptir. Uygulama aşağıdaki durumlarda kimlik doğrulama zayıflıkları yaşayabilir:  
  
- Saldırganın geçerli kullanıcı adları ve parolaların bir listesine sahip olduğu kimlik bilgisi doldurma gibi otomatik saldırılara izin verirse  
  
- Kaba kuvvet veya diğer otomatik saldırılara izin verirse  
  
- "Password1" veya "admin/admin" gibi varsayılan, zayıf veya iyi bilinen parolalara izin verirse  
  
- Güvenli hale getirilemeyen "bilgiye dayalı cevaplar" gibi zayıf veya etkisiz kimlik bilgisi kurtarma ve şifremi unuttum süreçleri kullanırsa
  
- Düz metin, şifreli veya zayıf karma parolalı veri depoları kullanırsa (bkz. A02:2021-Kriptografik Hatalar).  
  
- Eksik veya etkisiz çok faktörlü kimlik doğrulaması varsa  
  
- URL'de oturum tanımlayıcısını gösterirse 
  
- Başarılı oturum açma işleminden sonra oturum tanımlayıcısını yeniden kullanın.
  
- Oturum Kimliklerini doğru şekilde geçersiz kılmıyor. Kullanıcı oturumları veya kimlik doğrulama belirteçleri (özellikle çoklu oturum açma (SSO) belirteçleri), oturum kapatma veya hareketsizlik süresi sırasında düzgün bir şekilde geçersiz kılınmazsa


Örnek Saldırı Senaryoları:

Senaryo #1: Kimlik bilgisi doldurma, bilinen parolaların listelerinin kullanılması, yaygın bir saldırıdır. Bir uygulamanın otomatik tehdit veya kimlik bilgisi doldurma koruması uygulamadığını varsayalım. Bu durumda uygulama, kimlik bilgilerinin geçerli olup olmadığını belirlemek için bir parola kahini olarak kullanılabilir.  
  
Senaryo #2: Kimlik doğrulama saldırılarının çoğu, parolaların tek faktör olarak kullanılmaya devam edilmesi nedeniyle gerçekleşir. Bir zamanlar en iyi uygulamalar olarak kabul edilen parola rotasyonu ve karmaşıklık gereksinimleri, kullanıcıları zayıf parolaları kullanmaya ve yeniden kullanmaya teşvik eder. Kuruluşların NIST 800-63 uyarınca bu uygulamaları durdurmaları ve çok faktörlü kimlik doğrulama kullanmaları önerilir.  
  
Senaryo #3: Uygulama oturumu zaman aşımları doğru ayarlanmamış. Bir kullanıcı bir uygulamaya erişmek için herkese açık bir bilgisayar kullanıyor. Kullanıcı "oturumu kapat" seçeneğini seçmek yerine tarayıcı sekmesini kapatır ve uzaklaşır. Bir saldırgan bir saat sonra aynı tarayıcıyı kullanır ve kullanıcının kimliği hala doğrulanmıştır.