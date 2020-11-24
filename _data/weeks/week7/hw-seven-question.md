# Tekrar soruları

## `Hasan Tezcan - 17253046` - 2020/11/18


## `Soru 1` - **Throughput and bandwith ilgili açıklamalardan hangisi doğrudur.**
> Bilgisayar Ağları ve Internet - hafta 1  
*kaynak:* **[github.com/hasantezcan/computer-networks-notes](https://github.com/hasantezcan/computer-networks-notes/blob/main/_data/weeks/week1/Compute-Networks-and-the-Internet.md)**

A) Evinde bandwith'i 25Mbps'lık bir internet bağlantısı olan bir kişinin evde internetini kullanan kaç kişinin olursa olsun internet bağlantı hızı değişmez.

**B) Evinde throughput'u 25Mbps'lık bir internet bağlantısı olan bir kişinin evde internetini kullanan kaç kişinin olursa olsun internet bağlantı hızı değişmez.**

C) Throughput ile bandwith mantıken aynı şeylerdir.

D) İnternet bağlantımızı throughput değeri edinmek  bandwith ile edinmeye göre daha hesaplıdır. (25 Mbps'lık bandwith ile 25 Mbps'lık throughput internet bağlantısı kıyası)

---


## `Soru 2` - TCP ve UDP ile verilen bilgilerden hangisi doğrudur?

> Uygulama katmanı - hafta 2  
*kaynak:* **[github.com/hasantezcan/computer-networks-notes](https://github.com/hasantezcan/computer-networks-notes/blob/main/_data/weeks/week2/application-layer.md#internet-transport-protocols-services)**

A) HTTP protokülü UDP ile veri alışveirişini gerçekleştirir.

B) UDP genel olarak paket kaybının istenmediği durumlarda kullanılır.

C) TCP ile UDP arasında hiç bir fark yoktur.

**D) TCP veri güvenliğini garanti eden bir protokoldür.**

---


## `Soru 3` - DNS sunucuları ile ilgili bilgilerden hangisi doğrudur?

> Uygulama katmanı (DNS) - hafta 3  
*kaynak:* **[github.com/hasantezcan/computer-networks-notes](https://github.com/hasantezcan/computer-networks-notes)**

A) Tüm dünyada tek bir DNS sunucu kullanmak tüm verilerin tek elde sağladığı için veri güvenliği ve bütünlüğünü sağlar. 

B) Tek bir DNS sunucusu asla ve asla tüm dünyanın dns sorgusu yükünü kaldıramaz. 

C) Dünyada tek bir DNS sunucu kullanılmalıdır ve bu sunucuda da greenwich üzerine bulunmalıdır. Greenwich dünyanın merkezi olduğu için tüm dünya dns sorgularına eşit sürede cevap bulur.  

**D) Dünyadaki tüm dns sorgularına tek bir DNS sunucusu ile cevap vermek hem oluşak trafik hem yönetilebilirlik hem de yedeksizlik sebepleri ile kullanışlı bir yöntem değildir.**

---


## `Soru 4` - Taşıma katmanı fonksiyon öncelikle nerede uygulanır?

> İletim katmanı - hafta 4  
*kaynak:* **[http://gaia.cs.umass.edu/](http://gaia.cs.umass.edu/kurose_ross/)**

A) Taşıma katmanı işlevleri, öncelikle ağdaki yönlendiriciler(routers) ve anahtarlarda(switches) uygulanır.

**B) Taşıma katmanı işlevleri, öncelikle ağın "uçundaki" ana bilgisayarlarda uygulanır.**

C) Taşıma katmanı işlevleri, birincil olarak bir ana bilgisayarı/yönlendiriciyı/anahtarı diğer bir ana bilgisayara/yönlendiriciye/ anahtara bağlayan fiziksel bir bağlantının her bir ucunda uygulanır.

> Açıklama: Daha sonraki taşıma işlevleri aslında esas olarak ana bilgisayarlarda uygulanır. Bununla birlikte, ağ yönetimini incelediğimizde göreceğimiz gibi, TCP ve UDP kullanılır; ağ yönetimi işlevleri ile iletişim, bir yönlendirici veya anahtar görevi görür. Ancak normal kullanıcılar, bir yönlendiricide veya anahtarda taşıma katmanına erişmez.

---


## `Soru 5` - TCP güvenilirlik semantiği ile ilgili ifade doğru mu yanlış mı?

> İletim katmanı (TCP)- hafta 5  
*kaynak:* **[http://gaia.cs.umass.edu/](http://gaia.cs.umass.edu/kurose_ross/)**

Gönderen tarafta, TCP göndericisi, bir TCP soketine yazılan her bir uygulama katmanı veri yığınını alır ve ayrı bir TCP segmentinde gönderir. Ve sonra alıcı tarafta, TCP, uygulama tanımlı mesaj sınırını koruyarak, bir segmentin yükünü uygun sokete gönderecektir.

- Doğru
- **Yanlış**

> TCP'nin güvenilirlik semantiğinin güvenilir bir bayt akışı olduğunu unutmayın - veri baytları gönderenden alıcıya sırayla teslim edilecektir. TCP'nin dünya bayt akışı görünümünde mesaj sınırlayıcıları kavramı yoktur. Bu, uygulama tanımlı mesaj sınırlarını koruyan UDP ile çelişir.

---


## `Soru 6` - HOL (Head of the line) nedir?

> Ağ katmanı (Veri katmanı)- hafta 6  
*kaynak:* **[http://gaia.cs.umass.edu/](http://gaia.cs.umass.edu/kurose_ross/)**

- **A) Kuyruğun önünde hizmet bekleyen sıraya alınmış bir datagram, kuyruktaki diğer datagramların kuyrukta ilerlemesini engeller.**
- B) Bir kuyruğun önündeki kuyruğa alınmış bir datagram alma hizmeti, kuyruktaki diğer datagramların servis almasını engeller
- C) Bir blok hata kodunda, kodun ilk baytları, kullanılan kodlamanın türünü belirtir.

---


## `Soru 7` - DHCP'nin bir "tak ve çalıştır" protokolü olduğunu söylemekle ne kastedilmektedir?

> Ağ katmanı (Veri katmanı) - hafta 7  
*kaynak:* **[http://gaia.cs.umass.edu/](http://gaia.cs.umass.edu/kurose_ross/)**

- A) Ana bilgisayarın İnternete erişmek ("oynamak") için yerel ağa "takılması" (kablolu veya kablosuz olarak) gerekir
- B) Ağ, bir ana bilgisayarın ethernet adaptörü için bir Ethernet jakı sağlar.
- **C) Ana bilgisayarın ağa katılması için manuel konfigürasyona gerek yoktur.**