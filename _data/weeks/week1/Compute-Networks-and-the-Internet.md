## Veri iletişimi ve Bilgisayar Ağları - `CENG 403`

# Bölüm 1 - Giriş

> Chapter 1 - Introduction to Computer Networks and the Internet

> Bu bölümle ilgili tüm ders materyallerine [**buradan**](http://gaia.cs.umass.edu/kurose_ross/videos/1/) ulaşabilirsiniz.

---


> **`Bu ilk bölümde tüm konu başlıklarına genel bir bakış atıyoruz. Devamında konular üzerinde derinleşerek devam ediyor olacağız.`**

<br>

**Bu bölümde bu sorulara cevap arayacağız;**

- Bilgisayar ağları nedir?
- Bilgisayar ağları deyince aklımıza ne geliyor?
- Bilgisayar ağlarını ne oluşturur?
- Bilgisyar ağları neden vardır?
- İnternet nedir? Protokol nedir? İnterneti oluşturan ara-ana elemanlar nelerdir?
- Bilgisayar ağlarında karşımıza çıkan problemler nelerdir ve biz bu promlemlere nasıl çözümler getiririz?

Ve bilgisyar ağlarının temel kavramlarına değiniyor olacağız.

# 1.1 İnternet Nedir?

> What is the Internet?

>**İlgili bölümün [videolu anlatımı](https://www.youtube.com/watch?v=74sEFYBBRAY&feature=youtu.be), [](https://www.youtube.com/watch?v=74sEFYBBRAY&feature=youtu.be)[ders anlatım sunumu](http://gaia.cs.umass.edu/kurose_ross/videos/1/1/1.1_video_slides_posted.pptx).**

<p align="center">
	<a href="https://www.youtube.com/watch?v=Vywf48Dhyns">
		<img alt="the-internet" src="images/the-internet.gif" width="600">
	</a>
</p>

Ağların ağıdır. "**network of networks"**

Bu soruyu cevaplamanın birkaç yolu var. İlk olarak, İnternet'i oluşturan temel donanım ve yazılım bileşenlerini tanımlayabiliriz. İkinci olarak da interneti dağıtılmış uygulamalara hizmet sağlayan bir ağ altyapısı olarak tanımlayabiliriz.

Hadi internetin temel yapı taşları ile başlayalım.

## İnternet'nin temel yapı taşları

> The internet: a "nuts and bolts" view

**`İnternet:`** ağların ağı "**network of networks"**

- Birbirlerine ISP'ler ile bağlanırlar.


> ## ISP Nedir?

> **ISP**, *İnternet Servis Sağlayıcısı* anlamına gelen bir kısaltmadır. İnternet Servis Sağlayıcısı, kuruluşlara ve ev kullanıcılarına İnternet erişimi sağlayan bir şirkettir.  

> Kısacası, bir ISP size genellikle bir ücret karşılığında İnternet erişimi sağlar. Bir ISP olmadan, çevrimiçi alışveriş yapamaz, Facebook'a erişemez veya bu sayfayı okuyamazsınız. İnternete bağlanmak için belirli telekomünikasyon, ağ ve yönlendirme ekipmanı gerekir. ISP'ler, kullanıcıların gerekli ekipmanı içeren ağlara erişmesine izin vererek kullanıcıların İnternet bağlantısı kurmasına olanak tanır.  

> **ISS olmadan İnternete bağlanabilir miyim?**  
Hayır, kuruluşların ve ev kullanıcılarının İnternet'e erişebilmek için bir ISS'ye ihtiyacı vardır. ISP'niz çalışmıyorsa, başka bir ISP üzerinden erişiminiz olmadıkça İnternete erişemezsiniz.  

>**[[-1]](https://www.whoismyisp.org/articles/what-is-an-isp)**

**Protokoler** her yerde

- Mesajların yollanmasını, ulaşmasını  kontrol eder.
- Nedir bu protokoller; HTTP (Web), streaming video, Skype, TCP, IP, WiFi, 4G, Ethernet

Internet **standartları;**

- [RFC: Request for comments](https://github.com/hasantezcan/oyk-2020-kis-bilisim-hukuku/blob/master/days/day2.md#rfc---requests-for-comment)
- [IETF: Internet engineering task force](https://en.wikipedia.org/wiki/Internet_Engineering_Task_Force)

Niye bu standartlar var? 

Ortak bir dil konuşularak topluluklar ile çalışmaya başlandığında belirlenen orta yollar hizasında çalışmak.  kg, metre, gibi..


## İnternet servislerine(hizmetlerine) bakış

> The Internet: a “services” view

`İnternet:` Uygulamara hizmet veren **altyapıdır.**

Web, streaming video, multimedia teleconferencing, email, games, e-commerce, social media, inter-connected appliances, …

## Protokol nedir?

> What is a protocol?

### `a) İnsani protokoller:`

Güdelik hayatta farkına varmadan uyguladığımız bir protokolden başlayacak olursak; **`Saat sorma protokolü`!**

- `A:` Merhabalar
- **B:** ***Merhabalar***
- `A:` Saat kaç acaba?
- **B:** ***Saat 20.54***
- `A:` Teşekkürler

Bu normal bir ikili konuşma örneğidir(dialog). 

Karşı tarfın selamınızı almaması durumunda konuşma sonlacak, karşı tarafın Türkçe bilmemesi gibi bir durumda; sizin de bilmediğiniz bir dilse iletşim sona erecek ya da sizin de bildiğiniz bir dilse konuşma o dil ile devam edecek demektir. 

Yani B kişisinin veridiği cevaplara göre iletişimiz başka bir yönde gelişecektir. 

Bu insani bir iletişimde kullanılan iletişim ön tanımını görebilirsiniz.

### `b) Ağ protokolleri`

>Yukardaki örneğe nazaran tek fark insanlar yerini bilgisayarların alması.

İnternettiki tüm iletşim aktiviteleri protokoller ile yönetilir.

<p align="center">
	<img alt="humans-and-computer-protocols" src="images/Untitled%201.png" width="600">
</p>

> A **protocol** defines the **format** and the **order** of messages exchanged between two or more communicating entities, as well as the **actions taken** on the transmission and/or receipt of a message or other event.

---

Internet yapısına daha yakından bakalım..

# 1.2 Ağ cihazları

> The Network Edge

> **İlgili bölümün [videolu anlatımı](https://www.youtube.com/watch?v=k8NmM-hImBU&feature=youtu.be), [](https://www.youtube.com/watch?v=74sEFYBBRAY&feature=youtu.be)[ders anlatım sunumu](http://gaia.cs.umass.edu/kurose_ross/videos/1/2/1.2_video_slides_posted.pptx).**

## a. **Network Edge (Uç cihaz)**

İnternete bağlanan herhangi bir cihazı `network edge(uç cihaz)` olarak kabul edebiliriz. Nedir bunlar; bilgisayarlar, sunucular, mobil cihazlar, arabalar, buz dolapları....

<p align="center">
  <img alt="network-edge" src="images/Untitled%202.png" width="300">
  <br>
	<em>Network Edge</em>
</p>

## b. **Access networks (Ara cihazlar), physical media**

Bu paketleri taşıyan birimleri birbirine bağlayan ara cihazlardır. Bunlar kablolu veya kablosuz olabilir.

<p align="center">
  <img alt="access-networks" src="images/Untitled%203.png" width="300">
  <br>
	<em>Access networks</em>
</p>

## c. **Network Core ISP**

Bu yukarda bahsetiğimiz birimler mantıksal ya da fiziksel olarak birleştiren birimlere de ISP diyoruz.

- Birbirine bağlanmış router'lar
- Ağların ağı network of networks

<p align="center">
  <img alt="the-network-core" src="images/Untitled%202.png" width="300">
  <br>
	<em>The network core</em>
</p>

---

## `SORU:` Uç cihazlar bir sisteme (bir router'a) nasıl bağlanır?

- Akla gelen ilk ***ev senaryosunda*** kullandığınız cihaz bir access point'e bağlanıyor. Access point ISP'ye bağlanıyor. ISP de sunucuya bağlanıyor olabilir. **`"residential access net"`(konut ağları)**
- Ya da bir ***kahve dükkanında*** bulunan ***ortak ağdan*** bağlanıyor olabilirsiniz. `**"institutional access networks"` (kurumsal erişim ağları)**
- Bunların dışında direkt telefonun **4G/5G**'si ya da **wifi** ile bağlanabilirsiniz. `**"mobile access networks"**` **(mobil erişim ağları)**

# Ağlara erişim - Kablo tabanlı erişim

> Access Networks - cable-based access

Ağlara erişim sağlarken karşımıza çıkan ilk problem: ağa bağlı olan bir çok cihazın verisini bozulmadan ulaşması gereken yere gönderebilmektir.

<p align="center">
  <img alt="cable-based-access" src="images/Untitled%205.png" width="500">
</p>

Bunu sağlamak için iki farklı yaklaşımdan yararlanabiliriz. Bunlar `FDM (Frequency Division Multiplexing)` ve TDM dir.

## FDM (Frequency Division Multiplexing)

> frekansa bağlı bölümleme

Bu yaklaşımda verileri tek kablo içinde farklı frenks aralıklarında taşırız. **Pink floyd**'un [**The dark side of the moon**](https://www.youtube.com/watch?v=HW-lXjOyUWo&list=PL3PhWT10BW3Urh8ZXXpuU9h526ChwgWKy&index=1) albüm kapağında da olan -ışık prizması- beyaz ışığın içindeki farklı frekans aralıklarında saklanan renkler buna güzel bir örnektir.

<p align="center">
  <img alt="pink-floyd" src="images/Untitled%206.png" width="600">
</p>

## TDM (Time Division Multiplexing)

> zamana bağlı bölümleme

Bu yaklaşımda ise veriler frekans aralıklarına bölünerek değilde bir sıra dahilinde gönderilir. 

Önce **A cihazının** verisi göderilir sonra **B cihazının** verisi ve sonra **C cihazının**...

<p align="center">
  <img alt="TDM-and-FDM-example" src="images/Untitled%207.png" width="600">
  <br>
	<em>A four-node TDM and FDM example</em>
</p>

<br>

<p align="center">
  <img alt="TDM-and-FDM-example-2" src="images/Untitled%208.png" width="300">
</p>


> **Topology nedir?**
 
> Topoloji, yüzeylerin ve şekillerin özellikleri ile ilgilenir ancak uzunluk ve açılarla ilgilenmez. Önem verdiği konu, şekiller başka bir şekle dönüştükleri zaman değişmeyen özellikleridir. Topolojide şekiller, her yönü ile çekiştirilebilir. Basitçe ifade etmek istenirse, topolojik nesneleri yırtmadan, kesmeden ve koparmadan, sadece eğip bükerek sürekli bir şekilde bir başka nesneye dönüştürmek mümkündür.

> Örneğin bilgisayar ağları (network), hem fiziksel hem de mantıksal topolojiye dayanmaktadır. Ağ üzerindeki bütün terminaller birbirine bağlıdır. Bu ara bağlantıların haritalanması fiziksel topolojidir, veri akışı ise ağın mantıksal topolojisini belirlemektedir. Başka bir ifade ile fiziksel topoloji, ağın fiziksel tasarımını belirtirken, mantıksal topoloji, bundan bağımsız olarak ağda verilerin nasıl işlendiğini belirtmektedir.

> **[[Ağ topolojileri]](https://mail.ecomputernotes.com/computernetworkingnotes/computer-network/what-is-lan-topologies-explain-each-topology) -** *Bus, star vb...*

<br>

Bu farklı yerlerden gönderilen verilerin karışmaması için kullanılan belli başlı cihazlar vardır. 

Bu örnekte gösterilen evler **`paylaşılmış bir ağı(shared access network)`** kullanıp internete bu şekilde çıkıyorlar.

# Ağlara erişim - DSL (Digital Subscriber Line)

> Access Networks - digital subscriber line (DSL)

Bir önceki örneğe göre kedimize ait bir üyeliğimiz mevcut **(subscriber line)** ve deminkinin aksine mahallede tek bir ağ yok da herkesin kendi ağı var gibi düşünebiliriz. Tabiki teknik olarak günün sonunda mahalledeki ortak kabloya bağlanacak olan bu ev ağları ISP'lerin müşterilerine suduğu özel hizmetler olarak nitelendiriliyor.

> Bir önceki örnekde **`paylaşımlı (shared)`** bir ağ mevcut iken DSL örneğinde **`evlere atanmış (dedicated)`** bir kablo mevcut.

<p align="center">
  <img alt="A-typical-home-network" src="images/Untitled%209.png" width="500">
  <br>
	<em>A typical home network</em>
</p>

---

Bir konaktan veri nasıl göderiliyordu konuşmuştuk. Bu sefer ise bir mühendislik problemini ele alıcaz. **`Verinin Geçikmesi`**

## Verinin geçikmesi

Veri geçikmesi veri transferinde yaşayacağımız en yaygın problemdir. Oyun oynarken bağlantımız yavaşlayabilir (lag olabilir), canlı yayın izlerken paketler geçikmeli gelebilir...

<p align="center">
  <img alt="delay-packge" src="images/network.png" width="300">
</p>

Ya da farklı kaynaklardan gelen veri gelmesi durumunda bunu varış noktasında sıralamamız gerekir. Bu geçikmeleri servis kalitesi için düzenlememiz gerekir.

***Peki bu geçikmeler neden kaynaklanıyor?***

<p align="center">
  <img alt="package-transform" src="images/Group_25.png" width="500">
</p>

<!-- $$\text {paket iletim gecikmesi} = \frac{L \text { (bits)}}{R \text { (bits/sec)}} $$ -->

<p align="center">
  <img alt="package-latency" src="images/Untitled%2010.png" width="400">
</p>

**L** = paket boyutu

**R** = bağlantı iletim hızı

---

## Bağlantılar: Fiziksel medya

> Links: physical media

Bu bölümde bağlatı kabloları ile ilgili konuşacağız. Fiziksel ders ortamı var oluşursa bir ağ kablosu nasıl çakılır bunu uygulayark göreceğiz. [**RJ453U katogori 5 kabloya nasıl çakılır?**](https://www.youtube.com/watch?v=FYKN0vK6VFk) 

<p align="center">
  <img alt="RJ453U" src="images/Untitled%2011.png" width="450">
</p>

**bit:** verici / alıcı çiftleri arasında yayılan bilgicikler

**physical link:** verici / alıcı arasındakiler

**guided media:** belirlenmiş akışı takip eden sinyaller ör: bakır, fiber, coax kabloda yayılan yayınlar.

**unguided media:** serbest yayılan sinyaller ör: radyo sinyalleri

## Twisted pair (TP)

İki yalıtımlı bakır tel

- **Category 5**: 100 Mbps, 1 Gbps Ethernet
- **Category 6**: 10Gbps Ethernet

<p align="center">
  <img alt="Twisted-pair" src="images/Untitled%2012.png" width="400">
</p>

## Coaxial cable

Kablo yayını yapan kablolar.
iki eş merkezli bakır iletken 
iki yönlü (bidirectional)
multiple frequency channels on cable
100’s Mbps per channel

<p align="center">
  <img alt="Coaxial-cable" src="images/Untitled%2013.png" width="300">
</p>

## Fiber optic cable

[**Fiber optik kablolar nasıl çalışır?**](https://www.youtube.com/watch?v=0MwMkBET_5I)

- Işık atımları taşıyan cam elyaf, her atım bir bit
- Yüksek hız kapasitesi

    Yüksek hızlı noktadan noktaya iletim (10’lar-100’ler Gbps)

- Düşük hata oranı

<p align="center">
  <img alt="Fiber-optic-cable" src="images/Untitled%2014.png" width="300">
</p>

---

# 1.3 Ağ'ın temeli

> Network core

> **İlgili bölümün [videolu anlatımı,](https://www.youtube.com/watch?v=f1nUcCdQJ8Y&feature=youtu.be) [](https://www.youtube.com/watch?v=74sEFYBBRAY&feature=youtu.be)[ders anlatım sunumu.](http://gaia.cs.umass.edu/kurose_ross/videos/1/3/1.3_video_slides_posted.pptx)**

Birbirine bağlı router'lar ağı.

Uç cihazlara destek veren **router** ve **switch** dediğimiz cihazlar mevcut. Bu cihazlar paket switch denilen olayı gerçekleştiriyorlar. Paketi bir yerden alıp anahtarlayıp bir başka konuma iletiyorlar.

<p align="center">
  <img alt="anahtarlama-ve-iletme" src="images/IMG_20201012_190041.jpg" width="500">
</p>

Network Core'da iki temel işlevimiz var bunlar: **Forwarding** ve **Routing**

## **Forwarding**

**Forwarding'i** bir paketi kaynak noktadan hedef noktaya hiç bir aktarma yapmaya gerek kalmadan gerçekleşen paketi iletmi olarak açıklayabiliriz. namıdiğer **switching**. **`Yerel hareket (Local action)`**

> move arriving packets from router’s input link to appropriate router output link

## **Routing**

**Routing** ise bir paketi kaynak noktadan alıp hedef noktaya ulaştırırken arada bu paketin başka taşıyıcılar  arasında el değiştirmesi ile meydana gelir. **`Evrensel hareket (Global action)`**

Yön belirleme. 

> determine source-destination paths taken by packets

<table><tr>
<td> 
  <p align="center" style="padding: 10px">
    <img alt="Forwarding" src="images/IMG_20201012_183152_(2).jpg" width="320">
    <br>
    <em style="color: grey">Forwarding (Anahtarlama)</em>
  </p> 
</td>
<td> 
  <p align="center">
    <img alt="Routing" src="images/IMG_20201012_183158_(2).jpg" width="515">
    <br>
    <em style="color: grey">Routing (yönlendirme)</em>
  </p> 
</td>
</tr></table>

---

## Paketin İletilmesi: saklama ve yönlendirme

> Packet-switching: store-and-forward

<p align="center">
  <img alt="img-name" src="images/IMG_20201012_195659-01.jpeg" width="400">
</p>

**Neden paketler saklanır? (Paket iletimindeki geçikmeler)**

- Paketin nereye gideceği bilinmiyor olablir.
- Başka paketler bekleniyor olablir.
- Öncesinde göndersmesi gereken paketler mevcuttur.

## Paketin İletilmesi: kuyruk

> Packet-switching: queueing

**`Kuyruk hizmet kapasetisinden fazla talep oluştuğunda meydana gelir.`**

<p align="center">
  <img alt="queue" src="images/macau-photo-agency-Yww5F0Vqh0I-unsplash.jpg" width="300">
</p>

Paket iletilmesinde yaşanan kuyruklarda akla ilk **Paket kaybı yaşanır mı?** sorusu gelir.

- Paket kaybı yaşanması durumunda ne yapılması gerekir?
- Kuyruğu nasıl verimli hale getiririz?

> Bu sorulara ilerleyeden derslerede cevap arıyor olacağız.

<p align="center">
  <img alt="package loss" src="images/Untitled%2015.png" width="600">
</p>

## Paket anahtarlamaya altarnatif: Devre Anahtarlama

> Alternative to packet switching: circuit switching

Sadece hedefle sizin aranızda sadece sizin kullanımıza açık bir kanaldır.

<p align="center">
  <img alt="milatary-line" src="images/russia_phone_c0-0-2100-1224_s885x516.jpg" width="300">
</p>

Bunu askeri telefon hatlarına benzetebiliriz. İki cephe arasında iletişim kurmak için sadece birbirine bağlı telefonlar.

> **Devre anahtarlamayı iki uç cihaz arasında doğrudan bir kanal oluşturulması gibi düşünebiliriz.**

<table><tr>
<td> 
  <p align="center" style="padding: 10px">
    <img alt="packet-switching" src="images/paket-anahtalama.png.jpg" width="300">
    <br>
    <em style="color: grey">packet switching</em>
  </p> 
</td>
<td> 
  <p align="center">
    <img alt="circuit-switching" src="images/devre-ana_hteirlama.png.jpg" width="350">
    <br>
    <em style="color: grey">circuit switching</em>
  </p> 
</td>
</tr></table>

> **Devre anahtarlamanını paket anahtarlamdan en büyük farkı: paylaşımlı bir yapısının olmamasıdır.**

## Devre Anahtarlama: FDM ve TDM

> Circuit switching: FDM and TDM

FDM ve TDM hakkında **The Network Edge bölümünde** zaten konuşmuştuk. İlerleyen bölümlerde bunlardan daha detaylı bahsedicez.

<br>

## Packet switching vs Circuit switching

> Paket anahtarlama devre anahtarlamaya karşı

<table><tr>
<td> 
  <p align="center" >
    <img alt="img-name" src="images/Untitled%2016.png" width="300">
    </p> 

  ### Packet Switching

- Paylaşımlı kanal kullanımı.(Daha yoğun bir kullanımı mevcut!)
- Daha fazla kullanıcıya hizmet verebilir. Daha yaygın kullanılıyor
- 1 Gbps'lık bir bant genişliğinde yaklaşık 35 kullanıcıya hizmet verebilir. `(Kullcanıcı başı 100Mbps)`
</td>
<td> 
  <p align="center">
    <img alt="img-name" src="images/Untitled%2017.png" width="500">
  </p>

  ### Circut Switching

- Adanmış kanal kullanımı
- Daha maliyetli olduğu için az tercih edilen bir yöntem.
- 1 Gbps'lık bir bant genişliğinde en fazla 10 kullanıcıya hizmet sunabilir. `(Kullcanıcı başı 100Mbps)`
</td>
</tr></table>

## Peki `Packet Switching` , `Circut Switching`'e göre daha baskın bir yöntem mi?

Packet Switching,  çok fazla yönetim ve planlama istier ayrıca aşırı paket aktarımında kuyruk taşmaları sonucu oluşan paket kayıbı problemlerini de gidermek gerekir. 

İletim problemleri, tıkanıklık çalışmaları gibi problemleri dönem içinde iredeleyeyip bu problemleri nasıl çözümleyeceğimize bakcağız.

---

# İnternetin yapısı: Ağların ağı

> Internet structure: a “network of networks”

<p align="center">
  <img alt="img-name" src="images/Untitled%2018.png" width="500">
</p>

ISP'lerin ne oldğundan bahsetmiştik. `**Peki tüm bu ISP'leri birbirine nasıl bağlarız?**`

<p align="center">
  <img alt="img-name" src="images/Untitled%2019.png" width="500">
</p>

Tüm ISP'leri birbirine bağlamaya çalşmak **`ölçeklendirebilecek bir bağlantı değildir.`** Peki nasıl bir yol izleyebiliriz?

<p align="center">
  <img alt="img-name" src="images/Untitled%2020.png" width="500">
</p>

Bir çok olan bu ISP'leri birine bağlamak yerine **`global bir ISP*`**'ye bağlayıp ölçeklendirilebilir bir bağlantı elde edebilirz.

<p align="center">
  <img alt="img-name" src="images/Untitled%2021.png" width="500">
</p>

Tabi bu evrensel ISP işi makul bir iş tipi olacağından bu hizmeti veren başka **`Evrensel ISP'ler`** de var olacaktır. 

<p align="center">
  <img alt="img-name" src="images/Untitled%2022.png" width="500">
</p>
Bu evresel ISP'leri de birbirne bağlarken `**IXP (Internet eXchange Point)**` diye isimlendirdiğimiz kıtalar arası yüksek hızlı router'ları kullanıyoruz.

<p align="center">
  <img alt="img-name" src="images/Untitled%2023.png" width="500">
</p>

Evrensel ISP'ler kadar büyük çaplı olmasa da yine aynı mantıkta çalışan **`Regional (bölgesel) ISP`**'ler de mevcutur.

<p align="center">
  <img alt="img-name" src="images/Untitled%2024.png" width="500">
</p>

Ayrıca **`içerik sağlayıcı ağlar (content provider networks)`** -ör. Google, Microsoft gibi- hizmetleri ve içeriklerini son kullanıcılara yaklaştırmak için kendi özel ağlarını kullanabilirler.

<p align="center">
  <img alt="img-name" src="images/Untitled%2025.png" width="500">
</p>

**`tier-1`** ticari ISP'ler:  (Sprint, AT&T, Turkcell, Vodafone vb...) ulusal ya da uluslar arası şirketler.

**`content provider networks`**: (Google, Facebook vb..) Veri merkezlerini **`teir-1`** ve **`regional`** ISP'leri atlayarak internete bağlayan özel ağlar.


> **`SORU:`** **Access ISP'nin şirket bazında örneği nedir?**  
> **`Cevap:`** ?

---

# 1.4 Performans

> Performance: Delay, Loss and Throughput in Computer Networks

> **İlgili bölümün [videolu anlatımı](https://www.youtube.com/watch?v=hm1y4LsphQQ&feature=youtu.be), [](https://www.youtube.com/watch?v=74sEFYBBRAY&feature=youtu.be)[ders anlatım sunumu](http://gaia.cs.umass.edu/kurose_ross/videos/1/4/1.4_video_slides_posted.pptx).**

Bu bölümde;
- Bir ağın performansını etkileyen şeyler nelerdir?
- Bir ağın performansını nasıl ölçeriz?

gibi sorulara cevap arayacağız.


## Packet delay: four sources

> Paket geçikmesinin dört kaynağı

<p align="center">
  <img alt="Packet-delay-four-sources" src="images/Untitled%2026.png" width="500">
</p>

- **Processing Delay(İşleme geçikmesi):** Paket header'ını incelemek ve paketin nereye yönlendirileceğini belirlemek için gereken süre. **`Processing Delay,` bit-düzeyindeki hataları kontrol etmek gibi** başka sepeblerden de kaynaklanabilir. Bu işlem geçikmesi yüksek seviye router'larda mikrosaniye ya da bununda altındadır. Bu nodal processing'den sonra paket diğer router'a gitme kuyruğuna alınır. -*İlerleyen derslerde (bölüm 4) router'ların nasıl çalıştığına dair ayrıntılara değineceğiz*.-
- **Queuing Delay (Kuyruk geçikmesi)**: Kuyruğun son sırasında olan bir paketin sıranı başına geçene kadar yaşadığı geçikme. Bu kuyruk geçikmesinin uzunluğu kuyruğa alınan ve aktarılmayı bekleyen paketlerin sayısına bağlı olarak değişir.
- **Transmission Delay (Cihaz içi geçikme):**  Router'ın paketi yönlendirirken nereye yönlendireceğini anlaması için gereken sürenin büyüklüğü. (Paketi işledim, paketi etiketledim, okudumi nereye gidecekmiş öğrendim be yönlendirdim) ?!
- **Propagation Delay (İletim geçikmesi):** Bir uç noktadan bir uç noktaya iletim sırsasında yaşanan iletim geçikmesi. Yayılma hızı, bağlantının fiziksel ortamına (yani, fiber optik, bükülü çift bakır tel vb.) bağlıdır

<br>

<!-- $$dnodal = dproc + dqueue + dtrans +  dprop$$ -->

<p align="center">
  <img alt="img-name" src="images/dnodal.png" width="400">
</p>

<br>

[Transmission versus Propagation Delay simulation](https://media.pearsoncmg.com/aw/ecs_kurose_compnetwork_7/cw/content/interactiveanimations/transmission-vs-propogation-delay/transmission-propagation-delay-ch1/index.html)




> **Anoloji (benzeşim);**  
Bir akıl yürütme yolu olarak, iki şey arasındaki benzerliğe dayanan analoji, bu iki şeyden birisi hakkında varılan hükmün ve ulaşılan yargının, diğeri hakkında da geçerli olması anlamına gelir. Bu durumda, bir nesne ya da olay hakkında ileri sürülen bir yargı, ona benzeyen başka bir nesne ya da olay için de geçerlidir. **[[2]](https://www.felsefe.gen.tr/analoji-benzesim-nedir-ne-demektir/)**



## Karavan analojisi

<p align="center">
  <img alt="img-name" src="images/Untitled%2027.png" width="600">
</p>

## Packet queueing delay

> Paket kuyruğa alma gecikmesi

a: average packet arrival rate - (ortalam paket varış oranı)  
L: packet length (bits) - (paket büyüklüğü)  
R: link bandwidth (bit transmission rate) - bağlantı bant genişliği (bit aktarım hızı)

<!-- $$\text {“traffic 
intensity (yoğunluğu)”} = \frac{L .a}{R} : \frac{ \text{arrival rate of bits}}{\text{service rate of bits}}  $$ -->

<p align="center">
  <img alt="img-name" src="images/traffic-intensity.png" width="500">
</p>

La/R ~ 0: avg. queueing delay küçük  
La/R -> 1: avg. queueing delay büyük  
La/R > 1: verilen hizmetten fazla iş gelmesi durumunda ortalama geçikme sonsuzdur!

<p align="center">
  <img alt="img-name" src="images/Untitled%2029.png" width="400">
  <br>
	<em style="color: grey">Dependence of average queuing delay on traffic intensity</em>
</p>

<p align="center">
  <img alt="img-name" src="images/Untitled%2030.png" width="300">
</p>

## “Real” Internet delays and routes

> Gerçek internet üzerinde üzerindeki geçikmeler ve rotalar

**`Traceroute`** araçı; kaynaktan çıkan paketin uç noktaya gidene kadar izlediği yolu ve bu yolda gerçekleşen geçikmeyi bize gösterir.

<p align="center">
  <img alt="Traceroute" src="images/Untitled%2031.png" width="800">
</p>

Bu çıktılardan bazı sonuçlara varabiliriz:

- Geçikme sürelerine mesafe tayini yapabiliriz. Özellikle kıta atlamalarında artan geçikmeyi görebiliriz.
- Üç yıldız alamaya başladığımızda artık paketimizin bir cevap alamanığını anlayabiliriz.

Daha fazla bilgi için [www.traceroute.org](http://www.traceroute.org/)

## Packet loss

> Paket kaybı

Sınırlı kapasiteye sahip queue (buna buffer'da deriz) dolduğunda üzerine gelen paketler  kaybolacaktır. 

<p align="center">
  <img alt="img-name" src="images/Untitled%2032.png" width="600">
</p>

Paket kaybını simule eden bu animasyona [**burdan**](https://media.pearsoncmg.com/aw/ecs_kurose_compnetwork_7/cw/content/interactiveanimations/queuing-loss-applet/index.html) ulaşabilirsiniz.

## Throughput and bandwith

> Throughput ve band genişliği

Bant genişliğini bir otoban örneği üzerinden açıklamak gerekirse; otobanın birim zamanda taşıyabildiği araç sayısına **`bandwidth`** denir. Badwith'i ölçerken büyüklüklerine göre; kilobits per second (kbps), megabits bits per second (Mbps), ve gigabits per second (Gbps) gibi birimler kullanırız. 

ISP'nizden 100Mbps'lık bir internet bağlantısı aldınızğınızı düşünelim. Bu hızda bir internet bağlantısı tekil bir kullanım için günümüz standartlarında gayet tatmin edici nitelikte. Fakat evde yaşan diğer bireyler de ya da kapı komşunuz hatta ve hatta internet parolanız yeterince güçlü değilse alt katta bulunan kahvehanedeki insalar da bu 100Mbps'lık internetinize erişim sağlayıp buradan internete çıkmaya başladığında da siz bu internet bağlantısından aynı randumanı alabilecek misiniz? Ya da internet hız testi yaptığınızda hala 100Mbps bağlantı hızını görebilcek misiniz? 

**Tabiki de hayır.** Bu gibi bir senaryoda ilk başta 100Mbps olan internet hızınız 10Mbps'lara kadar hatta kullanıcı sayısı arttıkça daha da aşağılara düşebilir.

> *Peki neden? Nasıl internet 100Mbps diye aldlığım internet bağlantım bunun altına düşüyor? Benim hızım 100Mbps değil miydi?*

En başta söylediğim üzere tekil bir bağlantıda bu bandwith size çok rahat yetecektir. Yani 5 şeritli bir otobanda en orta şeritten ya da dilediğiniz şeritten 100 Km/s hızla otobanın keyfini süreceksiniz. Fakat bu yola başka arabalar çıktmaya başladığında şeritler yavaş yavaş dolmaya başlayacak en başta yaşadığınız konforlu sürüş deneyiminden ödün vermeye başlayacaksınız. Hele bir de bi kaza olursa işte o zaman ayvayı yediniz! Trafik kilit noktasına gelecek yani internet hızınız 1Mbps'lara kadar düşecek. İnternet hızında bir kaza deneyimini ağınıza bağlı 5 kişinin aynı anda torrent'den filim oyun indirmeye başladğınında nasıl cerayan edeceğini tahmin edin.

Yani demek 100Mbps diye aldığınız internet yanlızca bir bağlantı aralığı `(Bandwith)` değişkenlik gösterebilen bir değer.

Peki değişkenlik göstermeden ne olursa olsun aynı değeri görebileceğim bir internet bağlantı değeri var mı?

Var, değişmeden aynı değeri gösteren internet bağlantı değerine thorugput diyoruz. Throughtput otoban örneği üzerinden gidersek anlık zamanda desteklenen araç sayısı şekilde ifade edilebilir. Bu da nedemek otobanda anlık zamanda geçecek kim varsa aynı hızda geçecek sel de olsa depremde olsa 1000 araba da geçse aynı hızda geçecekler. Bu hız bir şekilde sağlanacak.

Yani ISP'dan throughtput değeri baz alnmış bir internet alırsanız. Yukarda da bahsettiğim gibi tüm ihtimallerden arınmış sabit bir bağlantı almış olacaksınız. Ayrıca throughput'da yine bandwith gibi kilobits per second (kbps), megabits bits per second (Mbps) gibi birimler ile ölçülür.

Tabi bu böyle bir durumda doğal olarak çok daha yüksek değerlerde bir bandwidht değeriniz olacak. Çünkü bu kavramlar birbirleri ile ilişkili kavramlar. Biri varken biri yok olan kavramlar değiller. 

**[[0]](https://www.differencebetween.com/difference-between-throughput-and-vs-bandwidth/), [[1]](https://www.youtube.com/watch?v=A_-L-kn9biw)**

<p align="center">
  <img alt="img-name" src="images/Untitled%2033.png" width="600">
</p>

Bu örnek olarak benim kendi evimde kullandığım internet bağlantı değerlerim. ISP'ımdan aldığım 25Mbps'lık bant genişliğindeki internet bağlatımdan şu an için 24.4 Mbps'lık bir anlık kullanımım mevcut.

---

# 1.5 Protokol katmanları ve Hizmet Modelleri

> Protocol layers and Their Service Models

> **İlgili bölümün [videolu anlatımı](https://www.youtube.com/watch?v=IZ_PnVXtMeY&feature=youtu.be), [](https://www.youtube.com/watch?v=74sEFYBBRAY&feature=youtu.be)[ders anlatım sunumu](http://gaia.cs.umass.edu/kurose_ross/videos/1/5/1.5_video_slides_posted.pptx).**

..

..

..

..

---

# 1.6 Güvenlik

> Networks under attack - Security

**İlgili bölümün [videolu anlatımı](https://www.youtube.com/watch?v=yukwBqSwAkg&feature=youtu.be), [](https://www.youtube.com/watch?v=74sEFYBBRAY&feature=youtu.be)[ders anlatım sunumu](http://gaia.cs.umass.edu/kurose_ross/videos/1/6/1.6_video_slides_posted.pptx).**

Ağda bulunan cihazların, ağda gezen paketlerin ağ kullanıcılarının güvenliği bizim için önemli

Ben bir hizmet sağlarken bunu nasıl güvenli verebilirim?

## Packet "sniffing"

> paket koklaması

Wireshark paket sniff için kullanılan araçlardan biri uygulama derslerinde bu araçı kullanacağız.

<p align="center">
  <img alt="Packet-sniffing" src="images/aa.jpg" width="400">
  <br>
	<em style="color: grey">Packet "sniffing"</em>
</p>

## Ip spoofing/Fake identity

Kendini başkası gibi gösteriyor.
<p align="center">
  <img alt="Ip-spoofing-Fake-identity" src="images/aa2.jpg" width="400">
  <br>
	<em style="color: grey">Ip spoofing/Fake identity</em>
</p>


## Denial of Service - DOS

> Servis dışı saldırı

Uç cihazların sunucuyu hizmet veremeyecek şekilde trafiğe boğması. Sunucu gelen tüm isteklere yanıt verebilecek bilgiye sahip olsa bile gelen aşırı talep karşısında yetişememeye başlıyor.

**Analoji:** Anaokul öğrecilerinin öğretmenlerini **"Bu ne öğretmenim?"** sorusu ile boğması gibi.

<p align="center">
  <img alt="DOS" src="images/aa3.jpg" width="300">
</p>


## Defans hattı

> Lines of defense

Bu saldırılara karşı kendimizi nasıl savunacağız?

- **Confidentiality:** Via encryption
- **Integrity checks:** digital signatures prevent/detect tampering
- **Authentication: P**roving you are who you say you are
cellular networks provides hardware identity via SIM card; no such hardware assist in traditional Internet
- **Access restrictions:** password-protected VPNs
- **Firewalls:** specialized “middleboxes” in access and core networks:

güvenlik hakkında bölüm 8'de daha detaylıca konuşuyor olacağız.

# 1.7 İnternet Tarihi

> Internet history

**İlgili bölümün [videolu anlatımı](https://www.youtube.com/watch?v=yukwBqSwAkg&feature=youtu.be), [](https://www.youtube.com/watch?v=74sEFYBBRAY&feature=youtu.be)[ders anlatım sunumu](http://gaia.cs.umass.edu/kurose_ross/videos/1/6/1.6_video_slides_posted.pptx).**

..  
..  
..  
..