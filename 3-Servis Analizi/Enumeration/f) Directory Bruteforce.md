Hedef web sitesinde gezinirken bazı dosya ve dizinleri bulabilirsiniz, ancak kullanıcı için o kadar belirgin olmayan daha gizli şeyleri bulmak için Directory Busting gibi araçları kullanabiliriz:
## Wfuzz

WFuzz, Kali Linux'ta bulunan bir komut satırı yardımcı programıdır. Web uygulamalarındaki yaygın güvenlik açıklarını fuzzing yöntemiyle keşfetmek için kullanılır. Fuzzing, herhangi bir girdinin web uygulamasını tehlikeye atıp atmadığını belirlemek için bir web uygulamasıyla bilinen birçok savunmasız girdiyi deneme kavramıdır.

wfuzz -c -W /usr/share/wfuzz/wordlist/dir/common.txt --hc 400,404,403 http://x.x.x.x

Burada -c seçeneği renkli çıktı için; -W kelime listesi için; -hc belirtilen kod/satır/kelimeler/harfler ile yanıtları gizlemek için kullanılır. Ayrıca Kali Linux'unuzda yerleşik olarak bulunur.

![[Pasted image 20231102193807.png]]
## DirBuster

DirBuster, web / uygulama sunucularındaki dizinleri ve dosya adlarını kaba kuvvetle bulmak için tasarlanmış çok iş parçacıklı bir java uygulamasıdır. DirBuster toplam 9 farklı liste ile birlikte gelir; bu da DirBuster'ı gizli dosya ve dizinleri bulmada son derece etkili kılar.

Benzer şekilde, terminali açın ve Dirbuster yazın, ardından aşağıdaki resimde gösterildiği gibi hedef URL'yi girin ve kaba kuvvet saldırısı için /usr/share/dirbuster/wordlis/ directory-list-2-3-medium.txt dosyasına göz atın.  
  
Dir seçeneğini /dvwa ile başlatmak için seçin, aracı saldırı için yapılandırdıktan sonra başlat'a tıklayın.

![[Pasted image 20231024115047.png]]
![[Pasted image 20231024115126.png]]