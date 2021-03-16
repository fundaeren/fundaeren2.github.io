# Linux Dosya Sistem Hiyerarşisi Nedir?

Dosy Sistem Hiyerarşisi linux bir kök dizin yapısına sahiptir. Öncelikle root olan kök dizinden sırasıyla alt dizinlere doğru ayrılır. Bu ayrılma / ile gösterilmektedir. Kök dizinimiz bizi en yetkili kullanıcımız anlamına gelmektedir. Onun sistemde yaptığı değişiklikler yetkili olduğu için bir soruna sebep olmamaktadır. Sistemde bir dizin yada dosyada kalıcı değişiklikler yapılması için yetki yükseltilmesi yapılıp root olunması gerekmektedir. Alt dizinlere yarılan linux dağıtık bir sistemdir. Dağıtık sistem tek bir makinede tüm özelliklerin bulunmamasıdır. Ağ üzerinden iletişim halinde olan bir çok makine farklı sunucuları farklı makinelere kullanıp ağ üzerinden iletişime geçebilir. Bu şekilde tek bir makinenin yükü azalarak performansı artmaktadır.

## /bin

Temel komutlar bu dizinde çalışmaktadır. Sistemde herhangi bir sorun olduğunda bin dizini çalışmaya devam etmektedir. Komutlar çalışmaya devam ettiğinden dolayı sistemdeki sorun /bin dizini sayesinde düzelebilmektedir.

![image](https://user-images.githubusercontent.com/55113204/109427367-2d64bf80-7a03-11eb-9a87-2d0531006495.png)

## /boot

Sistemi boot etmek işletim sitemine ulaşarak bilgisayar açılırken öncelik verdiğimiz sistemin yüklenerek sisteme güç vermesi demektir. Sistemin boot öncelik ayarlarını değiştirebilmek için BIOS a girmemiz gerekir. BIOS donanım çalışırken işletim sistemi ile aradaki iletişimi kuran yazılım işletim sisteminin nereden yükleneceğini bileni donanımsal protokolleri belirleyen ve işletim sisteminin öncelikle hangi donanımı okumasını sağlayan yazılımdır.
 
![image](https://user-images.githubusercontent.com/55113204/109427438-7e74b380-7a03-11eb-9854-87dfd9e87c23.png)

## /dev

Linuxtaki herşey dosya şeklinde dizinlere ayrılmıştır bunların içine donanım aygıtları olan fare, modem gibi aygıtların bağlandığı portlar olan tty dizini, birincil ses kayıtlarının olduğu dsp aygıtlarını içerir.
 
![image](https://user-images.githubusercontent.com/55113204/109427461-977d6480-7a03-11eb-83e7-b6afabaa6988.png)

## /etc

Sisteme dair tüm yapılandırmaları ve bilgisayara özel yapılandırmaları içermektedir. Çalıştırılabilir dosyalar bulunmamaktadır. 
 
![image](https://user-images.githubusercontent.com/55113204/109427454-90565680-7a03-11eb-9857-3f9b969c6ab4.png)


## /home

Kişisel verilerinin depolandığı, başka programlara yaptığı değişiklikler burada depolanmaktadır. Ayrıca kullanıcının resim, müzik gibi dosyaları da burada tutulmaktadır.
 
![image](https://user-images.githubusercontent.com/55113204/109427464-9f3d0900-7a03-11eb-843f-d76cf7e43c78.png)

## /initrd

Çekirdek yüklenmesinden sonra oluşan bellek diskin üzerinde root olarak açılmasını sağlamaktadır.

## /lib

Çekirdeğe ai tolan modüller ve kütüphane dosyaları burada tutulmaktadır.
 
![image](https://user-images.githubusercontent.com/55113204/109427469-a532ea00-7a03-11eb-881e-cdee180c1728.png)

## /mnt

Sabit disk ve tüm donanımsal aygıtların bağlanma noktasır. İşletim sisteminin kurulu olduğu disk buna değildir.

## /opt

İşletim sisteminden bağımsız, kurulumu zorunlu olmayan programların bulunduğu dizindir.

## /proc

![image](https://user-images.githubusercontent.com/55113204/109427478-af54e880-7a03-11eb-9478-aa7e2dee9f6e.png)

Fiziksel dosyaların bulundurulmadığı donanımsal yapılandırmalar, süreç, bağlı aygıtların bulunduğu sanal bir dosya sistemidir.
 
## /root

Yetkilendirme olarak en üst yetkiye sahip olan kulllanıcıdır. Sistemdeki tüm değişikliklere izini bulunmaktadır. Kullanıcı olarak yapılamayacak tüm işlemleri root olarak yapılandırılabilir. Kalıcı olarak root olmamıza sistem izin vermemektedir. Geçici olarak root olma yetkisi için sudo komutu kullanılır ve sistem root olmanız için makinenin parolasını istemektedir.

## /sbin

Root tarafında kullanılacak yönetimsel ve bakımsal programlar bu dizin altında tutulmaktadır. Genellikle sistem yöneticisi tarafından kullanılmaktadır.

![image](https://user-images.githubusercontent.com/55113204/109427496-b67bf680-7a03-11eb-8aa0-4512f18c7d0f.png)

## /user

Sadece kullanılan makineye özel local klasör olan usr komutlar, programlar, kütüphaneler gibi tüm kullanıcılara paylaşılan verileri içeren dizindir.

## /var

Sisteme ait güvenlik duvarını ve sisteme düşen logları görüntülemek için ve e-posta, yazıcı kuyrukları bu dizin altında tutulmaktadır.

## /tmp

Geçici programların depolandığı dizindir. Belirli zaman aralıklarında temizlendiğinden dolayı önemli programları buraya kurmamalısınız. Çünkü makine yeniden başlatıldığında silinir. 

![image](https://user-images.githubusercontent.com/55113204/109427509-c3004f00-7a03-11eb-8250-c76e01816e29.png)

