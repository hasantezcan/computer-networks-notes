## Veri iletişimi ve Bilgisayar Ağları - `CENG 403`

## `Hafta 1 Uygulama dersi` - Temel Ağ Komutları ve Ağ Yapılandırma Uygulaması


> Bu bölümle ilgili ders materyaline [**buradan**](/doc/week1-lab.pdf) ulaşabilirsiniz.

---

## The internet map

[https://internet-map.net/](https://internet-map.net/)

Bu site yapılan aktif bağlantılara göre sitelerin bağlantılarını sunuyor. Bize internetin üzerinde gezen paketlerin yoğunlukla hangi hedeflere gittiğini gösteriyor. Görüldüğü üzere genelde arama motorlarına sonrasında onların üzerinden de diğer sitelere bir trafiğin olduğu görülüyor.

<p align="center">
    <img alt="imgName" src="images/lab/Untitled.png" width="600">
    <br>
    <em></em>
</p>

<p align="center">
    <img alt="imgName" src="images/lab/Untitled%201.png" width="600">
    <br>
    <em></em>
</p>

## threatmap.checkpoint.com

> [https://threatmap.checkpoint.com/](https://threatmap.checkpoint.com/)

İnternet üzerinden yapılan saldırıları gösteren bir sayfa.

<p align="center">
    <img alt="imgName" src="images/lab/Untitled%202.png" width="600">
    <br>
    <em></em>
</p>

## cybermap.kaspersky.com

[https://cybermap.kaspersky.com/](https://cybermap.kaspersky.com/)

<p align="center">
    <img alt="imgName" src="images/lab/giphy2.gif" width="600">
    <br>
    <em></em>
</p>

## spamhaus.com/threat-map

> [https://www.spamhaus.com/threat-map/](https://www.spamhaus.com/threat-map/)

Dünyada aktif olan botnet sunucularını görebileceğimiz bir harita.

<p align="center">
    <img alt="imgName" src="images/lab/Untitled%203.png" width="600">
    <br>
    <em></em>
</p>

## submarinecablemap.com

> [https://www.submarinecablemap.com/](https://www.submarinecablemap.com/)

İnternetin gizli bağlayıcıları denizler altındaki bağlantıyı bize sergileyen bir harita.

<p align="center">
    <img alt="imgName" src="images/lab/Untitled%204.png" width="600">
    <br>
    <em></em>
</p>

## lookinglass.org

> [https://lookinglass.org/](https://lookinglass.org/)

Dünya üzerindeki ISP'leri görebilceğimiz bir db.

<p align="center">
    <img alt="imgName" src="images/lab/Untitled%205.png" width="600">
    <br>
    <em></em>
</p>

[Lookinglass.org](http://lookinglass.org) üzerinden turkiye ISP'lerinden olan [**Türk telekomun](http://lg.turktelekom.com.tr/lg/index.php)** lookinglass sayfasına bağlanıp bir ip için bir ping ve bir trace route sorgusu yaptık.

<p align="center">
    <img alt="imgName" src="images/lab/Untitled%206.png" width="600">
    <br>
    <em></em>
</p>

## internetexchangemap.com

> [https://www.internetexchangemap.com/](https://www.internetexchangemap.com/)

ISP db Internet exchange point cihazlarını dünya üzerindeki yerleşimlerini gösteriyor.

Türkiyede 4 tane ISP görülüyor. Bunların dördüde İstanbul'da bulunmakta. Türkiye global ağa buralardan bağlanıyor. 

<p align="center">
    <img alt="imgName" src="images/lab/Untitled%207.png" width="600">
    <br>
    <em></em>
</p>

# Bilgisayar ağları yardımcı komutlar

## hostname

O an hangi cihazda çalıştığımızı görmek için çalıştrıdığımız çalıştırılabilirdir.

```bash
~ ❯ hostname
my-lovely-dell-xps
```

## whoami

O an hangi kullanıcı ile çalıştığımızı görmek için çalıştırdığımız çalıştırılabilirdir. 

```bash
~ ❯ whoami               
hasantezcan
```

## net user

Bu cihaza ağ üzerinde hangi aktif kullanıcılar bağlı. 

OSI katmanlarına göre Fiziksel katman cihazımızın üzerindeki ethernet portu oluyor. Sistemdeki mac adreslerini görmek için.. **MAC adresi = fiziksel adres**

## getmac

Bu komut sadece windows üzerinde çalışyor. **Linux** bir sistemde mac adresslerinizi görüntülemek isterseniz. aşşağıdaki komutu çalıştırabilirsiniz. **[[0]](https://www.cyberithub.com/how-to-list-display-find-mac-address-in-linux/)**

```bash
~ ❯ ip a | grep -i ether | awk '{print $1"\t"$2}'
link/ether	11:ab:1b:3a:34:16
link/ether	g6:25:18:9q:90:2m
```

[https://www.wireshark.org/tools/oui-lookup.html](https://www.wireshark.org/tools/oui-lookup.html) bulduğumuz bu mac adresslerini **wireshark** sitesisindeki ouı lookup araçı ile aradığımızda mac adresslerimizin hangi şirketlerle ilişkili olduğunu görebiliyoruz.

<p align="center">
    <img alt="imgName" src="images/lab/Untitled%208.png" width="600">
    <br>
    <em></em>
</p>

## ipconfig / ip a

Sanal adresllerimizi görmek için ise bu komutları kullanıyoruz. Windows kullanıyorsanız `ipconfig` ile; linux'da çalışıyorsanız `ip a`  ile çıktı alabilirsiniz.

<p align="center">
    <img alt="imgName" src="images/lab/Untitled%209.png" width="600">
    <br>
    <em></em>
</p>

ip config çıktısı - windows 10

**gateway** adresi sizi ağa çıkaran adresdir.

**maske** adresiniz ile **ip adresinizi** çarptığınızda **network adresini** bulursunuz.

<p align="center">
    <img alt="imgName" src="images/lab/Untitled%2010.png" width="600">
    <br>
    <em></em>
</p>

**ipconfig /relase :** DHCP (Dynamic Host Conf.) 'ye bağlantıyı kes demektir.

**ipconfig /renew :** DHCP yeni ip adresi istemeye yarar.

## netstats -s

Network'ün aktif bağlantılarındaki istatistiklerini verir.

<p align="center">
    <img alt="imgName" src="images/lab/Untitled%2011.png" width="600">
    <br>
    <em></em>
</p>

bu komutun linux alternatifi ise `**ss -aut`** 'dir. **[[0]](https://linux-audit.com/alternative-netstat-ss-tool/)**

```bash
~ ❯ ss -aut
Netid State      Recv-Q Send-Q                                                 Local Address:Port                                           Peer Address:Port
udp   UNCONN     0      0                                                                  *:bootpc                                                    *:*
tcp   LISTEN     0      128                                                                *:ssh                                                       *:*
tcp   ESTAB      0      0                                                      192.168.1.251:ssh                                           192.168.1.220:hnmp
tcp   LISTEN     0      128                                                               :::19531                                                    :::*
tcp   LISTEN     0      128        
```

## who.is

Bir domain'in hangi adrese ait olduğunu görmek için kullanılan araçtır.

[https://who.is/dns/pau.edu.tr](https://who.is/dns/pau.edu.tr)

<p align="center">
    <img alt="imgName" src="images/lab/Untitled%2012.png" width="600">
    <br>
    <em></em>
</p>

aynı şekilde bulduğun ip ile tersine bir arama da gerçekleştirebilirsiniz.

## ping

Send ICMP ECHO_REQUEST packets to network hosts.

```bash
~ ❯ ping hasantezcan.dev                                                  15s
PING hasantezcan.dev (185.199.111.153) 56(84) bytes of data.
64 bytes from 185.199.111.153 (185.199.111.153): icmp_seq=1 ttl=50 time=67.9 ms
64 bytes from 185.199.111.153 (185.199.111.153): icmp_seq=2 ttl=50 time=62.1 ms
64 bytes from 185.199.111.153 (185.199.111.153): icmp_seq=3 ttl=50 time=61.8 ms
64 bytes from 185.199.111.153 (185.199.111.153): icmp_seq=4 ttl=50 time=62.8 ms
^C64 bytes from 185.199.111.153: icmp_seq=5 ttl=50 time=62.2 ms

--- hasantezcan.dev ping statistics ---
5 packets transmitted, 5 received, 0% packet loss, time 20447ms
rtt min/avg/max/mdev = 61.778/63.349/67.866/2.285 ms
~ ❯
```

**ttl (time to live)** = paketi kontrol etmek için kullanılırız her adımda bir can kaybederek devam eder.

**icmp =** 

## traceroute

Print the route packets trace to network host.

```bash
~ ❯ traceroute facebook.com                                                 24s
traceroute to facebook.com (157.240.9.35), 30 hops max, 60 byte packets
 1  _gateway (192.168.0.1)  0.307 ms  0.249 ms  0.211 ms
 2  * * *
 3  172.25.20.1 (172.25.20.1)  11.352 ms  11.317 ms  9.377 ms
 4  195.175.74.113.static.turktelekom.com.tr (195.175.74.113)  8.490 ms  8.451 ms  8.417 ms
 5  20-denizli-t2-2---20-bahcelievler-t3-1.statik.turktelekom.com.tr (81.212.202.12)  9.214 ms  9.178 ms  9.145 ms
 6  35-hatay-t2-2---20-denizli-t2-2.statik.turktelekom.com.tr (195.175.169.215)  14.634 ms  14.575 ms  14.501 ms
 7  06-ulus-xrs-t2-1---35-hatay-t2-2.statik.turktelekom.com.tr (212.156.121.83)  23.368 ms  22.949 ms  22.924 ms
 8  06-ebgp-ulus-sr12e-k---06-ulus-xrs-t2-1.statik.turktelekom.com.tr (81.212.217.5)  22.913 ms  22.901 ms  22.889 ms
 9  307-sof-col-2---06-ulus-xrs-t2-2.statik.turktelekom.com.tr (212.156.104.150)  39.349 ms  39.442 ms  39.430 ms
10  ae6.pr03.sof1.tfbnw.net (157.240.72.200)  42.751 ms  42.739 ms  42.728 ms
11  po101.psw01.sof1.tfbnw.net (31.13.27.219)  39.903 ms po103.psw01.sof1.tfbnw.net (157.240.40.55)  39.891 ms po103.psw04.sof1.tfbnw.net (157.240.47.147)  39.806 ms
12  157.240.38.107 (157.240.38.107)  39.993 ms 173.252.67.167 (173.252.67.167)  39.769 ms 173.252.67.45 (173.252.67.45)  39.364 ms
13  edge-star-mini-shv-01-sof1.facebook.com (157.240.9.35)  39.330 ms  39.311 ms  39.293 ms
```