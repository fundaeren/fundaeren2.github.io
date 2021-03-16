# KULLANICI İŞLEMLERİ

Kullanıcı değiştirme için su komutu kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109428279-7880d180-7a07-11eb-850d-0e2121cf78e9.png)

Root olmak için sudo komutu kullanılır.
Yeni kullanıcı ekleme için sudo adduser name dizilimi kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109428283-7cacef00-7a07-11eb-9736-93634101cda9.png)

Kullanıcı şifresini değiştirmek için passwd parametresi kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109428286-8171a300-7a07-11eb-852a-858365612785.png)

## Kullanıcı silme

![image](https://user-images.githubusercontent.com/55113204/109428293-89314780-7a07-11eb-9a0f-97261ba10239.png)
 
-r parametresi ile kullanıcıya ait her şeyi sileriz.

## Grup oluşturma

![image](https://user-images.githubusercontent.com/55113204/109428297-90f0ec00-7a07-11eb-9fdc-b89dab35c050.png)
 
## Grup silme
 
![image](https://user-images.githubusercontent.com/55113204/109428300-964e3680-7a07-11eb-8793-cbebdee6aaf4.png)

## Kullanıcının üye olduğu grupları gösterme

![image](https://user-images.githubusercontent.com/55113204/109428305-9a7a5400-7a07-11eb-9b6d-8f3cdce388ac.png)

## Kullanıcıyı yetkilendirme

![image](https://user-images.githubusercontent.com/55113204/109428310-a0703500-7a07-11eb-89bd-4fe72f4c2cdc.png)

## Kullanıcıyı kilitleme

![image](https://user-images.githubusercontent.com/55113204/109428311-a49c5280-7a07-11eb-9fe9-05e5b50c9b7f.png)

## Kullanıcının kilidini kaldırma

![image](https://user-images.githubusercontent.com/55113204/109428315-a9610680-7a07-11eb-83a2-2a015f680623.png)

## Kullanıcı sayısı alma

![image](https://user-images.githubusercontent.com/55113204/109428321-ac5bf700-7a07-11eb-9510-641ea684f96c.png)


# GÜNCELLEME, KURMA VE KALDIRMA İŞLEMLERİ

## GÜNCELLEME

Bu komut depolarda olan yeni sürümleri günceller.

### apt-get update

yeni sürümleri kontrol edilip bildirilmiş paketlerin en son versiyonlarına günceller.

### apt-get upgrade

hem güncelleme yapar hemde sistemdeki gereksiz paketleri siler.

### apt-get dist-upgrade

depodan indirilen tüm paketlerin silinmesini sağlar sistem tertemiz olur.

### apt-get clean

eski sürüm olan artık kullanılmayan paketleri siler.

### apt-get autoclean

silinen uygulamadan geriye kalmış ve artık kullanılmayan paketleri siler.

### apt-get autoremove

-y parametresi otomatik olarak yes olarak sistemi devam ettirir bizden cevap beklemeden yes diyerek sistem kesintisiz çalışır.

## KURMA

## Depodan kurulum ile program kurmak

Sistemimiz güncel ise ve program depoda varsa apt-get install program_adı şeklinde programlarımızı kurarız. 
Programın depoda olup olmadığını kontrol etmek için apt-cache search program_adı komutu ile girer bakar kontrol ederiz. Tekrar konsola programın adını yazarak teyit edebiliriz.

## Program kaldırma

Kurulan program kaldırmak istiyorsak apt-get remove program_adı şeklinde girdiğimizde otomatik olarak kaldırırız. 
Programın yapılandırma dosyalarını sistemden kaldırmak istiyorsak apt-get - -purge remove program_adı ile kaldırabiliriz.

## Paket yönetim sistemi ile kurulum

Debian paketleme sistemine sahip olduğu için kali uzantı olarak .deb olarak kurulum gerçekleştirebiliriz.
Dpkg -i dosya_adı.deb ile program kurarız.
Dpkg -r dosya_adı ile sileriz.
/etc altındaki paketlerini de silmek istersek -p parametresi kullanırız.
Paketleri tekrar yapılandırmamız gerekirse reconfigure dosya_adı şeklinde yazarız.
-l parametresi ile tüm parametreler hakkında bilgi alırız.

Çıktıda yer alan paketlerin sol tarafındaki ifadelerin anlamı:
ii : paket normal olarak sisteme yüklendi.
rc : paket yüklendikten sonra silindi ancak konfigürasyon dosyaları halen mevcut.
pn : paket konfigürasyon dosyaları ile birlikte sistemden kaldırıldı.

Kurulu paketin durumu için dpkg -s program_adı şeklinde paketin durumunu öğrenebiliriz.

Kurulu paketin içeriğini öğrenmek istersek dpkg -L parametresini kullanırız.

Indirdiğimiz paketleri kurmadan içeriğini görmek istiyorsak dpkg -c parametresi kullanırız.

Sistemden kaldırılmış paketleri dpkg - - get – selections ile görürüz.

Bu paketi daha sonraya yedeklemek istersek dpkg - - get – selections > yedeklenecek_dosya şeklinde yazarız.

Yedeklenen dosyaları başka bir sisteme tek seferd yüklemek için;
dpkg - - set – selections > yedeklenecek_dosya

Eksik olan bişey varsa onları güncellemek için ise;
apt-get deselect-upgrade komutu ile yaparız.

# JOKER KARAKTERLERİN KULLANIMI

Tek seferde birden fazla dosyaya işlem yapan karakterlere joker karakterler denir. 
Asterix işareti : ‘*’ rm funda* yaparsak funda ile ilgili her şeyi silmiş oluruz.

![image](https://user-images.githubusercontent.com/55113204/109428425-28eed580-7a08-11eb-9a1a-b7cd9448de87.png)

? karakteri

Birbirine yakın yazılışlara yakın dosyaları görüntülememizi sağlar.

![image](https://user-images.githubusercontent.com/55113204/109428431-2e4c2000-7a08-11eb-866f-befeb41502e1.png)
 
[] karakteri

Istenilen değerler parantez içinde belirtilerek çağırılır.

![image](https://user-images.githubusercontent.com/55113204/109428443-373cf180-7a08-11eb-861f-5658ec02dbf9.png)

[!değer] burada belirtilen değerler haricindeki değerleri basar.
[değer-değer] aralıklarını basar

# AĞ BAĞLANTI KOMUTLARI

## ifconfig Komutu

Ağ bağlantı kartlarını listelemek için kullanılır. Eth ethernet kartları hakkında bilgi vermektedir.
Lo localhost hakkında bilgi vermektedir.
Wlan0 ise kablosuz ağ hakkında bilgi vermektedir.
Ifconfig kart_adı ile tüm kartları değil istediğimiz kartı listeleyebiliriz.
Eth0 ip adresini değiştirmek istiyorsak sudo ifconfig eth0 ip_adres şeklinde yapabiliriz.
ağları kapatmak istersek ifconfig ağ_adı down yaparız. ifconfig ağ_adı up ile de geri açarız.

## Ping Komutu

Ağın ayakta olup olmadığını kontrol eden komuttur. Sınırlı sayıda pinglemek istersek -c parametresi kullanılır.
Route komutu
Sistemimizdeki ip yönlendirme tablosunun içeriğini görmemizi sağlayan komuttur.

## traceroute Komutu

Belirli bir yere gönderilen iplerin hangi hostlar üzerinden geçtiğini gösteren komuttur.

## whois Komutu

Domain hakkında bilgiler veren yani domain ne zaman kurulmuş, ne zamana kadar geçerli, kimin üzerine kayıtlı bunun gibi bilgileri verir.

## host Komutu

Host hakkında bilgi almamızı sağlar.

![image](https://user-images.githubusercontent.com/55113204/109428480-59cf0a80-7a08-11eb-818d-c460f269867c.png)

## dig Komutu

Dns kayıtlarına bakmak için kullanılan komuttur.

![image](https://user-images.githubusercontent.com/55113204/109428497-62bfdc00-7a08-11eb-9044-bd7ffffbb699.png)

## arp Komutu

Mac ve ip eşleşmesinin tablolandığı komuttur.

![image](https://user-images.githubusercontent.com/55113204/109428510-69e6ea00-7a08-11eb-9878-e11a51d8bea0.png)

## tcpdump Komutu

Sisteme yapılan ve sistemin yaptığı bağlantıları anlık olarak görüntüleyen komuttur.

![image](https://user-images.githubusercontent.com/55113204/109428526-753a1580-7a08-11eb-9712-535ba3674d5c.png)

Direk olarak bağlantıları görüntülemek istersek ise -n parametresi kullanırız.

![image](https://user-images.githubusercontent.com/55113204/109428573-a87ca480-7a08-11eb-8349-522d4c55c4d4.png)

# cron Komutu

Cron belirlenmiş zamanda belirlenmiş görevi yerine getiren komuttur.
Öncelikle cron ayakta mı değil mi ona bakıyoruz. Evet cron şu anda aktif durumda.

![image](https://user-images.githubusercontent.com/55113204/109428582-b0d4df80-7a08-11eb-9d09-df4ab41a0b02.png)

Cron dosyasının nerede olduğunu /etc dizinin içinde bulabiliriz.

![image](https://user-images.githubusercontent.com/55113204/109428590-b7fbed80-7a08-11eb-9515-e96afc3ec310.png)

Düzenleme yapmak için -e parametresini kullanırız.

![image](https://user-images.githubusercontent.com/55113204/109428594-bd593800-7a08-11eb-8aa6-5a663cc8573b.png)

Crontabları listelemek istediğimizde -l parametresini kullanırız.

![image](https://user-images.githubusercontent.com/55113204/109428599-c1855580-7a08-11eb-8374-e5e4b4d74bd9.png)

Oluşturduğumuz tüm crontabları silmek istersek -r parametresini kullanırız.

# LOG DOSYALARI

Log dosyaları kayıt dosyalarıdır. Bu dosyalarının nereden kaynaklandığını syslog konfigürasyon dosyasından bakabiliriz. 

![image](https://user-images.githubusercontent.com/55113204/109979246-bd5e7e00-7d0f-11eb-86a2-dbdd12a7bc90.png)
 
Sisteme şuanda bağlı olan kullanıcıların varlığını listeleyen log komutu /var/run ls ile bunu listelemekteyiz.

![image](https://user-images.githubusercontent.com/55113204/109979269-c3ecf580-7d0f-11eb-9b8b-259da8ceebee.png)

var/run içindeki who komutu sistemin son başlatılmasında hangi kullanıcının aktif olduğunu ve ne zaman aktif olduğunu görüntülemekteyiz. Ayrıca hangi id aldığını da görmekteyiz.

![image](https://user-images.githubusercontent.com/55113204/109979288-c8b1a980-7d0f-11eb-896a-c8e7e8363981.png)

Utmp şuandaki bağlanan kullanıcılar hakkında bilgi verirken wtmp ise daha önce bağlanmış kullanıcılar hakkında bilgi vermektedir.

![image](https://user-images.githubusercontent.com/55113204/109979308-cd765d80-7d0f-11eb-8891-face8cf14950.png)

Last hem geçmişte hemde şuanda kayıtlı ola kullanıcıları listeler.

![image](https://user-images.githubusercontent.com/55113204/109979329-d23b1180-7d0f-11eb-9fc8-c09e22224ed4.png)

Bad logların listesini lastb komutu ile bakarız.

![image](https://user-images.githubusercontent.com/55113204/109979345-d6ffc580-7d0f-11eb-84c2-a78a8323d44d.png)

Syslog ağ üzerinden gelen TCP UDP portlarını dinleyenilen bir C kütüphanesidir. 

Ryslog ise ip bazlı kısaltmalar ile herhangi bir bilgiyi log dosyasını istediğimiz bir log dosyasına yönlendirebiliriz. 


