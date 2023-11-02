## TCP Nedir? (kaynak: https://berqnet.com/blog/port)

**TCP**; bilgisayarlar arası iletişimde veri alışverişinin yanı sıra kimlik doğrulaması da sağlayan bir port türüdür.

Açılımı **_Transmission Control Protocol_** olan [TCP,](https://berqnet.com/blog/tcp-ip) Amerika Savunma Bakanlığı tarafından bilgisayarlar arası iletişimde kaybı önlemek üzere geliştirilmiştir. Anlaşılır bir örnekle betimleyecek olursak TCP, akıllı telefonunuzdan Bluetooth, Airdrop, WhatsApp gibi bir aracı ile veri paylaşmaya benzer. Paylaşmanız gereken verileri paylaşırsınız ve telefonun kontrolü tamamen sizdedir.

Günümüzün bilgisayarlar arası iletişim protokollerinden en popüler olan HTTP, HTTPS, POP3, SSH, SMTP, TELNET ve FTP gibi protokoller TCP protokolünü kullanır ve her birinin kendine özel bir 0-65535 arası numarası bulunur.

## UDP Nedir?

UDP; ağırlıklı olarak ses ve video iletişiminde kullanılmak üzere geliştirilmiş bir port türüdür ve açılımı User Datagram Protocol olup Türkçe’ye Kullanıcı Veri Bloğu İletişim Kuralları olarak çevrilebilir.

TCP gibi veri bütünlüğü ve kimlik doğrulaması sorumluluğu olmamasından dolayı TCP’ye göre daha hızlı olan UDP, bu özelliğinden dolayı ne kadar hızlı olsa da daha az güvenilir olduğu anlamına geldiğinden TCP’ye bir alternatif olarak değerlendirilir. Yine basit bir örnekle anlatacak olursak TCP, bir videoyu izlemek veya bir şarkıyı dinlemek için telefonunuzu arkadaşınıza vermektir. O an telefon elinizde olmadığı için arkadaşınız eğer art niyetli ise size özel olan tüm bilgilere erişebilecektir.

## TCP ve UDP Arasındaki Farklar Nelerdir?

Yukarıda TCP ve UDP ile ilgili yapılan açıklamalarda bahsedilmiş olmakla birlikte TCP ve UDP arasındaki farkları aşağıdaki gibi özetlemek mümkündür:

- TCP, veri bütünlüğü ve kimlik doğrulaması sağladığı için UDP’ye göre biraz daha yavaştır ancak güvenilirlik açısından UDP’ten önce gelir,
- TCP, iletişim esnasında verileri paketler halinde ve sırayla gönderirken UDP’de bu yönetim akış sistemiyle sağlanır.
- TCP, bütünsel ve kayıpsız veri akışlarında tercih edilirken UDP ise ses ve video iletişiminde tercih edilir.
## Port Ne İşe Yarar?

Ne işe yaradığını tek bir cümle ile özetleyecek olursak port; **bilgisayar IP adreslerinin birden çok amaçla veri alışverişi yapabilmesini sağlayan kapılardır.**

## En Popüler Portlar

- 21 FTP
- 22 SSH
- 23 TELNET
- 25 SMTP
- 53 DNS
- 80 HTTP
- 110 POP3
- 115 SFTP
- 135 RPC
- 143 IMAP
- 194 IRC
- 443 SSL
- 445 SMB
- 1433 MSSQL
- 3306 MYSQL
- 3389 Remote Desktop

HTTP Durum Kodları ve Anlamları:

https://learning.mlytics.com/the-internet/http-response-status-codes/